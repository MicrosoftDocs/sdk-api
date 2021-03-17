---
UID: NF:eapmethodpeerapis.EapPeerBeginSession
title: EapPeerBeginSession function (eapmethodpeerapis.h)
description: Starts an EAP authentication session on the peer EAPHost using the EAP method.
helpviewer_keywords: ["EapPeerBeginSession","EapPeerBeginSession function [EAPHost]","eaphost.eappeerbeginsession","eapmethodpeerapis/EapPeerBeginSession"]
old-location: eaphost\eappeerbeginsession.htm
tech.root: eaphost
ms.assetid: 770a548c-c227-4708-bc40-08bf2681c90f
ms.date: 12/05/2018
ms.keywords: EapPeerBeginSession, EapPeerBeginSession function [EAPHost], eaphost.eappeerbeginsession, eapmethodpeerapis/EapPeerBeginSession
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
 - EapPeerBeginSession
 - eapmethodpeerapis/EapPeerBeginSession
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
 - EapPeerBeginSession
---

# EapPeerBeginSession function


## -description

Starts an EAP authentication session on the peer EAPHost using the EAP method.

## -parameters

### -param dwFlags [in]

A combination of [EAP flags](/windows/win32/eaphost/eap-method-flags) that describe the  new EAP authentication session behavior.

### -param pAttributeArray [in]

A pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes">EAP_ATTRIBUTES</a> array structure that specifies the EAP attributes of the entity to authenticate.

### -param hTokenImpersonateUser [in]

Specifies a handle to the user impersonation token to use in this session.

### -param dwSizeofConnectionData [in]

Specifies the size, in bytes, of the connection data buffer provided in <i>pConnectionData</i>.

### -param pConnectionData [in]

Connection data specific to this method used to decide the user data returned from this API, where the user data depends on certain connection data configuration. When this parameter is <b>NULL</b> the method implementation should  use default values for connection.

### -param dwSizeofUserData [in]

Specifies the size in bytes of the user data buffer provided in <i>pUserData</i>.

### -param pUserData [in]

A pointer to a byte buffer that contains the opaque user data BLOB.

### -param dwMaxSendPacketSize [in]

Specifies the maximum size in bytes of an EAP packet sent during the session. If the method needs to
send a packet larger than the maximum size, the method must accommodate fragmentation and reassembly.

### -param pSessionHandle [out]

A pointer to an <b>EAP_SESSION_HANDLE</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server.

### -param ppEapError [out]

A pointer to a pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.

## -remarks

This call is performed by a peer-based EAPHost using a function pointer to this API. This API must be implemented on the EAP method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.

## -see-also

[EAPHost Peer Method Run-Time Functions](/windows/win32/eaphost/eaphost-peer-method-run-time-functions)



<a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerendsession">EapPeerEndSession</a>



[SSO and PLAP](/windows/win32/eaphost/understanding-sso-and-plap)