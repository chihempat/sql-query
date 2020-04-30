---

copyright:
  years: 2020
lastupdated: "2020-04-29"

keywords: SQL query, disaster recovery, backup
subcollection: sql-query

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}

# Disaster recovery and backup
{: #disaster}

{{site.data.keyword.sqlquery_full}} stores information about submitted jobs, such as SQL statements, job status, and job IDs. Backups are performed on a regular basis, therefore, in case of a disaster, you can at the most lose information of the last eight hours. Backups are done automatically, so there is no action required on you side, neither for the creation of the backups, nor for their recovery.

The job results are stored in {{site.data.keyword.cos_full}} and are independent of any {{site.data.keyword.sqlquery_short}} disaster recovery.

If a region becomes unavailable due to a disaster, {{site.data.keyword.Bluemix}} will automatically replicate the service to another region in the same geography as part of the recovery. The recovery region for *us-south* is *us-east*. The recovery region for *eu-de* is *eu-gb*. You do not need to perform specific actions to replicate the service to another region in the case of a disaster.

During the time of disaster and recovery, the service at that location is not available, which means that you cannot use your instance(s) that had been created in the affected location. Once the phase of disaster recovery is over, you can access your service instances and submit new jobs, even before data recovery completes. Once data recovery completes, job history will be available for the instances again.
