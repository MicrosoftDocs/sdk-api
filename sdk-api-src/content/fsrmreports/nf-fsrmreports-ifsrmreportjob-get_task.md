---
UID: NF:fsrmreports.IFsrmReportJob.get_Task
title: IFsrmReportJob::get_Task
author: windows-sdk-content
description: Retrieves or sets the name of the report job.
old-location: fsrm\ifsrmreportjob_task.htm
tech.root: Fsrm
ms.assetid: 2c9ceaca-f696-4506-bc25-efd601522560
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IFsrmReportJob interface [File Server Resource Manager],Task property, IFsrmReportJob.Task, IFsrmReportJob.get_Task, IFsrmReportJob::Task, IFsrmReportJob::get_Task, IFsrmReportJob::put_Task, Task property [File Server Resource Manager], Task property [File Server Resource Manager],IFsrmReportJob interface, fs.ifsrmreportjob_task, fsrm.ifsrmreportjob_task, fsrmreports/IFsrmReportJob::Task, fsrmreports/IFsrmReportJob::get_Task, fsrmreports/IFsrmReportJob::put_Task, get_Task
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: fsrmreports.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmReportJob.Task
 - IFsrmReportJob.get_Task
 - IFsrmReportJob.put_Task
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- fsrmreports.h
: 
- IFsrmReportJob.get_Task
: 
---

# IFsrmReportJob::get_Task


## -description


Retrieves or sets the name of the report job.

This property is read/write.


## -parameters


## -remarks



Typically, the name is the same name that you specify when you call the 
    <a href="https://msdn.microsoft.com/983a6d05-417f-4aea-9652-955fd96e78f0">IFsrmReportScheduler::CreateScheduleTask</a> 
    method to create a scheduled task that runs the report job.

Use the task name when calling the 
    <a href="https://msdn.microsoft.com/60a1387f-a25f-4026-a582-71981c26dd1b">IFsrmReportManager::GetReportJob</a> method to 
    retrieve a report job.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/a91c4fe7-ec8c-4d2b-b565-559e16668c87">Defining a Report Job</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/ea8a3f6b-326b-4c8f-a6fc-7b7525c5543f">IFsrmReportJob</a>
 

 

