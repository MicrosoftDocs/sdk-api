---
UID: NF:rdpencomapi.IRDPSRAPISharingSession2.SendControlLevelChangeResponse
title: IRDPSRAPISharingSession2::SendControlLevelChangeResponse (rdpencomapi.h)
description: Sends an OnControlLevelChangeResponse event.
helpviewer_keywords: ["IRDPSRAPISharingSession2 interface [RDP]","SendControlLevelChangeResponse method","IRDPSRAPISharingSession2.SendControlLevelChangeResponse","IRDPSRAPISharingSession2::SendControlLevelChangeResponse","SendControlLevelChangeResponse","SendControlLevelChangeResponse method [RDP]","SendControlLevelChangeResponse method [RDP]","IRDPSRAPISharingSession2 interface","rdp.irdpsrapisharingsession2_sendcontrollevelchangeresponse","rdpencomapi/IRDPSRAPISharingSession2::SendControlLevelChangeResponse"]
old-location: rdp\irdpsrapisharingsession2_sendcontrollevelchangeresponse.htm
tech.root: rdp
ms.assetid: d10c8f2b-b1ee-4966-9e96-21e78124874b
ms.date: 12/05/2018
ms.keywords: IRDPSRAPISharingSession2 interface [RDP],SendControlLevelChangeResponse method, IRDPSRAPISharingSession2.SendControlLevelChangeResponse, IRDPSRAPISharingSession2::SendControlLevelChangeResponse, SendControlLevelChangeResponse, SendControlLevelChangeResponse method [RDP], SendControlLevelChangeResponse method [RDP],IRDPSRAPISharingSession2 interface, rdp.irdpsrapisharingsession2_sendcontrollevelchangeresponse, rdpencomapi/IRDPSRAPISharingSession2::SendControlLevelChangeResponse
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016
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
 - IRDPSRAPISharingSession2::SendControlLevelChangeResponse
 - rdpencomapi/IRDPSRAPISharingSession2::SendControlLevelChangeResponse
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
 - IRDPSRAPISharingSession2.SendControlLevelChangeResponse
---

# IRDPSRAPISharingSession2::SendControlLevelChangeResponse


## -description

Sends an <a href="/previous-versions/windows/desktop/rdp/oncontrollevelchangeresponse">OnControlLevelChangeResponse</a> event.

## -parameters

### -param pAttendee [in]

Attendee that requests control.

### -param RequestedLevel [in]

Level of control requested by the attendee. For possible values, see the <a href="/windows/win32/api/rdpencomapi/ne-rdpencomapi-ctrl_level">CTRL_LEVEL</a> enumeration.

### -param ReasonCode [in]

Specifies the reason for the change.

## -returns

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapisharingsession2">IRDPSRAPISharingSession2</a>