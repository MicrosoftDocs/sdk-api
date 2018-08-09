---
UID: NN:fsrmreports.IFsrmReportJob
title: IFsrmReportJob
author: windows-sdk-content
description: Used to configure a report job.
old-location: fsrm\ifsrmreportjob.htm
old-project: fsrm
ms.assetid: ea8a3f6b-326b-4c8f-a6fc-7b7525c5543f
ms.author: windowssdkdev
ms.date: 08/01/2018
ms.keywords: IFsrmReportJob, IFsrmReportJob interface [File Server Resource Manager], IFsrmReportJob interface [File Server Resource Manager],described, fs.ifsrmreportjob, fsrm.ifsrmreportjob, fsrm/IFsrmReportJob
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: fsrmreports.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
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
 - IFsrmReportJob
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmReportJob interface


## -description


Used to configure a report job. The job specifies a set of directories that will be scanned 
    to generate one or more different type of reports. The reports help the administrator analyze how the storage is 
    used. The job may also be associated with a scheduled task that will trigger report generation.

To create this interface, call the 
    <a href="https://msdn.microsoft.com/30274108-a820-409e-ba7c-6971b7726b9b">IFsrmReportManager::CreateReportJob</a> 
    method.

The following methods return this interface:
<ul>
<li>
<a href="https://msdn.microsoft.com/af66beb6-e82c-47e6-8658-da9702041053">IFsrmReportManager::EnumReportJobs</a>
</li>
<li>
<a href="https://msdn.microsoft.com/60a1387f-a25f-4026-a582-71981c26dd1b">IFsrmReportManager::GetReportJob</a>
</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmReportJob</b> interface inherits from <a href="https://msdn.microsoft.com/bb08ea40-6f0e-4ad5-ad57-78f17bbbd4b7">IFsrmObject</a>. <b>IFsrmReportJob</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFsrmReportJob</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406716">Cancel</a>
</td>
<td align="left" width="63%">
Cancels the running reports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/484941d1-726c-4765-8652-bcb378f277b4">CreateReport</a>
</td>
<td align="left" width="63%">
Creates a report object of the specified type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a1292084-f1b5-43eb-9b59-fa2f3f99557d">EnumReports</a>
</td>
<td align="left" width="63%">
Enumerates all the reports configured for this report job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff569516">Run</a>
</td>
<td align="left" width="63%">
Runs all the reports in the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/127027a0-7f05-4de4-a3be-8e3c3ec30910">WaitForCompletion</a>
</td>
<td align="left" width="63%">
Waits for the reports in the job to complete.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmReportJob</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9d0f7a7f-ad25-4d44-bc11-67da7685142a">Formats</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves or sets an array of formats which determine the content format of the reports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7a610d10-8e43-49b7-b85b-bb0ec122fda8">LastError</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the error message from the last time the reports were run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b72ce871-41e0-4321-8c9c-0ae77a02c7ff">LastGeneratedInDirectory</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the local directory path where the reports were stored the last time the reports were run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/90acfd1d-9cef-4900-8b67-d44509503809">LastRun</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the time stamp for when the reports were last run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8ec5d65a-9729-4d68-bceb-b07a2f56755e">MailTo</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves or sets the email addresses of those that will receive the reports via email.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/09c767ce-6a81-4c06-93cb-dd1a79d17d97">NamespaceRoots</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves or sets an array of local directory paths that will be scanned when the report job is run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ae87183c-8e82-487c-b774-6b2b802fa645">RunningStatus</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the running status of the report job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2c9ceaca-f696-4506-bc25-efd601522560">Task</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves or sets the name of the report job.

</td>
</tr>
</table> 


## -remarks



To <a href="https://msdn.microsoft.com/library/windows/hardware/hh439717">commit</a> the job, you must specify at least one 
    <a href="https://msdn.microsoft.com/484941d1-726c-4765-8652-bcb378f277b4">report type</a>, at least one 
    <a href="https://msdn.microsoft.com/09c767ce-6a81-4c06-93cb-dd1a79d17d97">namespace root</a>, and the 
    <a href="https://msdn.microsoft.com/2c9ceaca-f696-4506-bc25-efd601522560">task name</a>.

To <a href="https://msdn.microsoft.com/library/windows/hardware/ff569516">run</a> the job, you must specify at least one 
   <a href="https://msdn.microsoft.com/484941d1-726c-4765-8652-bcb378f277b4">report type</a> and 
   <a href="https://msdn.microsoft.com/09c767ce-6a81-4c06-93cb-dd1a79d17d97">namespace root</a>.



