---
UID: NF:fsrmreports.IFsrmReportScheduler.CreateScheduleTask
title: IFsrmReportScheduler::CreateScheduleTask
author: windows-sdk-content
description: Creates a scheduled task that is used to trigger a report job.
old-location: fsrm\ifsrmreportscheduler_createscheduletask.htm
old-project: Fsrm
ms.assetid: 983a6d05-417f-4aea-9652-955fd96e78f0
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: CreateScheduleTask, CreateScheduleTask method [File Server Resource Manager], CreateScheduleTask method [File Server Resource Manager],FsrmReportScheduler class, CreateScheduleTask method [File Server Resource Manager],IFsrmReportScheduler interface, FsrmReportScheduler class [File Server Resource Manager],CreateScheduleTask method, IFsrmReportScheduler interface [File Server Resource Manager],CreateScheduleTask method, IFsrmReportScheduler.CreateScheduleTask, IFsrmReportScheduler::CreateScheduleTask, fs.ifsrmreportscheduler_createscheduletask, fsrm.ifsrmreportscheduler_createscheduletask, fsrmreports/IFsrmReportScheduler::CreateScheduleTask
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
 - IFsrmReportScheduler.CreateScheduleTask
 - FsrmReportScheduler.CreateScheduleTask
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmReportScheduler::CreateScheduleTask


## -description


<p class="CCE_Message">[Starting with Windows Server 2012 this method is not supported; use the 
    <a href="https://msdn.microsoft.com/8ed0ec1c-3af2-4c49-92cf-0911473fb33a">MSFT_FSRMScheduledTask</a> WMI class to manage 
    scheduled tasks.]

Creates a scheduled task that is used to trigger a report job.


## -parameters




### -param taskName [in]

The name of a <a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a> 
      task to create. The string is limited to 230 characters.


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



To run a report job on a schedule, the value of the <i>taskName</i> parameter and the value 
    of the <a href="https://msdn.microsoft.com/2c9ceaca-f696-4506-bc25-efd601522560">IFsrmReportJob::Task</a> property must be the 
    same.

Specify the same namespaces for this method that you specified for the 
    <a href="https://msdn.microsoft.com/09c767ce-6a81-4c06-93cb-dd1a79d17d97">IFsrmReportJob::NamespaceRoots</a> property. 
    This method validates the namespace paths. For validation details, see the Remarks section of 
    <a href="https://msdn.microsoft.com/bb5139c8-e01f-48cf-a8a9-d3a3e5b86238">VerifyNamespaces</a>.

To generate the XML, you can use the Task Scheduler v2.0 interfaces to define the scheduled task; however, the 
    task definition must be v1.0 compatible. (Use the Task Scheduler API to define the task but not to register the 
    task—this method registers the task.) After defining the task, access the 
    <a href="https://msdn.microsoft.com/1bdafec0-634f-4977-8f41-60dcacc23dec">ITaskDefinition::XmlText</a> property to get 
    the XML.

Note that FSRM ignores triggers in the XML that FSRM does not support.  For the "MONTHLYDOW" 
    trigger, you cannot use the V2 extensions. For example,  if you specify "WeeksOfMonth", you can 
    specify only one week of the month and it cannot be the fifth week. Also, for "DaysOfWeek", you 
    can specify only one day.


#### Examples

For an example, see 
     <a href="https://msdn.microsoft.com/7994bf40-cc9d-4519-a0d4-d48d7ec10fda">Scheduling a Report Job</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/306f1d7f-6ad4-457a-97be-193aefeccfeb">FsrmReportScheduler</a>



<a href="https://msdn.microsoft.com/f3e71a39-d880-4035-a719-42ace5eeb9e0">IFsrmReportScheduler</a>
 

 

