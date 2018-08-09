---
UID: NF:fsrmreports.IFsrmReportScheduler.ModifyScheduleTask
title: IFsrmReportScheduler::ModifyScheduleTask
author: windows-sdk-content
description: Modifies a task that is used to trigger a report job.
old-location: fsrm\ifsrmreportscheduler_modifyscheduletask.htm
old-project: fsrm
ms.assetid: ca950e00-d391-4a03-8ff9-2ddef3a17038
ms.author: windowssdkdev
ms.date: 08/01/2018
ms.keywords: FsrmReportScheduler class [File Server Resource Manager],ModifyScheduleTask method, IFsrmReportScheduler interface [File Server Resource Manager],ModifyScheduleTask method, IFsrmReportScheduler.ModifyScheduleTask, IFsrmReportScheduler::ModifyScheduleTask, ModifyScheduleTask, ModifyScheduleTask method [File Server Resource Manager], ModifyScheduleTask method [File Server Resource Manager],FsrmReportScheduler class, ModifyScheduleTask method [File Server Resource Manager],IFsrmReportScheduler interface, fs.ifsrmreportscheduler_modifyscheduletask, fsrm.ifsrmreportscheduler_modifyscheduletask, fsrmreports/IFsrmReportScheduler::ModifyScheduleTask
ms.prod: windows
ms.technology: windows-sdk
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
 - IFsrmReportScheduler.ModifyScheduleTask
 - FsrmReportScheduler.ModifyScheduleTask
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmReportScheduler::ModifyScheduleTask


## -description


<p class="CCE_Message">[Starting with Windows Server 2012 this method is not supported; use the 
    <a href="https://msdn.microsoft.com/8ed0ec1c-3af2-4c49-92cf-0911473fb33a">MSFT_FSRMScheduledTask</a> WMI class to manage 
    scheduled tasks.]

Modifies a task that is used to trigger a report job.


## -parameters




### -param taskName [in]

The name of a <a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a> 
      task to modify. The string is limited to 230 characters.


### -param namespacesSafeArray [in]

A <b>VARIANT</b> that contains a <b>SAFEARRAY</b> of local 
      directory paths to verify (see Remarks). Each element of the array is a variant of type 
      <b>VT_BSTR</b>. Use the <b>bstrVal</b> member of the variant to set the 
      path.


### -param serializedTask [in]

An XML string that defines the Task Scheduler job. For details, see 
      <a href="https://msdn.microsoft.com/9b1b8e34-c635-413a-a230-79a58017cf21">Task Scheduler Schema</a>.


## -returns



The method returns the following return values.




## -remarks



Specify the same namespaces for this method that you specified for the 
    <a href="https://msdn.microsoft.com/09c767ce-6a81-4c06-93cb-dd1a79d17d97">IFsrmReportJob::NamespaceRoots</a> property. 
    This method validates the namespace paths. For validation details, see the Remarks section of 
    <a href="https://msdn.microsoft.com/bb5139c8-e01f-48cf-a8a9-d3a3e5b86238">IFsrmReportScheduler::VerifyNamespaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/306f1d7f-6ad4-457a-97be-193aefeccfeb">FsrmReportScheduler</a>



<a href="https://msdn.microsoft.com/f3e71a39-d880-4035-a719-42ace5eeb9e0">IFsrmReportScheduler</a>
 

 

