---
UID: NF:rdpencomapi.IRDPSRAPIAttendee.get_Invitation
title: IRDPSRAPIAttendee::get_Invitation (rdpencomapi.h)
description: The invitation used to grant the attendee access to the conference.
helpviewer_keywords: ["IRDPSRAPIAttendee interface [RDP]","Invitation property","IRDPSRAPIAttendee.Invitation","IRDPSRAPIAttendee.get_Invitation","IRDPSRAPIAttendee::Invitation","IRDPSRAPIAttendee::get_Invitation","Invitation property [RDP]","Invitation property [RDP]","IRDPSRAPIAttendee interface","Invitation property [RDP]","RDPSRAPIAttendee object","RDPSRAPIAttendee object [RDP]","Invitation property","get_Invitation","rdp.irdpsrapiattendee_invitation","rdpencomapi/IRDPSRAPIAttendee::Invitation","rdpencomapi/IRDPSRAPIAttendee::get_Invitation"]
old-location: rdp\irdpsrapiattendee_invitation.htm
tech.root: rdp
ms.assetid: 71fed876-8b9d-4b19-a278-45ab620fb61e
ms.date: 12/05/2018
ms.keywords: IRDPSRAPIAttendee interface [RDP],Invitation property, IRDPSRAPIAttendee.Invitation, IRDPSRAPIAttendee.get_Invitation, IRDPSRAPIAttendee::Invitation, IRDPSRAPIAttendee::get_Invitation, Invitation property [RDP], Invitation property [RDP],IRDPSRAPIAttendee interface, Invitation property [RDP],RDPSRAPIAttendee object, RDPSRAPIAttendee object [RDP],Invitation property, get_Invitation, rdp.irdpsrapiattendee_invitation, rdpencomapi/IRDPSRAPIAttendee::Invitation, rdpencomapi/IRDPSRAPIAttendee::get_Invitation
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRDPSRAPIAttendee::get_Invitation
 - rdpencomapi/IRDPSRAPIAttendee::get_Invitation
dev_langs:
 - c++
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
---

# IRDPSRAPIAttendee::get_Invitation


## -description

The invitation used to grant the attendee access to the conference.

This property is read-only.

## -parameters

## -remarks

An application can have multiple groups of attendees. For example, an application can define a "Moderators" group and a "Spectators" group. Attendees that belong to the "Moderators" group are granted interactive control, while attendees in the "Spectators" group are  only granted access to view the session.  The application achieves this  implementation by creating two invitation objects, one for each group. When an attendee connects, the application can verify which group the attendee belongs to by checking the <a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiinvitation-get_groupname">GroupName</a> property of the invitation object used for authentication.  If the group name is "Spectators," the application sets the <a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiattendee-get_controllevel">ControlLevel</a> property for the attendee to CTRL_LEVEL_VIEW. If the group name is "Moderators," it sets the <b>ControlLevel</b> property to CTRL_LEVEL_INTERACTIVE.

If this property is accessed on the viewer side, it returns a dummy invitation.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiattendee">IRDPSRAPIAttendee</a>