---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IFsrmFileManagementJob::AddNotification


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/0c1bafe2-db1a-4325-8ce9-24b22b30a2d4">MSFT_FSRMFMJNotification::CreateFMJNotification</a> 
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

The <a href="https://msdn.microsoft.com/f891679d-3d94-4fbe-99b1-9445666b7694">FromDate</a> determines when the 
    notification window begins. The following properties determine when the file is to expire:

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
<li>
<a href="https://msdn.microsoft.com/6a51dbc2-8e60-4575-9e97-c798e73c02a4">FileNamePattern</a>
</li>
</ul>
To associate an action with the notification value, call the 
    <a href="https://msdn.microsoft.com/d0cb2ac1-842c-4ebb-adac-8298a0e0beed">IFsrmFileManagementJob::CreateNotificationAction</a> 
    method.




## -see-also




<a href="https://msdn.microsoft.com/e9ae697d-4f7c-47d9-8d2a-c46c2e5f838f">IFsrmFileManagementJob</a>



<a href="https://msdn.microsoft.com/d21e289a-5062-4897-9479-3408589db11f">IFsrmFileManagementJob::DeleteNotification</a>



<a href="https://msdn.microsoft.com/f2b26ed7-5bbc-4b34-ae11-7fcdb621a55b">IFsrmFileManagementJob::ModifyNotification</a>



<a href="https://msdn.microsoft.com/f0aee951-12f3-40d0-bbf4-c72af117952f">IFsrmFileManagementJob::Notifications</a>



<a href="https://msdn.microsoft.com/0c1bafe2-db1a-4325-8ce9-24b22b30a2d4">MSFT_FSRMFMJNotification::CreateFMJNotification</a>
 

 

