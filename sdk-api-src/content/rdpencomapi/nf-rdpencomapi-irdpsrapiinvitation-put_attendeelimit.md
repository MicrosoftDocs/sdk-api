---
UID: NF:rdpencomapi.IRDPSRAPIInvitation.put_AttendeeLimit
title: IRDPSRAPIInvitation::put_AttendeeLimit (rdpencomapi.h)
description: The maximum number of attendees that can connect to the session. (Put)
helpviewer_keywords: ["AttendeeLimit property [RDP]","AttendeeLimit property [RDP]","IRDPSRAPIInvitation interface","AttendeeLimit property [RDP]","RDPSRAPIInvitation object","IRDPSRAPIInvitation interface [RDP]","AttendeeLimit property","IRDPSRAPIInvitation.AttendeeLimit","IRDPSRAPIInvitation.put_AttendeeLimit","IRDPSRAPIInvitation::AttendeeLimit","IRDPSRAPIInvitation::get_AttendeeLimit","IRDPSRAPIInvitation::put_AttendeeLimit","RDPSRAPIInvitation object [RDP]","AttendeeLimit property","put_AttendeeLimit","rdp.irdpsrapiinvitation_attendeelimit","rdpencomapi/IRDPSRAPIInvitation::AttendeeLimit","rdpencomapi/IRDPSRAPIInvitation::get_AttendeeLimit","rdpencomapi/IRDPSRAPIInvitation::put_AttendeeLimit"]
old-location: rdp\irdpsrapiinvitation_attendeelimit.htm
tech.root: rdp
ms.assetid: ab16039f-210a-46ba-aaa8-0dcc840123b2
ms.date: 12/05/2018
ms.keywords: AttendeeLimit property [RDP], AttendeeLimit property [RDP],IRDPSRAPIInvitation interface, AttendeeLimit property [RDP],RDPSRAPIInvitation object, IRDPSRAPIInvitation interface [RDP],AttendeeLimit property, IRDPSRAPIInvitation.AttendeeLimit, IRDPSRAPIInvitation.put_AttendeeLimit, IRDPSRAPIInvitation::AttendeeLimit, IRDPSRAPIInvitation::get_AttendeeLimit, IRDPSRAPIInvitation::put_AttendeeLimit, RDPSRAPIInvitation object [RDP],AttendeeLimit property, put_AttendeeLimit, rdp.irdpsrapiinvitation_attendeelimit, rdpencomapi/IRDPSRAPIInvitation::AttendeeLimit, rdpencomapi/IRDPSRAPIInvitation::get_AttendeeLimit, rdpencomapi/IRDPSRAPIInvitation::put_AttendeeLimit
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
 - IRDPSRAPIInvitation::put_AttendeeLimit
 - rdpencomapi/IRDPSRAPIInvitation::put_AttendeeLimit
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
 - IRDPSRAPIInvitation.AttendeeLimit
 - IRDPSRAPIInvitation.get_AttendeeLimit
 - IRDPSRAPIInvitation.put_AttendeeLimit
 - RDPSRAPIInvitation.AttendeeLimit
---

# IRDPSRAPIInvitation::put_AttendeeLimit


## -description

The maximum number of attendees that can connect to the session. When this limit is reached, no additional attendees can connect to a session.

This property is read/write.

## -parameters

## -remarks

The password is set when the invitation is created and can be modified using <b>put_AttendeeLimit</b>.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiinvitation">IRDPSRAPIInvitation</a>
