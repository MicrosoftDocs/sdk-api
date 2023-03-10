---
UID: NF:eapmethodpeerapis.EapPeerGetResponsePacket
title: EapPeerGetResponsePacket function (eapmethodpeerapis.h)
description: Obtains a response packet from the EAP method.
helpviewer_keywords: ["EapPeerGetResponsePacket","EapPeerGetResponsePacket function [EAPHost]","eaphost.eappeergetresponsepacket","eapmethodpeerapis/EapPeerGetResponsePacket"]
old-location: eaphost\eappeergetresponsepacket.htm
tech.root: eaphost
ms.assetid: 4e1deaab-53fe-4c8f-9018-d7b148131231
ms.date: 12/05/2018
ms.keywords: EapPeerGetResponsePacket, EapPeerGetResponsePacket function [EAPHost], eaphost.eappeergetresponsepacket, eapmethodpeerapis/EapPeerGetResponsePacket
req.header: eapmethodpeerapis.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EapPeerGetResponsePacket
 - eapmethodpeerapis/EapPeerGetResponsePacket
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - eapmethodpeerapis.h
api_name:
 - EapPeerGetResponsePacket
---

# EapPeerGetResponsePacket function


## -description

Obtains a response packet from the EAP method.

## -parameters

### -param sessionHandle [in]

A pointer to an <b>EAP_SESSION_HANDLE</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionHandle</i> parameter in a previous call to <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession">EapPeerBeginSession</a>.

### -param pcbSendPacket [in, out]

A pointer to a value that contains the size in bytes of the buffer allocated for the response packet. On return, this parameter receives a pointer to the actual size in bytes of <i>pSendPacket</i>.

### -param pSendPacket [out]

A pointer to an <a href="/windows/desktop/api/eapmethodtypes/ns-eapmethodtypes-eappacket">EapPacket</a> structure that contains the response packet.

### -param ppEapError [out]

A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling<a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.

## -remarks

<b>EapPeerGetResponsePacket</b> is called by EAPHost on the EAP method to obtain a response packet. EAPHost only calls this API when the action code from a prior call indicates that a packet is available.

This call is performed by a peer-based EAPHost using a function pointer to this API. This API must be implemented on the EAP method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.

## -see-also

[EAPHost Peer Method Run-Time Functions](/windows/win32/eaphost/eaphost-peer-method-run-time-functions)