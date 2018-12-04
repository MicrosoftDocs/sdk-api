---
UID: NN:fsrmreports.IFsrmFileManagementJob
title: IFsrmFileManagementJob
author: windows-sdk-content
description: Defines a file management job.
old-location: fsrm\ifsrmfilemanagementjob.htm
tech.root: fsrm
ms.assetid: e9ae697d-4f7c-47d9-8d2a-c46c2e5f838f
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IFsrmFileManagementJob, IFsrmFileManagementJob interface [File Server Resource Manager], IFsrmFileManagementJob interface [File Server Resource Manager],described, fs.ifsrmfilemanagementjob, fsrm.ifsrmfilemanagementjob, fsrm/IFsrmFileManagementJob
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: fsrmreports.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmFileManagementJob
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmFileManagementJob interface


## -description


<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a> class.]

Defines a file management job. The job specifies a schedule, conditions, a command or 
    actions to execute if a file meets all the conditions, user notifications, and reporting.

To create a file management job, call the 
    <a href="https://msdn.microsoft.com/22ac77f5-264e-482b-aacf-0c1d90dd4dbe">IFsrmFileManagementJobManager::CreateFileManagementJob</a> 
    method.

The following methods return this interface:
<ul>
<li>
<a href="https://msdn.microsoft.com/4af6f794-d9d4-4e03-9cd5-a4d8769888ca">IFsrmFileManagementJobManager::EnumFileManagementJobs</a>
</li>
<li>
<a href="https://msdn.microsoft.com/106c5237-94bc-4556-aa65-247697133810">IFsrmFileManagementJobManager::GetFileManagementJob</a>
</li>
</ul>If a file management job object is modified using 
    <a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a> or a related WMI 
    class, then the methods and properties of the 
    <b>IFsrmFileManagementJob</b> interface may no longer be 
    usable and fail in unexpected ways when working with the same job.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmFileManagementJob</b> interface inherits from <a href="https://msdn.microsoft.com/bb08ea40-6f0e-4ad5-ad57-78f17bbbd4b7">IFsrmObject</a>. <b>IFsrmFileManagementJob</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFsrmFileManagementJob</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95b41aa0-44c9-41a2-8132-6aecc4685243">AddNotification</a>
</td>
<td align="left" width="63%">
Adds a new notification value to the file management job's list of notifications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3abb6673-fdd8-4828-ba7a-7666208dc8f0">Cancel</a>
</td>
<td align="left" width="63%">
Cancels the job if it is running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/886992bd-ca0b-4f21-8036-39703c7c99ba">CreateCustomAction</a>
</td>
<td align="left" width="63%">
Creates a new custom action.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d0cb2ac1-842c-4ebb-adac-8298a0e0beed">CreateNotificationAction</a>
</td>
<td align="left" width="63%">
Creates a notification action of a specific type and associates it with the notification value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b264e9c-4ba0-4de2-acdc-94338519c5af">CreatePropertyCondition</a>
</td>
<td align="left" width="63%">
Creates a new property condition and adds it to the collection of property conditions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d21e289a-5062-4897-9479-3408589db11f">DeleteNotification</a>
</td>
<td align="left" width="63%">
Deletes a notification from the file management job's list of notifications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cfb58db2-39af-434e-95e2-abbd21f4487a">EnumNotificationActions</a>
</td>
<td align="left" width="63%">
Enumerates the actions associated with a notification value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2b26ed7-5bbc-4b34-ae11-7fcdb621a55b">ModifyNotification</a>
</td>
<td align="left" width="63%">
Modifies a notification in the file management job's list of notifications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2db27e05-5c3b-4827-a616-36fd46281911">Run</a>
</td>
<td align="left" width="63%">
Runs the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d0d0046-989f-4d6a-b9da-caf6df44e1db">WaitForCompletion</a>
</td>
<td align="left" width="63%">
Waits for the specified period of time or until the job has finished running.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmFileManagementJob</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/25014b2d-4f08-45bb-a4c4-d8ab72dc53b1">CustomAction</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The action to execute when all the conditions are met and custom action is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f897321f-3e32-4965-b6c0-33d156601481">DaysSinceFileCreated</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The minimum number of days that must elapse from when the file was created to meet the conditions for the 
     job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0892f31d-e2e4-4aeb-9496-f0ff10c2c0af">DaysSinceFileLastAccessed</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The minimum number of days that must elapse from when the file was last accessed to meet the conditions for 
     the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3ee02d60-50c7-4643-9604-b72ca1da01f6">DaysSinceFileLastModified</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The minimum number of days that must elapse from when a file was last modified to meet the conditions for 
     the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c52dab05-34fb-4d9d-ac12-cbcee7e1fb9b">Enabled</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Indicates whether the job is allowed to run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7c8a2584-23ff-4839-b426-8f5411955746">ExpirationDirectory</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The root directory that will contain the expired files.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6a51dbc2-8e60-4575-9e97-c798e73c02a4">FileNamePattern</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
A condition property: wildcard filter for names.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1147829d-c47b-4d80-8b49-4328dd54f8ef">Formats</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The formats of the report to generate when the job is run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f891679d-3d94-4fbe-99b1-9445666b7694">FromDate</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The date from which the file management operation should be executed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f7a7d5fd-b060-41f6-be1f-038ab252259a">LastError</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The error message from the last time the job was run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/404d45e0-621e-47d5-b987-0f9347242653">LastReportPathWithoutExtension</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The path and file name (without extension) of the last report.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/07559b06-4744-466a-a8b0-e907eff7227d">LastRun</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The last time the file management job was run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a1bed6bf-9c34-40ab-b5fc-ba870e1f084a">Logging</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The types of logging to perform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5a6fdb6f-ac95-448c-bbf4-cbcbaf942bd4">MailTo</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The email addresses to which to send the reports, if any.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/48f0b5ad-a986-4d56-a50f-4bb4dfa7a4b8">Name</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The name of the file management job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1f48ac40-eace-49f2-b77d-2456a1a5fa34">NamespaceRoots</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
An array of local directory paths that will be scanned when the file management job is run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f0aee951-12f3-40d0-bbf4-c72af117952f">Notifications</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The list of notifications to perform before the operation is performed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/98816ea0-7651-42ef-8893-13c568ed859a">OperationType</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The type of file management job; the type determines the operation to perform on a file when all conditions 
     are met.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/87eb994c-3d15-4c6b-90c3-1ddb340f7458">Parameters</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The file management job parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/49435c4b-211e-4aae-a6b3-ad40de811526">PropertyConditions</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
A list of property conditions configured for the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/687367c7-5bed-4f42-ade1-f841da484b38">ReportEnabled</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Indicates whether the job will generate a report when it is run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/030efc19-69c0-4321-99ac-ff8abfc38757">RunningStatus</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The running status of the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ca562a21-5b0a-4726-9921-68c6a9fbde6c">Task</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The name of the scheduled task associated with the job.

</td>
</tr>
</table> 


## -remarks



When a file management job runs, it scans the files in the specified folders and if a file in the folder meets 
    the conditions specified by the job, FSRM moves the file to the specified expired files folder if the type is 
    expiration, or runs the custom action if defined. If notifications or actions are specified, FSRM sends the 
    notifications and performs the actions.

Use the following properties to specify the expiration conditions:

<ul>
<li>
<a href="https://msdn.microsoft.com/f897321f-3e32-4965-b6c0-33d156601481">DaysSinceFileCreated</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0892f31d-e2e4-4aeb-9496-f0ff10c2c0af">DaysSinceFileLastAccessed</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3ee02d60-50c7-4643-9604-b72ca1da01f6">DaysSinceFileLastModified</a>
</li>
<li>
<a href="https://msdn.microsoft.com/49435c4b-211e-4aae-a6b3-ad40de811526">PropertyConditions</a> (use 
      the 
      <a href="https://msdn.microsoft.com/1b264e9c-4ba0-4de2-acdc-94338519c5af">CreatePropertyCondition</a> 
      method to create the property condition)</li>
</ul>
FSRM performs a logical AND on all the conditions to determine if the file meets those conditions.

FSRM does not expire files in the system directories (for example, "\Windows", 
    "\System Volume Information", "$Event", and 
    "$Recycle").




## -see-also




<a href="https://msdn.microsoft.com/bbd888d9-1005-4173-8e82-ced13e68c09e">FSRM Interfaces</a>



<a href="https://msdn.microsoft.com/bb08ea40-6f0e-4ad5-ad57-78f17bbbd4b7">IFsrmObject</a>



<a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a>
 

 

