---
UID: NF:fsrmreports.IFsrmFileManagementJob.AddNotification
title: IFsrmFileManagementJob::AddNotification (fsrmreports.h)
description: Adds a new notification value (period) to the file management job's list of notifications.
helpviewer_keywords: ["AddNotification","AddNotification method [File Server Resource Manager]","AddNotification method [File Server Resource Manager]","IFsrmFileManagementJob interface","IFsrmFileManagementJob interface [File Server Resource Manager]","AddNotification method","IFsrmFileManagementJob.AddNotification","IFsrmFileManagementJob::AddNotification","fs.ifsrmfilemanagementjob_addnotification","fsrm.ifsrmfilemanagementjob_addnotification","fsrmreports/IFsrmFileManagementJob::AddNotification"]
old-location: fsrm\ifsrmfilemanagementjob_addnotification.htm
tech.root: fsrm
ms.assetid: 95b41aa0-44c9-41a2-8132-6aecc4685243
ms.date: 12/05/2018
ms.keywords: AddNotification, AddNotification method [File Server Resource Manager], AddNotification method [File Server Resource Manager],IFsrmFileManagementJob interface, IFsrmFileManagementJob interface [File Server Resource Manager],AddNotification method, IFsrmFileManagementJob.AddNotification, IFsrmFileManagementJob::AddNotification, fs.ifsrmfilemanagementjob_addnotification, fsrm.ifsrmfilemanagementjob_addnotification, fsrmreports/IFsrmFileManagementJob::AddNotification
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
 - IFsrmFileManagementJob::AddNotification
 - fsrmreports/IFsrmFileManagementJob::AddNotification
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
 - IFsrmFileManagementJob.AddNotification
---

# IFsrmFileManagementJob::AddNotification


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjnotification-createfmjnotification">MSFT_FSRMFMJNotification::CreateFMJNotification</a> 
    method.]

Adds a new notification value (period) to the file management job's list of 
    notifications.

## -parameters

### -param days [in]

A unique notification value to add. The value cannot be less than zero.

## -returns

The method returns the following return values.

## -remarks

The <i>days</i> parameter specifies the number of days before the file is to expire. If the 
    appropriate conditions set in the job are met, notification will be sent to the user to let them know that the 
    file is about to expire. FSRM uses the actions associated with the notification value to determine how the user is 
    notified.

Notification occurs when the job runs and the following conditions are met:

<ul>
<li>Today is the day when notification should occur.</li>
<li>The day when notification should occur is before the next scheduled run time.</li>
</ul>
Note that it is possible for the user to receive duplicate notifications. For example, the user can receive 
    duplicate notifications if the job is run manually after the notification is sent but on or before the day when 
    the notification should occur.

The <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_fromdate">FromDate</a> determines when the 
    notification window begins. The following properties determine when the file is to expire:

<ul>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_dayssincefilecreated">DaysSinceFileCreated</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_dayssincefilelastaccessed">DaysSinceFileLastAccessed</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_dayssincefilelastmodified">DaysSinceFileLastModified</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_propertyconditions">PropertyConditions</a> (use 
      the 
      <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-createpropertycondition">CreatePropertyCondition</a> 
      method to create the property condition)</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_filenamepattern">FileNamePattern</a>
</li>
</ul>
To associate an action with the notification value, call the 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-createnotificationaction">IFsrmFileManagementJob::CreateNotificationAction</a> 
    method.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmfilemanagementjob">IFsrmFileManagementJob</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-deletenotification">IFsrmFileManagementJob::DeleteNotification</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-modifynotification">IFsrmFileManagementJob::ModifyNotification</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_notifications">IFsrmFileManagementJob::Notifications</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjnotification-createfmjnotification">MSFT_FSRMFMJNotification::CreateFMJNotification</a>