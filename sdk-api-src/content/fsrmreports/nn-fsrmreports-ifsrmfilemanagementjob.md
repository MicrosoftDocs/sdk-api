---
UID: NN:fsrmreports.IFsrmFileManagementJob
title: IFsrmFileManagementJob (fsrmreports.h)
author: windows-sdk-content
description: Defines a file management job.
old-location: fsrm\ifsrmfilemanagementjob.htm
tech.root: fsrm
ms.assetid: e9ae697d-4f7c-47d9-8d2a-c46c2e5f838f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFsrmFileManagementJob, IFsrmFileManagementJob interface [File Server Resource Manager], IFsrmFileManagementJob interface [File Server Resource Manager],described, fs.ifsrmfilemanagementjob, fsrm.ifsrmfilemanagementjob, fsrm/IFsrmFileManagementJob
ms.topic: interface
f1_keywords: 
 - "fsrmreports/IFsrmFileManagementJob"
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
ms.custom: 19H1
---

# IFsrmFileManagementJob interface


## -description


<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a> class.]

Defines a file management job. The job specifies a schedule, conditions, a command or 
    actions to execute if a file meets all the conditions, user notifications, and reporting.

To create a file management job, call the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjobmanager-createfilemanagementjob">IFsrmFileManagementJobManager::CreateFileManagementJob</a> 
    method.

The following methods return this interface:
<ul>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjobmanager-enumfilemanagementjobs">IFsrmFileManagementJobManager::EnumFileManagementJobs</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjobmanager-getfilemanagementjob">IFsrmFileManagementJobManager::GetFileManagementJob</a>
</li>
</ul>If a file management job object is modified using 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a> or a related WMI 
    class, then the methods and properties of the 
    <b>IFsrmFileManagementJob</b> interface may no longer be 
    usable and fail in unexpected ways when working with the same job.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmFileManagementJob</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmobject">IFsrmObject</a>. <b>IFsrmFileManagementJob</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-addnotification">AddNotification</a>
</td>
<td align="left" width="63%">
Adds a new notification value to the file management job's list of notifications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-cancel">Cancel</a>
</td>
<td align="left" width="63%">
Cancels the job if it is running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-createcustomaction">CreateCustomAction</a>
</td>
<td align="left" width="63%">
Creates a new custom action.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-createnotificationaction">CreateNotificationAction</a>
</td>
<td align="left" width="63%">
Creates a notification action of a specific type and associates it with the notification value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-createpropertycondition">CreatePropertyCondition</a>
</td>
<td align="left" width="63%">
Creates a new property condition and adds it to the collection of property conditions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-deletenotification">DeleteNotification</a>
</td>
<td align="left" width="63%">
Deletes a notification from the file management job's list of notifications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-enumnotificationactions">EnumNotificationActions</a>
</td>
<td align="left" width="63%">
Enumerates the actions associated with a notification value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-modifynotification">ModifyNotification</a>
</td>
<td align="left" width="63%">
Modifies a notification in the file management job's list of notifications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-run">Run</a>
</td>
<td align="left" width="63%">
Runs the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-waitforcompletion">WaitForCompletion</a>
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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_customaction">CustomAction</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_dayssincefilecreated">DaysSinceFileCreated</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_dayssincefilelastaccessed">DaysSinceFileLastAccessed</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_dayssincefilelastmodified">DaysSinceFileLastModified</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_enabled">Enabled</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_expirationdirectory">ExpirationDirectory</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_filenamepattern">FileNamePattern</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_formats">Formats</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_fromdate">FromDate</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_lasterror">LastError</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_lastreportpathwithoutextension">LastReportPathWithoutExtension</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_lastrun">LastRun</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_logging">Logging</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_mailto">MailTo</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_name">Name</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_namespaceroots">NamespaceRoots</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_notifications">Notifications</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_operationtype">OperationType</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_parameters">Parameters</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_propertyconditions">PropertyConditions</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_reportenabled">ReportEnabled</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_runningstatus">RunningStatus</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_task">Task</a>


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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_dayssincefilecreated">DaysSinceFileCreated</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_dayssincefilelastaccessed">DaysSinceFileLastAccessed</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_dayssincefilelastmodified">DaysSinceFileLastModified</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_propertyconditions">PropertyConditions</a> (use 
      the 
      <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-createpropertycondition">CreatePropertyCondition</a> 
      method to create the property condition)</li>
</ul>
FSRM performs a logical AND on all the conditions to determine if the file meets those conditions.

FSRM does not expire files in the system directories (for example, "\Windows", 
    "\System Volume Information", "$Event", and 
    "$Recycle").




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmobject">IFsrmObject</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a>
 

 

