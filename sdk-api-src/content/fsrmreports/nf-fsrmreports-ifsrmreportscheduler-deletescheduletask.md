---
UID: NF:fsrmreports.IFsrmReportScheduler.DeleteScheduleTask
title: IFsrmReportScheduler::DeleteScheduleTask
author: windows-sdk-content
description: Deletes a task that is used to trigger a report job.
old-location: fsrm\ifsrmreportscheduler_deletescheduletask.htm
tech.root: fsrm
ms.assetid: 31541668-6173-48d4-8650-13e78bc7a763
ms.author: windowssdkdev
ms.date: 09/07/2018
ms.keywords: DeleteScheduleTask, DeleteScheduleTask method [File Server Resource Manager], DeleteScheduleTask method [File Server Resource Manager],FsrmReportScheduler class, DeleteScheduleTask method [File Server Resource Manager],IFsrmReportScheduler interface, FsrmReportScheduler class [File Server Resource Manager],DeleteScheduleTask method, IFsrmReportScheduler interface [File Server Resource Manager],DeleteScheduleTask method, IFsrmReportScheduler.DeleteScheduleTask, IFsrmReportScheduler::DeleteScheduleTask, fs.ifsrmreportscheduler_deletescheduletask, fsrm.ifsrmreportscheduler_deletescheduletask, fsrmreports/IFsrmReportScheduler::DeleteScheduleTask
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IFsrmReportScheduler.DeleteScheduleTask
 - FsrmReportScheduler.DeleteScheduleTask
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmReportScheduler::DeleteScheduleTask


## -description


<p class="CCE_Message">[Starting with Windows Server 2012 this method is not supported; use the 
    <a href="https://msdn.microsoft.com/8ed0ec1c-3af2-4c49-92cf-0911473fb33a">MSFT_FSRMScheduledTask</a> WMI class to manage 
    scheduled tasks.]

Deletes a task that is used to trigger a report job.


## -parameters




### -param taskName [in]

The name of a <a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a> 
      task to delete. The string is limited to 230 characters.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/306f1d7f-6ad4-457a-97be-193aefeccfeb">FsrmReportScheduler</a>



<a href="https://msdn.microsoft.com/f3e71a39-d880-4035-a719-42ace5eeb9e0">IFsrmReportScheduler</a>
 

 

