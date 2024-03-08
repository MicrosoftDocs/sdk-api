---
UID: NF:fsrmreports.IFsrmFileManagementJob.get_Task
title: IFsrmFileManagementJob::get_Task (fsrmreports.h)
description: The name of the scheduled task to associate with the job. (Get)
helpviewer_keywords: ["IFsrmFileManagementJob interface [File Server Resource Manager]","Task property","IFsrmFileManagementJob.Task","IFsrmFileManagementJob.get_Task","IFsrmFileManagementJob::Task","IFsrmFileManagementJob::get_Task","IFsrmFileManagementJob::put_Task","Task property [File Server Resource Manager]","Task property [File Server Resource Manager]","IFsrmFileManagementJob interface","fs.ifsrmfilemanagementjob_task","fsrm.ifsrmfilemanagementjob_task","fsrmreports/IFsrmFileManagementJob::Task","fsrmreports/IFsrmFileManagementJob::get_Task","fsrmreports/IFsrmFileManagementJob::put_Task","get_Task"]
old-location: fsrm\ifsrmfilemanagementjob_task.htm
tech.root: fsrm
ms.assetid: ca562a21-5b0a-4726-9921-68c6a9fbde6c
ms.date: 12/05/2018
ms.keywords: IFsrmFileManagementJob interface [File Server Resource Manager],Task property, IFsrmFileManagementJob.Task, IFsrmFileManagementJob.get_Task, IFsrmFileManagementJob::Task, IFsrmFileManagementJob::get_Task, IFsrmFileManagementJob::put_Task, Task property [File Server Resource Manager], Task property [File Server Resource Manager],IFsrmFileManagementJob interface, fs.ifsrmfilemanagementjob_task, fsrm.ifsrmfilemanagementjob_task, fsrmreports/IFsrmFileManagementJob::Task, fsrmreports/IFsrmFileManagementJob::get_Task, fsrmreports/IFsrmFileManagementJob::put_Task, get_Task
req.header: fsrmreports.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IFsrmFileManagementJob::get_Task
 - fsrmreports/IFsrmFileManagementJob::get_Task
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
 - IFsrmFileManagementJob.Task
 - IFsrmFileManagementJob.get_Task
 - IFsrmFileManagementJob.put_Task
---

# IFsrmFileManagementJob::get_Task


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a> class.]

The name of the scheduled task to associate with the job.

This property is read/write.

## -parameters

## -remarks

Typically, the name is the same name that you specify when you call the 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportscheduler-createscheduletask">IFsrmReportScheduler::CreateScheduleTask</a> 
    method to create a scheduled task that runs the job.

The command that you specify for the scheduled job is C:\Windows\System32\Storrept.exe. The 
    arguments that you specify for Storrept.exe are 
    "FileMgmt Run /Scheduled /Task:<i>taskname</i>", where 
    <i>taskname</i> is the value of this property.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmfilemanagementjob">IFsrmFileManagementJob</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a>
