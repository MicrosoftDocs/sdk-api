---
UID: NF:eapmethodpeerapis.EapPeerProcessRequestPacket
title: EapPeerProcessRequestPacket function (eapmethodpeerapis.h)
description: Processes a packet received by EAPHost from a supplicant.
helpviewer_keywords: ["EapPeerProcessRequestPacket","EapPeerProcessRequestPacket function [EAPHost]","eaphost.eappeerprocessrequestpacket","eapmethodpeerapis/EapPeerProcessRequestPacket"]
old-location: eaphost\eappeerprocessrequestpacket.htm
tech.root: eaphost
ms.assetid: 7054b6e5-68df-4d76-9941-99ee00178926
ms.date: 12/05/2018
ms.keywords: EapPeerProcessRequestPacket, EapPeerProcessRequestPacket function [EAPHost], eaphost.eappeerprocessrequestpacket, eapmethodpeerapis/EapPeerProcessRequestPacket
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
 - EapPeerProcessRequestPacket
 - eapmethodpeerapis/EapPeerProcessRequestPacket
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
 - EapPeerProcessRequestPacket
---

# EapPeerProcessRequestPacket function


## -description

Processes a packet received by EAPHost from a supplicant.

## -parameters

### -param sessionHandle [in]

A pointer to an <b>EAP_SESSION_HANDLE</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionHandle</i> parameter in a previous call to <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession">EapPeerBeginSession</a>.

### -param cbReceivedPacket [in]

The size, in bytes, of the request packet specified in <i>pReceivePacket</i>.

### -param pReceivedPacket [in]

A pointer to an <a href="/windows/desktop/api/eapmethodtypes/ns-eapmethodtypes-eappacket">EapPacket</a> structure that contains the request packet to process.

### -param pEapOutput [out]

A pointer to an <a href="/windows/win32/api/eapauthenticatoractiondefine/ns-eapauthenticatoractiondefine-eappeermethodoutput">EapPeerMethodOutput</a> structure that contains the output of the packet process operation.

### -param ppEapError [out]

A pointer to a pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.

## -remarks

This call is performed by a peer-based EAPHost using a function pointer to this API. This API must be implemented on the EAP method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.

## -see-also

[EAPHost Peer Method Run-Time Functions](/windows/win32/eaphost/eaphost-peer-method-run-time-functions)