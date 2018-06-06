---
UID: NF:fsrmreports.IFsrmFileManagementJob.put_Task
title: IFsrmFileManagementJob::put_Task
author: windows-sdk-content
description: The name of the scheduled task to associate with the job.
old-location: fsrm\ifsrmfilemanagementjob_task.htm
old-project: Fsrm
ms.assetid: ca562a21-5b0a-4726-9921-68c6a9fbde6c
ms.author: windowssdkdev
ms.date: 04/18/2018
ms.keywords: IFsrmFileManagementJob interface [File Server Resource Manager],Task property, IFsrmFileManagementJob.Task, IFsrmFileManagementJob.put_Task, IFsrmFileManagementJob::Task, IFsrmFileManagementJob::get_Task, IFsrmFileManagementJob::put_Task, Task property [File Server Resource Manager], Task property [File Server Resource Manager],IFsrmFileManagementJob interface, fs.ifsrmfilemanagementjob_task, fsrm.ifsrmfilemanagementjob_task, fsrmreports/IFsrmFileManagementJob::Task, fsrmreports/IFsrmFileManagementJob::get_Task, fsrmreports/IFsrmFileManagementJob::put_Task, put_Task
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: FsrmTemplateApplyOptions
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
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmFileManagementJob::put_Task


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a> class.]

The name of the scheduled task to associate with the job.

This property is read/write.


## -parameters


## -remarks



Typically, the name is the same name that you specify when you call the 
    <a href="https://msdn.microsoft.com/983a6d05-417f-4aea-9652-955fd96e78f0">IFsrmReportScheduler::CreateScheduleTask</a> 
    method to create a scheduled task that runs the job.

The command that you specify for the scheduled job is C:\Windows\System32\Storrept.exe. The 
    arguments that you specify for Storrept.exe are 
    "FileMgmt Run /Scheduled /Task:<i>taskname</i>", where 
    <i>taskname</i> is the value of this property.




## -see-also




<a href="https://msdn.microsoft.com/e9ae697d-4f7c-47d9-8d2a-c46c2e5f838f">IFsrmFileManagementJob</a>



<a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a>
 

 

