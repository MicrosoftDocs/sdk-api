---
UID: NF:eapmethodpeerapis.EapPeerSetUIContext
title: EapPeerSetUIContext function (eapmethodpeerapis.h)
description: Provides a user interface context to the EAP method. This function is called after the UI has been raised through the EapPeerGetUIContext function.
helpviewer_keywords: ["EapPeerSetUIContext","EapPeerSetUIContext function [EAPHost]","eaphost.eappeersetuicontext","eapmethodpeerapis/EapPeerSetUIContext"]
old-location: eaphost\eappeersetuicontext.htm
tech.root: eaphost
ms.assetid: 90a3844b-5fe9-44ad-981a-0aae643b2390
ms.date: 12/05/2018
ms.keywords: EapPeerSetUIContext, EapPeerSetUIContext function [EAPHost], eaphost.eappeersetuicontext, eapmethodpeerapis/EapPeerSetUIContext
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
 - EapPeerSetUIContext
 - eapmethodpeerapis/EapPeerSetUIContext
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
 - EapPeerSetUIContext
---

# EapPeerSetUIContext function


## -description

Provides a user interface context to the EAP method. This function is called after the UI has been raised through the <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetuicontext">EapPeerGetUIContext</a> function.

## -parameters

### -param sessionHandle [in]

A pointer to an <b>EAP_SESSION_HANDLE</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionHandle</i> parameter in a previous call to <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession">EapPeerBeginSession</a>.

### -param dwSizeOfUIContextData [in]

A pointer to a value that specifies the size of the UI context data byte buffer provided in <i>pUIContextData</i>.

### -param pUIContextData [in]

A pointer to an address that contains a byte buffer with the new supplicant UI context data to set on EAPHost.

### -param pEapOutput [in]

 A pointer to an <a href="/windows/win32/api/eapauthenticatoractiondefine/ns-eapauthenticatoractiondefine-eappeermethodoutput">EapPeerMethodOutput</a> structure that contains the output of the packet process operation.

### -param ppEapError [out]

A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.

## -remarks

This call is performed by a peer-based EAPHost using a function pointer to this API. This API must be implemented on the EAP method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.

## -see-also

[EAPHost Peer Method Run-Time Functions](/windows/win32/eaphost/eaphost-peer-method-run-time-functions)



<a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetuicontext">EapPeerGetUIContext</a>