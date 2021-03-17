---
UID: NF:eapmethodpeerapis.EapPeerInvokeInteractiveUI
title: EapPeerInvokeInteractiveUI function (eapmethodpeerapis.h)
description: Raises a custom interactive user interface dialog for the EAP method on the client.
helpviewer_keywords: ["EapPeerInvokeInteractiveUI","EapPeerInvokeInteractiveUI function [EAPHost]","eaphost.eappeerinvokeinteractiveui","eapmethodpeerapis/EapPeerInvokeInteractiveUI"]
old-location: eaphost\eappeerinvokeinteractiveui.htm
tech.root: eaphost
ms.assetid: 16301c49-4415-4ebe-abdd-a03183db5f20
ms.date: 12/05/2018
ms.keywords: EapPeerInvokeInteractiveUI, EapPeerInvokeInteractiveUI function [EAPHost], eaphost.eappeerinvokeinteractiveui, eapmethodpeerapis/EapPeerInvokeInteractiveUI
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
 - EapPeerInvokeInteractiveUI
 - eapmethodpeerapis/EapPeerInvokeInteractiveUI
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - eapmethodpeerapis.h
api_name:
 - EapPeerInvokeInteractiveUI
---

# EapPeerInvokeInteractiveUI function


## -description

Raises a custom interactive user interface dialog for the EAP method on the client.

## -parameters

### -param pEapType [in]

An <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type">EAP_METHOD_TYPE</a> structure that contains vendor and author information about the EAP method used for authenticating the connection.

### -param hwndParent [in]

A handle to the parent window which will spawn the interactive user interface dialog.

### -param dwSizeofUIContextData [in]

The size, in bytes, of the user interface context data specified by <i>pUIContextData</i>.

### -param pUIContextData [in]

 A pointer to an opaque byte buffer that contains the context data used to create the user interface dialog.

### -param pdwSizeOfDataFromInteractiveUI [out]

A pointer to the size, in bytes, of the data returned in <i>ppDataFromInteractiveUI</i>.

### -param ppDataFromInteractiveUI [out]

A pointer to the address of an opaque byte buffer that contains data obtained from the interactive user interface dialog.

### -param ppEapError [out]

A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling<a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.

## -remarks

This API is used when EAPHost must obtain specific data from the user to continue.

This call is performed by a peer-based EAPHost using a function pointer to this API. This API must be implemented on the EAP method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.

## -see-also

[EAPHost Peer Method Configuration Functions](/windows/win32/eaphost/eaphost-peer-method-configuration-functions)