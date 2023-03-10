---
UID: NF:eapmethodpeerapis.EapPeerInvokeIdentityUI
title: EapPeerInvokeIdentityUI function (eapmethodpeerapis.h)
description: Raises a custom interactive user interface dialog to obtain user identity information for the EAP method on the client.
helpviewer_keywords: ["EapPeerInvokeIdentityUI","EapPeerInvokeIdentityUI function [EAPHost]","eaphost.eappeerinvokeidentityui","eapmethodpeerapis/EapPeerInvokeIdentityUI"]
old-location: eaphost\eappeerinvokeidentityui.htm
tech.root: eaphost
ms.assetid: 9b3a525a-2322-496e-83c7-a3180235583a
ms.date: 12/05/2018
ms.keywords: EapPeerInvokeIdentityUI, EapPeerInvokeIdentityUI function [EAPHost], eaphost.eappeerinvokeidentityui, eapmethodpeerapis/EapPeerInvokeIdentityUI
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
 - EapPeerInvokeIdentityUI
 - eapmethodpeerapis/EapPeerInvokeIdentityUI
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
 - EapPeerInvokeIdentityUI
---

# EapPeerInvokeIdentityUI function


## -description

Raises a custom interactive user interface dialog to obtain user identity information for the EAP method on the client.

## -parameters

### -param pEapType [in]

An <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type">EAP_METHOD_TYPE</a> structure that contains vendor and author information about the EAP method used for authenticating the connection.

### -param dwFlags [in]

A combination of [EAP flags](/windows/win32/eaphost/eap-method-flags) that describe the  EAP authentication session behavior.

### -param hwndParent [in]

A handle to the parent window which will spawn the interactive user interface dialog to obtain the identity data.

### -param dwSizeOfConnectionData [in]

The size, in bytes, of the user interface context data specified by <i>pUIContextData</i>.

### -param pConnectionData [in]

A pointer to an opaque byte buffer that contains the connection data.

### -param dwSizeOfUserData [out]

Specifies the size, in bytes, of the user identity data returned in <i>dwSizeOfUserData</i>.

### -param pUserData [in]

A pointer to the user data specific to this authentication used to   pre-populate the user data.
When this API is called for the first time, or when a new authentication session starts, this parameter is <b>NULL</b>.
Otherwise, set this parameter to the <b>pUserData</b> member of the structure pointed to by the <i>ppResult</i> parameter received by <b>EapPeerGetResult</b>.

### -param pdwSizeOfUserDataOut [out]

Specifies the size, in bytes, of the <i>ppUserDataOut</i> buffer.

### -param ppUserDataOut [out]

A pointer to the pointer of the returned user data. The data is passed to <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession">EapPeerBeginSession</a>   as input <i>pUserData</i>.

### -param ppwszIdentity [out]

 A pointer to the returned user identity. The pointer will be included in the identity response packet   and returned to the server.

### -param ppEapError [out]

A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.

## -remarks

This call is performed by a peer-based EAPHost using a function pointer to this API. This API must be implemented on the EAP method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.

## -see-also

[EAPHost Peer Method Configuration Functions](/windows/win32/eaphost/eaphost-peer-method-configuration-functions)



<a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui">EapPeerInvokeIdentityUI</a>