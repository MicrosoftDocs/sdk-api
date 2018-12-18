---
UID: NN:fsrmreports.IFsrmReportScheduler
title: IFsrmReportScheduler
author: windows-sdk-content
description: Used to manage scheduled tasks for report jobs and file management jobs.
old-location: fsrm\ifsrmreportscheduler.htm
tech.root: fsrm
ms.assetid: f3e71a39-d880-4035-a719-42ace5eeb9e0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFsrmReportScheduler, IFsrmReportScheduler interface [File Server Resource Manager], IFsrmReportScheduler interface [File Server Resource Manager],described, fs.ifsrmreportscheduler, fsrm.ifsrmreportscheduler, fsrmreports/IFsrmReportScheduler
ms.topic: interface
req.header: fsrmreports.h
req.include-header: FsrmReports.h, FsrmTlb.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FsrmReports.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmReportScheduler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmReportScheduler interface


## -description


<p class="CCE_Message">[Starting with Windows Server 2012 this interface is not supported; use the 
    <a href="https://msdn.microsoft.com/8ed0ec1c-3af2-4c49-92cf-0911473fb33a">MSFT_FSRMScheduledTask</a> WMI class to manage 
    scheduled tasks.]

Used to manage scheduled tasks for report jobs and file management jobs.

To get this interface, call the 
    <a href="https://msdn.microsoft.com/en-us/library/ms680701(v=VS.85).aspx">CoCreateInstanceEx</a> function. Use 
    <b>CLSID_FsrmReportScheduler</b> as the class identifier and 
    <code>__uuidof(IFsrmReportScheduler)</code> as the interface identifier. 
    For an example, see <a href="https://msdn.microsoft.com/7994bf40-cc9d-4519-a0d4-d48d7ec10fda">Scheduling a Report Job</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmReportScheduler</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFsrmReportScheduler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFsrmReportScheduler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/983a6d05-417f-4aea-9652-955fd96e78f0">CreateScheduleTask</a>
</td>
<td align="left" width="63%">
Creates a task that is used to trigger a report job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31541668-6173-48d4-8650-13e78bc7a763">DeleteScheduleTask</a>
</td>
<td align="left" width="63%">
Deletes a task that is used to trigger a report job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca950e00-d391-4a03-8ff9-2ddef3a17038">ModifyScheduleTask</a>
</td>
<td align="left" width="63%">
Modifies a task that is used to trigger a report job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb5139c8-e01f-48cf-a8a9-d3a3e5b86238">VerifyNamespaces</a>
</td>
<td align="left" width="63%">
Verifies that the specified local directory paths that are used as the source for the reports are 
     valid.

</td>
</tr>
</table> 


## -remarks



To enumerate the schedules for reports, call the 
    <a href="https://msdn.microsoft.com/af66beb6-e82c-47e6-8658-da9702041053">IFsrmReportManager::EnumReportJobs</a> 
    method. Use the task name in the 
    <a href="https://msdn.microsoft.com/2c9ceaca-f696-4506-bc25-efd601522560">IFsrmReportJob::Task</a> property to retrieve the 
    schedule from the <a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>. To 
    retrieve the schedule, call the 
    <a href="https://msdn.microsoft.com/27391e34-8632-4ab5-9d6e-d2fde7942f80">ITaskScheduler::Activate</a> method. (FSRM 
    supports only Task Scheduler version 1.0, not version 2.0.) Note that some report jobs may not have an associated 
    schedule.

To enumerate the schedules for file management jobs, call the 
    <a href="https://msdn.microsoft.com/4af6f794-d9d4-4e03-9cd5-a4d8769888ca">IFsrmFileManagementJobManager::EnumFileManagementJobs</a> 
    method. Use the task name in the 
    <a href="https://msdn.microsoft.com/ca562a21-5b0a-4726-9921-68c6a9fbde6c">IFsrmFileManagementJob::Task</a> property to 
    retrieve the schedule from the 
    <a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>. To retrieve the 
    schedule, call the <a href="https://msdn.microsoft.com/27391e34-8632-4ab5-9d6e-d2fde7942f80">ITaskScheduler::Activate</a> 
    method.

To create this object from a script, use the "Fsrm.FsrmReportScheduler" program 
    identifier.




## -see-also




<a href="https://msdn.microsoft.com/bbd888d9-1005-4173-8e82-ced13e68c09e">FSRM Interfaces</a>



<a href="https://msdn.microsoft.com/306f1d7f-6ad4-457a-97be-193aefeccfeb">FsrmReportScheduler</a>
 

 

