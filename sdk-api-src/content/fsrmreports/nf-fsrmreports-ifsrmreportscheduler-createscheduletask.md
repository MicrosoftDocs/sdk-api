---
UID: NF:fsrmreports.IFsrmReportScheduler.CreateScheduleTask
title: IFsrmReportScheduler::CreateScheduleTask (fsrmreports.h)
description: Creates a scheduled task that is used to trigger a report job.
helpviewer_keywords: ["CreateScheduleTask","CreateScheduleTask method [File Server Resource Manager]","CreateScheduleTask method [File Server Resource Manager]","FsrmReportScheduler class","CreateScheduleTask method [File Server Resource Manager]","IFsrmReportScheduler interface","FsrmReportScheduler class [File Server Resource Manager]","CreateScheduleTask method","IFsrmReportScheduler interface [File Server Resource Manager]","CreateScheduleTask method","IFsrmReportScheduler.CreateScheduleTask","IFsrmReportScheduler::CreateScheduleTask","fs.ifsrmreportscheduler_createscheduletask","fsrm.ifsrmreportscheduler_createscheduletask","fsrmreports/IFsrmReportScheduler::CreateScheduleTask"]
old-location: fsrm\ifsrmreportscheduler_createscheduletask.htm
tech.root: fsrm
ms.assetid: 983a6d05-417f-4aea-9652-955fd96e78f0
ms.date: 12/05/2018
ms.keywords: CreateScheduleTask, CreateScheduleTask method [File Server Resource Manager], CreateScheduleTask method [File Server Resource Manager],FsrmReportScheduler class, CreateScheduleTask method [File Server Resource Manager],IFsrmReportScheduler interface, FsrmReportScheduler class [File Server Resource Manager],CreateScheduleTask method, IFsrmReportScheduler interface [File Server Resource Manager],CreateScheduleTask method, IFsrmReportScheduler.CreateScheduleTask, IFsrmReportScheduler::CreateScheduleTask, fs.ifsrmreportscheduler_createscheduletask, fsrm.ifsrmreportscheduler_createscheduletask, fsrmreports/IFsrmReportScheduler::CreateScheduleTask
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
 - IFsrmReportScheduler::CreateScheduleTask
 - fsrmreports/IFsrmReportScheduler::CreateScheduleTask
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
 - IFsrmReportScheduler.CreateScheduleTask
 - FsrmReportScheduler.CreateScheduleTask
---

# IFsrmReportScheduler::CreateScheduleTask


## -description

<p class="CCE_Message">[Starting with Windows Server 2012 this method is not supported; use the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmscheduledtask">MSFT_FSRMScheduledTask</a> WMI class to manage 
    scheduled tasks.]

Creates a scheduled task that is used to trigger a report job.

## -parameters

### -param taskName [in]

The name of a <a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a> 
      task to create. The string is limited to 230 characters.

### -param namespacesSafeArray [in]

A <b>VARIANT</b> that contains a <b>SAFEARRAY</b> of local 
      directory paths to verify (see Remarks). Each element of the array is a variant of type 
      <b>VT_BSTR</b>. Use the <b>bstrVal</b> member of the variant to set the 
      path.

### -param serializedTask [in]

An XML string that defines the Task Scheduler job. For details, see 
      <a href="/windows/desktop/TaskSchd/task-scheduler-schema">Task Scheduler Schema</a>.

## -returns

The method returns the following return values.

## -remarks

To run a report job on a schedule, the value of the <i>taskName</i> parameter and the value 
    of the <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportjob-get_task">IFsrmReportJob::Task</a> property must be the 
    same.

Specify the same namespaces for this method that you specified for the 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportjob-get_namespaceroots">IFsrmReportJob::NamespaceRoots</a> property. 
    This method validates the namespace paths. For validation details, see the Remarks section of 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportscheduler-verifynamespaces">VerifyNamespaces</a>.

To generate the XML, you can use the Task Scheduler v2.0 interfaces to define the scheduled task; however, the 
    task definition must be v1.0 compatible. (Use the Task Scheduler API to define the task but not to register the 
    task—this method registers the task.) After defining the task, access the 
    <a href="/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_xmltext">ITaskDefinition::XmlText</a> property to get 
    the XML.

Note that FSRM ignores triggers in the XML that FSRM does not support.  For the "MONTHLYDOW" 
    trigger, you cannot use the V2 extensions. For example,  if you specify "WeeksOfMonth", you can 
    specify only one week of the month and it cannot be the fifth week. Also, for "DaysOfWeek", you 
    can specify only one day.


#### Examples

For an example, see 
     <a href="/previous-versions/windows/desktop/fsrm/scheduling-a-report-job">Scheduling a Report Job</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmreportscheduler">FsrmReportScheduler</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmreportscheduler">IFsrmReportScheduler</a>