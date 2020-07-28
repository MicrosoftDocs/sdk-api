---
UID: NN:fsrmreports.IFsrmReportScheduler
title: IFsrmReportScheduler (fsrmreports.h)
description: Used to manage scheduled tasks for report jobs and file management jobs.
helpviewer_keywords: ["IFsrmReportScheduler","IFsrmReportScheduler interface [File Server Resource Manager]","IFsrmReportScheduler interface [File Server Resource Manager]","described","fs.ifsrmreportscheduler","fsrm.ifsrmreportscheduler","fsrmreports/IFsrmReportScheduler"]
old-location: fsrm\ifsrmreportscheduler.htm
tech.root: fsrm
ms.assetid: f3e71a39-d880-4035-a719-42ace5eeb9e0
ms.date: 12/05/2018
ms.keywords: IFsrmReportScheduler, IFsrmReportScheduler interface [File Server Resource Manager], IFsrmReportScheduler interface [File Server Resource Manager],described, fs.ifsrmreportscheduler, fsrm.ifsrmreportscheduler, fsrmreports/IFsrmReportScheduler
f1_keywords:
- fsrmreports/IFsrmReportScheduler
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmReportScheduler interface


## -description


<p class="CCE_Message">[Starting with Windows Server 2012 this interface is not supported; use the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmscheduledtask">MSFT_FSRMScheduledTask</a> WMI class to manage 
    scheduled tasks.]

Used to manage scheduled tasks for report jobs and file management jobs.

To get this interface, call the 
    <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex">CoCreateInstanceEx</a> function. Use 
    <b>CLSID_FsrmReportScheduler</b> as the class identifier and 
    <code>__uuidof(IFsrmReportScheduler)</code> as the interface identifier. 
    For an example, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/scheduling-a-report-job">Scheduling a Report Job</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmReportScheduler</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFsrmReportScheduler</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportscheduler-createscheduletask">CreateScheduleTask</a>
</td>
<td align="left" width="63%">
Creates a task that is used to trigger a report job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportscheduler-deletescheduletask">DeleteScheduleTask</a>
</td>
<td align="left" width="63%">
Deletes a task that is used to trigger a report job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportscheduler-modifyscheduletask">ModifyScheduleTask</a>
</td>
<td align="left" width="63%">
Modifies a task that is used to trigger a report job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportscheduler-verifynamespaces">VerifyNamespaces</a>
</td>
<td align="left" width="63%">
Verifies that the specified local directory paths that are used as the source for the reports are 
     valid.

</td>
</tr>
</table> 


## -remarks



To enumerate the schedules for reports, call the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-enumreportjobs">IFsrmReportManager::EnumReportJobs</a> 
    method. Use the task name in the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportjob-get_task">IFsrmReportJob::Task</a> property to retrieve the 
    schedule from the <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>. To 
    retrieve the schedule, call the 
    <a href="https://docs.microsoft.com/windows/desktop/api/mstask/nf-mstask-itaskscheduler-activate">ITaskScheduler::Activate</a> method. (FSRM 
    supports only Task Scheduler version 1.0, not version 2.0.) Note that some report jobs may not have an associated 
    schedule.

To enumerate the schedules for file management jobs, call the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjobmanager-enumfilemanagementjobs">IFsrmFileManagementJobManager::EnumFileManagementJobs</a> 
    method. Use the task name in the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_task">IFsrmFileManagementJob::Task</a> property to 
    retrieve the schedule from the 
    <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>. To retrieve the 
    schedule, call the <a href="https://docs.microsoft.com/windows/desktop/api/mstask/nf-mstask-itaskscheduler-activate">ITaskScheduler::Activate</a> 
    method.

To create this object from a script, use the "Fsrm.FsrmReportScheduler" program 
    identifier.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrmreportscheduler">FsrmReportScheduler</a>
 

 

