---
UID: NF:rdpencomapi.IRDPSRAPISharingSession.Open
title: IRDPSRAPISharingSession::Open (rdpencomapi.h)
description: Puts the session in an active state.
helpviewer_keywords: ["IRDPSRAPISharingSession interface [RDP]","Open method","IRDPSRAPISharingSession.Open","IRDPSRAPISharingSession2 interface [RDP]","Open method","IRDPSRAPISharingSession2::Open","IRDPSRAPISharingSession::Open","Open","Open method [RDP]","Open method [RDP]","IRDPSRAPISharingSession interface","Open method [RDP]","IRDPSRAPISharingSession2 interface","rdp.irdpsrapisharingsession_open","rdpencomapi/IRDPSRAPISharingSession2::Open","rdpencomapi/IRDPSRAPISharingSession::Open"]
old-location: rdp\irdpsrapisharingsession_open.htm
tech.root: rdp
ms.assetid: 2c97a37d-5862-4ad3-9029-481ea0a789e0
ms.date: 12/05/2018
ms.keywords: IRDPSRAPISharingSession interface [RDP],Open method, IRDPSRAPISharingSession.Open, IRDPSRAPISharingSession2 interface [RDP],Open method, IRDPSRAPISharingSession2::Open, IRDPSRAPISharingSession::Open, Open, Open method [RDP], Open method [RDP],IRDPSRAPISharingSession interface, Open method [RDP],IRDPSRAPISharingSession2 interface, rdp.irdpsrapisharingsession_open, rdpencomapi/IRDPSRAPISharingSession2::Open, rdpencomapi/IRDPSRAPISharingSession::Open
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
 - IRDPSRAPISharingSession::Open
 - rdpencomapi/IRDPSRAPISharingSession::Open
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
 - IRDPSRAPISharingSession2.Open
 - IRDPSRAPISharingSession.Open
---

# IRDPSRAPISharingSession::Open


## -description

Puts the session in an active state. After this method is called, the listener is started   and incoming connections will be accepted.



## -returns

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code. The following are possible values.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapisharingsession">IRDPSRAPISharingSession</a>



<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapisharingsession2">IRDPSRAPISharingSession2</a>
