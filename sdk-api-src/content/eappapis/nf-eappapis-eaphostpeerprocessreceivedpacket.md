---
UID: NF:eappapis.EapHostPeerProcessReceivedPacket
title: EapHostPeerProcessReceivedPacket function (eappapis.h)
description: Is called by the supplicant every time the supplicant receives a packet that EAPHost needs to process.
helpviewer_keywords: ["EapHostPeerProcessReceivedPacket","EapHostPeerProcessReceivedPacket function [EAPHost]","eaphost.eaphostpeerprocessreceivedpacket","eappapis/EapHostPeerProcessReceivedPacket"]
old-location: eaphost\eaphostpeerprocessreceivedpacket.htm
tech.root: eaphost
ms.assetid: 7b3bc23d-312d-494d-afd0-ce82d2d5136c
ms.date: 12/05/2018
ms.keywords: EapHostPeerProcessReceivedPacket, EapHostPeerProcessReceivedPacket function [EAPHost], eaphost.eaphostpeerprocessreceivedpacket, eappapis/EapHostPeerProcessReceivedPacket
req.header: eappapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Eappprxy.lib
req.dll: Eappprxy.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EapHostPeerProcessReceivedPacket
 - eappapis/EapHostPeerProcessReceivedPacket
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - eappprxy.dll
api_name:
 - EapHostPeerProcessReceivedPacket
---

# EapHostPeerProcessReceivedPacket function


## -description

Is called by the supplicant every time the supplicant receives a packet that EAPHost
   needs to process. <b>EapHostPeerProcessReceivedPacket</b> should be called only after a successful call to
   <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession">EapHostPeerBeginSession</a>.

## -parameters

### -param sessionHandle [in]

A pointer to an <b>EAP_SESSIONID</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionId</i> parameter in a previous call to <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession">EapHostPeerBeginSession</a>. <i>sessionHandle</i> can be zero if the supplicant receives a new identity request not associated with any session.

### -param cbReceivePacket [in]

	The size, in bytes, of the received packet buffer pointed to by the <i>cbReceivePacket</i> parameter.

### -param pReceivePacket [in]

A pointer to a buffer that contains the incoming EAP data received by 
      the supplicant.

### -param pEapOutput [out]

A pointer to an <a href="/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction">EapHostPeerResponseAction</a> value that indicates the supplicant should take appropriate action. Typically the supplicant either calls 
      another method on EAPHost or acts  on its own.

### -param ppEapError [out]

A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure. The address should be set to <b>NULL</b> before calling this function. If error data is available, a pointer to the address of an <b>EAP_ERROR</b> structure that contains any errors raised during the execution of this function call is received. After using the error data, free this memory by calling <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerfreeeaperror">EapHostPeerFreeEapError</a>.

## -see-also

[EAPHost Supplicant Run-time Functions](/windows/win32/eaphost/eap-host-supplicant-run-time-functions)