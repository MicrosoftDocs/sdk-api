---
UID: NF:eapmethodpeerapis.EapPeerEndSession
title: EapPeerEndSession function (eapmethodpeerapis.h)
description: Ends an EAP authentication session for the EAP method.
helpviewer_keywords: ["EapPeerEndSession","EapPeerEndSession function [EAPHost]","eaphost.eappeerendsession","eapmethodpeerapis/EapPeerEndSession"]
old-location: eaphost\eappeerendsession.htm
tech.root: eaphost
ms.assetid: e4740a71-bf80-41ae-b9c1-91b9769854e7
ms.date: 12/05/2018
ms.keywords: EapPeerEndSession, EapPeerEndSession function [EAPHost], eaphost.eappeerendsession, eapmethodpeerapis/EapPeerEndSession
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
 - EapPeerEndSession
 - eapmethodpeerapis/EapPeerEndSession
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
 - EapPeerEndSession
---

# EapPeerEndSession function


## -description

Ends an EAP authentication session for the EAP method.

## -parameters

### -param sessionHandle [in]

A pointer to an <b>EAP_SESSION_HANDLE</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionHandle</i> parameter in a previous call to <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession">EapPeerBeginSession</a>.

### -param ppEapError [out]

A pointer to a pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.

## -remarks

An authentication session involves a supplicant requesting authentication, and the EAP method that performs the authentication. When a supplicant closes an authentication session with a call to <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession">EapHostPeerEndSession</a>, EAPHost must also close the session for the EAP method that performed the authentication with this API. 

This call is performed by a peer-based EAPHost using a function pointer to this API. This API must be implemented on the EAP method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.

## -see-also

[EAPHost Peer Method Run-Time Functions](/windows/win32/eaphost/eaphost-peer-method-run-time-functions)



<a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection">EapHostPeerClearConnection</a>



<a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession">EapPeerBeginSession</a>