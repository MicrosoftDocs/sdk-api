---
UID: NF:rdpencomapi.IRDPSRAPIAttendee.get_Invitation
title: IRDPSRAPIAttendee::get_Invitation
author: windows-sdk-content
description: The invitation used to grant the attendee access to the conference.
old-location: rdp\irdpsrapiattendee_invitation.htm
tech.root: Rdp
ms.assetid: 71fed876-8b9d-4b19-a278-45ab620fb61e
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IRDPSRAPIAttendee interface [RDP],Invitation property, IRDPSRAPIAttendee.Invitation, IRDPSRAPIAttendee.get_Invitation, IRDPSRAPIAttendee::Invitation, IRDPSRAPIAttendee::get_Invitation, Invitation property [RDP], Invitation property [RDP],IRDPSRAPIAttendee interface, Invitation property [RDP],RDPSRAPIAttendee object, RDPSRAPIAttendee object [RDP],Invitation property, get_Invitation, rdp.irdpsrapiattendee_invitation, rdpencomapi/IRDPSRAPIAttendee::Invitation, rdpencomapi/IRDPSRAPIAttendee::get_Invitation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RdpEncomAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: RdpEncomAPI.tlb
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncom.dll
api_name:
 - IRDPSRAPIAttendee.Invitation
 - IRDPSRAPIAttendee.get_Invitation
 - RDPSRAPIAttendee.Invitation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

