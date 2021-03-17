---
UID: NF:eapmethodauthenticatorapis.EapMethodAuthenticatorBeginSession
title: EapMethodAuthenticatorBeginSession function (eapmethodauthenticatorapis.h)
description: Creates a new EAP authentication session on the server EAPHost.
helpviewer_keywords: ["EapMethodAuthenticatorBeginSession","EapMethodAuthenticatorBeginSession function [EAPHost]","eaphost.eapmethodauthenticatorbeginsession","eapmethodauthenticatorapis/EapMethodAuthenticatorBeginSession"]
old-location: eaphost\eapmethodauthenticatorbeginsession.htm
tech.root: eaphost
ms.assetid: 02364783-71e4-4af0-95a2-a4ade7e17521
ms.date: 12/05/2018
ms.keywords: EapMethodAuthenticatorBeginSession, EapMethodAuthenticatorBeginSession function [EAPHost], eaphost.eapmethodauthenticatorbeginsession, eapmethodauthenticatorapis/EapMethodAuthenticatorBeginSession
req.header: eapmethodauthenticatorapis.h
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
 - EapMethodAuthenticatorBeginSession
 - eapmethodauthenticatorapis/EapMethodAuthenticatorBeginSession
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - eapmethodauthenticatorapis.h
api_name:
 - EapMethodAuthenticatorBeginSession
---

# EapMethodAuthenticatorBeginSession function


## -description

Creates a new EAP authentication session on the server EAPHost.

<b>EapMethodAuthenticatorBeginSession</b> is a function prototype.

## -parameters

### -param dwFlags [in]

A combination of [EAP flags](/windows/win32/eaphost/eap-method-flags) that describe the  EAP authentication session behavior.

### -param bInitialId [in]

A zero-terminated Unicode string that contains the identity of the user to authenticate.

### -param pwszIdentity

Identity of the user being authenticated.

### -param pAttributeArray [in]

A pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes">EapAttributes</a> array structure that specifies the EAP attributes of the entity to authenticate.

### -param dwSizeofConnectionData [in]

Specifies the size in bytes of the data pointed to by *pConnectionData*. If *pConnectionData* is NULL, this member is zero.

### -param pConnectionData

Pointer to connection data received from the authentication protocol's configuration user interface.

### -param dwMaxSendPacketSize [in]

Specifies the maximum size, in bytes, of an EAP packet sent during the session.

### -param pSessionHandle [out]

A pointer to an <b>EAP_SESSION_HANDLE</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server.

### -param ppEapError [out]

Optionally receives a pointer to a pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorfreememory">EapMethodAuthenticatorFreeMemory</a>.

## -remarks

This call is performed by a authenticator-based EAPHost using a function pointer to this API. This API must be implemented on the EAP authenticator method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.

## -see-also

[EAPHost Authenticator Method Functions](/windows/win32/eaphost/eap-host-authenticator-method-functions)



<a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession">EapHostPeerBeginSession</a>