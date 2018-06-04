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

# IRDPSRAPIAttendee::get_Invitation


## -description


The invitation used to grant the attendee access to the conference.

This property is read-only.


## -parameters


## -remarks



An application can have multiple groups of attendees. For example, an application can define a "Moderators" group and a "Spectators" group. Attendees that belong to the "Moderators" group are granted interactive control, while attendees in the "Spectators" group are  only granted access to view the session.  The application achieves this  implementation by creating two invitation objects, one for each group. When an attendee connects, the application can verify which group the attendee belongs to by checking the <a href="https://msdn.microsoft.com/7ac76417-bb5c-40ae-a22a-b322b42b0d2c">GroupName</a> property of the invitation object used for authentication.  If the group name is "Spectators," the application sets the <a href="https://msdn.microsoft.com/b154580d-f541-4668-9255-607ab2de46a9">ControlLevel</a> property for the attendee to CTRL_LEVEL_VIEW. If the group name is "Moderators," it sets the <b>ControlLevel</b> property to CTRL_LEVEL_INTERACTIVE.

If this property is accessed on the viewer side, it returns a dummy invitation.




## -see-also




<a href="https://msdn.microsoft.com/e9edd9f2-ccbf-45b2-b71c-e30368435a60">IRDPSRAPIAttendee</a>
 

 

