---
UID: NF:eapmethodpeerapis.EapPeerGetUIContext
title: EapPeerGetUIContext function (eapmethodpeerapis.h)
description: Obtains the user interface context from the EAP method.
helpviewer_keywords: ["EapPeerGetUIContext","EapPeerGetUIContext function [EAPHost]","eaphost.eappeergetuicontext","eapmethodpeerapis/EapPeerGetUIContext"]
old-location: eaphost\eappeergetuicontext.htm
tech.root: eaphost
ms.assetid: 14bbffde-da24-4632-bd73-2f96dc983117
ms.date: 12/05/2018
ms.keywords: EapPeerGetUIContext, EapPeerGetUIContext function [EAPHost], eaphost.eappeergetuicontext, eapmethodpeerapis/EapPeerGetUIContext
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
 - EapPeerGetUIContext
 - eapmethodpeerapis/EapPeerGetUIContext
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
 - EapPeerGetUIContext
---

# EapPeerGetUIContext function


## -description

Obtains the user interface context from the EAP method. This function is always followed by the <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeinteractiveui">EapPeerInvokeInteractiveUI</a> function, which is followed by the <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetuicontext">EapPeerSetUIContext</a> function.

## -parameters

### -param sessionHandle [in]

A pointer to an <b>EAP_SESSION_HANDLE</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionHandle</i> parameter in a previous call to <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession">EapPeerBeginSession</a>.

### -param pdwSizeOfUIContextData [out]

A pointer to a value that specifies the size of the user interface context data byte buffer returned in <i>ppUIContextData</i>.

### -param ppUIContextData [out]

A pointer to an address that contains a byte buffer with the supplicant user interface context data from EAPHost.

### -param ppEapError [out]

A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.

## -remarks

<b>EapPeerGetUIContext</b> is called by EAPHost when a prior call indicates that a user interface context is available.

This call is performed by a peer-based EAPHost using a function pointer to this API. This API must be implemented on the EAP method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.

## -see-also

[EAPHost Peer Method Run-Time Functions](/windows/win32/eaphost/eaphost-peer-method-run-time-functions)



<a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeinteractiveui">EapPeerInvokeInteractiveUI</a>



<a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetuicontext">EapPeerSetUIContext</a>