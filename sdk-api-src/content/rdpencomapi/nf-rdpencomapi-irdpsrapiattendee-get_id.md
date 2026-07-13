---
UID: NF:rdpencomapi.IRDPSRAPIAttendee.get_Id
title: IRDPSRAPIAttendee::get_Id (rdpencomapi.h)
description: The unique identifier for the attendee.
helpviewer_keywords: ["CONST_ATTENDEE_ID_DEFAULT","IRDPSRAPIAttendee interface [RDP]","Id property","IRDPSRAPIAttendee.Id","IRDPSRAPIAttendee.get_Id","IRDPSRAPIAttendee::Id","IRDPSRAPIAttendee::get_Id","Id property [RDP]","Id property [RDP]","IRDPSRAPIAttendee interface","Id property [RDP]","RDPSRAPIAttendee object","RDPSRAPIAttendee object [RDP]","Id property","get_Id","rdp.irdpsrapiattendee_id","rdpencomapi/IRDPSRAPIAttendee::Id","rdpencomapi/IRDPSRAPIAttendee::get_Id"]
old-location: rdp\irdpsrapiattendee_id.htm
tech.root: rdp
ms.assetid: 9ed04c11-d3cc-4846-88e8-aad9fb23fee8
ms.date: 12/05/2018
ms.keywords: CONST_ATTENDEE_ID_DEFAULT, IRDPSRAPIAttendee interface [RDP],Id property, IRDPSRAPIAttendee.Id, IRDPSRAPIAttendee.get_Id, IRDPSRAPIAttendee::Id, IRDPSRAPIAttendee::get_Id, Id property [RDP], Id property [RDP],IRDPSRAPIAttendee interface, Id property [RDP],RDPSRAPIAttendee object, RDPSRAPIAttendee object [RDP],Id property, get_Id, rdp.irdpsrapiattendee_id, rdpencomapi/IRDPSRAPIAttendee::Id, rdpencomapi/IRDPSRAPIAttendee::get_Id
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
 - IRDPSRAPIAttendee::get_Id
 - rdpencomapi/IRDPSRAPIAttendee::get_Id
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
 - IRDPSRAPIAttendee.Id
 - IRDPSRAPIAttendee.get_Id
 - RDPSRAPIAttendee.Id
---

# IRDPSRAPIAttendee::get_Id


## -description

The unique identifier for the attendee.

This property is read-only.

## -parameters

## -remarks

If an attendee disconnects, the attendee object will be destroyed. If the attendee reconnects, a new object will be created with a new identifier.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiattendee">IRDPSRAPIAttendee</a>



<a href="https://github.com/MicrosoftDocs/sdk-api/blob/docs/sdk-api-src/content/rdpencomapi/ne-rdpencomapi-rdpencomapi_constants.md">RDPENCOMAPI_CONSTANTS</a>