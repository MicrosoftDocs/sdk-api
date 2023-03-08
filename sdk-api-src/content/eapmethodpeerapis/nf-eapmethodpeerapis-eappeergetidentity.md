---
UID: NF:eapmethodpeerapis.EapPeerGetIdentity
title: EapPeerGetIdentity function (eapmethodpeerapis.h)
description: Returns the user data and user identity after being called by EAPHost.
helpviewer_keywords: ["EapPeerGetIdentity","EapPeerGetIdentity function [EAPHost]","eaphost.eappeergetidentity","eapmethodpeerapis/EapPeerGetIdentity"]
old-location: eaphost\eappeergetidentity.htm
tech.root: eaphost
ms.assetid: 24ae093f-5ddf-4b09-934f-d0e945335cde
ms.date: 12/05/2018
ms.keywords: EapPeerGetIdentity, EapPeerGetIdentity function [EAPHost], eaphost.eappeergetidentity, eapmethodpeerapis/EapPeerGetIdentity
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
 - EapPeerGetIdentity
 - eapmethodpeerapis/EapPeerGetIdentity
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
 - EapPeerGetIdentity
---

# EapPeerGetIdentity function


## -description

Returns the user data and user identity after being called by EAPHost.

## -parameters

### -param dwFlags [in]

A combination of [EAP flags](/windows/win32/eaphost/eap-method-flags) that describe the  EAP authentication session behavior.

### -param dwSizeofConnectionData [in]

Specifies the size, in bytes, of the connection data buffer provided in <i>pConnectionData</i>

### -param pConnectionData [in]

A pointer to a byte buffer that contains the opaque configuration data BLOB.

### -param dwSizeofUserData [in]

Specifies the size, in bytes, of the user data buffer provided in <i>pUserData</i>.

### -param pUserData [in]

A pointer to the user data specific to this authentication used to   pre-populate the user data.
When this API is called for the first time, or when a new authentication session starts, this parameter is <b>NULL</b>.
Otherwise, set this parameter to the <b>pUserData</b> member of the structure pointed to by the <i>ppResult</i> parameter received by <b>EapPeerGetResult</b>.

### -param hTokenImpersonateUser [in]

Specifies a handle to the impersonation token of the user being authenticated. This handle will be <b>NULL</b> when doing machine authentication. By using this handle an EAP method can impersonate the user for the purpose of obtaining user specific information such as user name, domain name and credentials.

### -param pfInvokeUI [out]

Returns <b>TRUE</b> if the user identity and user data blob aren't returned successfully, and the method seeks to collect the information from the user through the user interface dialog.

### -param pdwSizeOfUserDataOut [in, out]

Specifies the size, in bytes, of the <i>ppUserDataOut</i> buffer.

### -param ppUserDataOut [out]

A pointer to a pointer to the returned user data. The data is passed to <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession">EapPeerBeginSession</a>   as input <i>pUserData</i>.

### -param ppwszIdentity [out]

 A pointer to the returned user identity. The pointer will be included in the identity response packet   and returned to the server.

### -param ppEapError [out]

A pointer to the pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.

## -remarks

This call is performed by a peer-based EAPHost using a function pointer to this API. This API must be implemented on the EAP method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.

## -see-also

[EAPHost Peer Method Run-Time Functions](/windows/win32/eaphost/eaphost-peer-method-run-time-functions)



<a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui">EapPeerInvokeIdentityUI</a>