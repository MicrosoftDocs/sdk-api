---
UID: NN:rdpencomapi.IRDPSRAPIAttendeeManager
title: IRDPSRAPIAttendeeManager (rdpencomapi.h)
description: Manages attendee objects.
helpviewer_keywords: ["IRDPSRAPIAttendeeManager","IRDPSRAPIAttendeeManager interface [RDP]","IRDPSRAPIAttendeeManager interface [RDP]","described","rdp.irdpsrapiattendeemanager","rdpencomapi/IRDPSRAPIAttendeeManager"]
old-location: rdp\irdpsrapiattendeemanager.htm
tech.root: rdp
ms.assetid: 202b539c-b7a0-4cf3-ba64-f60cc062575a
ms.date: 12/05/2018
ms.keywords: IRDPSRAPIAttendeeManager, IRDPSRAPIAttendeeManager interface [RDP], IRDPSRAPIAttendeeManager interface [RDP],described, rdp.irdpsrapiattendeemanager, rdpencomapi/IRDPSRAPIAttendeeManager
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
 - IRDPSRAPIAttendeeManager
 - rdpencomapi/IRDPSRAPIAttendeeManager
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
 - IRDPSRAPIAttendeeManager
---

# IRDPSRAPIAttendeeManager interface


## -description

Manages attendee objects.

Applications obtain access to this object using <a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapisharingsession-get_attendees">IRDPSRAPISharingSession::get_Attendees</a>.

## -remarks

The lifetime of the objects in this collection is controlled by the network layer.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiattendee">IRDPSRAPIAttendee</a>