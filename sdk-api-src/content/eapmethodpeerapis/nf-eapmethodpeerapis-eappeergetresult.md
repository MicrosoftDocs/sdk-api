---
UID: NF:eapmethodpeerapis.EapPeerGetResult
title: EapPeerGetResult function (eapmethodpeerapis.h)
description: Obtains the result of an authentication session from the EAP method.
helpviewer_keywords: ["EapPeerGetResult","EapPeerGetResult function [EAPHost]","eaphost.eappeergetresult","eapmethodpeerapis/EapPeerGetResult"]
old-location: eaphost\eappeergetresult.htm
tech.root: eaphost
ms.assetid: fc73cf5f-68c5-403b-8bf1-6befa2c4f5d8
ms.date: 12/05/2018
ms.keywords: EapPeerGetResult, EapPeerGetResult function [EAPHost], eaphost.eappeergetresult, eapmethodpeerapis/EapPeerGetResult
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
 - EapPeerGetResult
 - eapmethodpeerapis/EapPeerGetResult
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
 - EapPeerGetResult
---

# EapPeerGetResult function


## -description

Obtains the result of an authentication session from the EAP method. 

This function is called when a method has completed authentication, or when the lower layer receives an alternative result.

## -parameters

### -param sessionHandle [in]

A pointer to an <b>EAP_SESSION_HANDLE</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionHandle</i> parameter in a previous call to <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession">EapPeerBeginSession</a>.

### -param reason [in]

A <a href="/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresultreason">EapPeerMethodResultReason</a> structure that specifies the reason code for the authentication result returned in <i>ppResult</i>.

### -param ppResult [out]

A pointer to a <a href="/windows/win32/api/eapmethodpeerapis/ns-eapmethodpeerapis-eappeermethodresult">EapPeerMethodResult</a> structure that contains the authentication results.

### -param ppEapError [out]

A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.

## -remarks

This call is performed by a peer-based EAPHost using a function pointer to this API. This API must be implemented on the EAP method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.

## -see-also

[EAPHost Peer Method Run-Time Functions](/windows/win32/eaphost/eaphost-peer-method-run-time-functions)