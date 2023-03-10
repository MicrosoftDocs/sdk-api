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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmReportScheduler
 - fsrmreports/IFsrmReportScheduler
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmReportScheduler
---

# IFsrmReportScheduler interface


## -description

<p class="CCE_Message">[Starting with Windows Server 2012 this interface is not supported; use the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmscheduledtask">MSFT_FSRMScheduledTask</a> WMI class to manage 
    scheduled tasks.]

Used to manage scheduled tasks for report jobs and file management jobs.

To get this interface, call the 
    <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex">CoCreateInstanceEx</a> function. Use 
    <b>CLSID_FsrmReportScheduler</b> as the class identifier and 
    <code>__uuidof(IFsrmReportScheduler)</code> as the interface identifier. 
    For an example, see <a href="/previous-versions/windows/desktop/fsrm/scheduling-a-report-job">Scheduling a Report Job</a>.

## -inheritance

The <b>IFsrmReportScheduler</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFsrmReportScheduler</b> also has these types of members:

## -remarks

To enumerate the schedules for reports, call the 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-enumreportjobs">IFsrmReportManager::EnumReportJobs</a> 
    method. Use the task name in the 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportjob-get_task">IFsrmReportJob::Task</a> property to retrieve the 
    schedule from the <a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>. To 
    retrieve the schedule, call the 
    <a href="/windows/desktop/api/mstask/nf-mstask-itaskscheduler-activate">ITaskScheduler::Activate</a> method. (FSRM 
    supports only Task Scheduler version 1.0, not version 2.0.) Note that some report jobs may not have an associated 
    schedule.

To enumerate the schedules for file management jobs, call the 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjobmanager-enumfilemanagementjobs">IFsrmFileManagementJobManager::EnumFileManagementJobs</a> 
    method. Use the task name in the 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_task">IFsrmFileManagementJob::Task</a> property to 
    retrieve the schedule from the 
    <a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>. To retrieve the 
    schedule, call the <a href="/windows/desktop/api/mstask/nf-mstask-itaskscheduler-activate">ITaskScheduler::Activate</a> 
    method.

To create this object from a script, use the "Fsrm.FsrmReportScheduler" program 
    identifier.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="/previous-versions/windows/desktop/fsrm/fsrmreportscheduler">FsrmReportScheduler</a>
