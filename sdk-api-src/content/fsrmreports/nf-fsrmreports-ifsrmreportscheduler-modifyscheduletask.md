---
UID: NF:fsrmreports.IFsrmReportScheduler.ModifyScheduleTask
title: IFsrmReportScheduler::ModifyScheduleTask (fsrmreports.h)
description: Modifies a task that is used to trigger a report job.
helpviewer_keywords: ["FsrmReportScheduler class [File Server Resource Manager]","ModifyScheduleTask method","IFsrmReportScheduler interface [File Server Resource Manager]","ModifyScheduleTask method","IFsrmReportScheduler.ModifyScheduleTask","IFsrmReportScheduler::ModifyScheduleTask","ModifyScheduleTask","ModifyScheduleTask method [File Server Resource Manager]","ModifyScheduleTask method [File Server Resource Manager]","FsrmReportScheduler class","ModifyScheduleTask method [File Server Resource Manager]","IFsrmReportScheduler interface","fs.ifsrmreportscheduler_modifyscheduletask","fsrm.ifsrmreportscheduler_modifyscheduletask","fsrmreports/IFsrmReportScheduler::ModifyScheduleTask"]
old-location: fsrm\ifsrmreportscheduler_modifyscheduletask.htm
tech.root: fsrm
ms.assetid: ca950e00-d391-4a03-8ff9-2ddef3a17038
ms.date: 12/05/2018
ms.keywords: FsrmReportScheduler class [File Server Resource Manager],ModifyScheduleTask method, IFsrmReportScheduler interface [File Server Resource Manager],ModifyScheduleTask method, IFsrmReportScheduler.ModifyScheduleTask, IFsrmReportScheduler::ModifyScheduleTask, ModifyScheduleTask, ModifyScheduleTask method [File Server Resource Manager], ModifyScheduleTask method [File Server Resource Manager],FsrmReportScheduler class, ModifyScheduleTask method [File Server Resource Manager],IFsrmReportScheduler interface, fs.ifsrmreportscheduler_modifyscheduletask, fsrm.ifsrmreportscheduler_modifyscheduletask, fsrmreports/IFsrmReportScheduler::ModifyScheduleTask
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
 - IFsrmReportScheduler::ModifyScheduleTask
 - fsrmreports/IFsrmReportScheduler::ModifyScheduleTask
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
 - IFsrmReportScheduler.ModifyScheduleTask
 - FsrmReportScheduler.ModifyScheduleTask
---

# IFsrmReportScheduler::ModifyScheduleTask


## -description

<p class="CCE_Message">[Starting with Windows Server 2012 this method is not supported; use the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmscheduledtask">MSFT_FSRMScheduledTask</a> WMI class to manage 
    scheduled tasks.]

Modifies a task that is used to trigger a report job.

## -parameters

### -param taskName [in]

The name of a <a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a> 
      task to modify. The string is limited to 230 characters.

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

Specify the same namespaces for this method that you specified for the 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportjob-get_namespaceroots">IFsrmReportJob::NamespaceRoots</a> property. 
    This method validates the namespace paths. For validation details, see the Remarks section of 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportscheduler-verifynamespaces">IFsrmReportScheduler::VerifyNamespaces</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmreportscheduler">FsrmReportScheduler</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmreportscheduler">IFsrmReportScheduler</a>