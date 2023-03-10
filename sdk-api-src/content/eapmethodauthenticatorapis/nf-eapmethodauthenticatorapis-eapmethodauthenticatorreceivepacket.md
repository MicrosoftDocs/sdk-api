---
UID: NF:eapmethodauthenticatorapis.EapMethodAuthenticatorReceivePacket
title: EapMethodAuthenticatorReceivePacket function (eapmethodauthenticatorapis.h)
description: Processes an EAP authentication packet received by the server EAPHost and returns a response action.
helpviewer_keywords: ["EapMethodAuthenticatorReceivePacket","EapMethodAuthenticatorReceivePacket function [EAPHost]","eaphost.eapmethodauthenticatorreceivepacket","eapmethodauthenticatorapis/EapMethodAuthenticatorReceivePacket"]
old-location: eaphost\eapmethodauthenticatorreceivepacket.htm
tech.root: eaphost
ms.assetid: 93505c06-fc77-44e6-8ca2-e52ee67ca267
ms.date: 12/05/2018
ms.keywords: EapMethodAuthenticatorReceivePacket, EapMethodAuthenticatorReceivePacket function [EAPHost], eaphost.eapmethodauthenticatorreceivepacket, eapmethodauthenticatorapis/EapMethodAuthenticatorReceivePacket
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
 - EapMethodAuthenticatorReceivePacket
 - eapmethodauthenticatorapis/EapMethodAuthenticatorReceivePacket
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
 - EapMethodAuthenticatorReceivePacket
---

# EapMethodAuthenticatorReceivePacket function


## -description

Processes an EAP authentication packet received by the server EAPHost and returns a response action.

<b>EapMethodAuthenticatorReceivePacket</b> is a function prototype.

## -parameters

### -param sessionHandle [in]

A pointer to an <b>EAP_SESSION_HANDLE</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionHandle</i> parameter in a previous call to <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession">EapMethodAuthenticatorBeginSession</a>.

### -param cbReceivePacket [in]

The size, in bytes, of <i>pReceivePacket</i>.

### -param pReceivePacket [in]

A pointer to an <a href="/windows/desktop/api/eapmethodtypes/ns-eapmethodtypes-eappacket">EapPacket</a> structure that contains an EAP authentication session packet received from the supplicant by the server EAPHost.

### -param pEapOutput [out]

A pointer to an <a href="/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action">EAP_METHOD_AUTHENTICATOR_RESPONSE_ACTION</a> enumeration that indicates the next action the supplicant must take in the EAP authentication session.

### -param ppEapError [out]

A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorfreeerrormemory">EapMethodAuthenticatorFreeErrorMemory</a>.

## -remarks

This call is performed by a authenticator-based EAPHost using a function pointer to this API. This API must be implemented on the EAP authenticator method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.

## -see-also

[EAPHost Authenticator Method Functions](/windows/win32/eaphost/eap-host-authenticator-method-functions)



<a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession">EapMethodAuthenticatorBeginSession</a>