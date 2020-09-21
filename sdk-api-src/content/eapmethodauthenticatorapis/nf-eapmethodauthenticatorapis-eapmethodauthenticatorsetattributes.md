---
UID: NF:eapmethodauthenticatorapis.EapMethodAuthenticatorSetAttributes
title: EapMethodAuthenticatorSetAttributes function (eapmethodauthenticatorapis.h)
description: Provides updated EAP authentication attributes to set on the EAP authenticator method.
helpviewer_keywords: ["EapMethodAuthenticatorSetAttributes","EapMethodAuthenticatorSetAttributes function [EAPHost]","eaphost.eapmethodauthenticatorsetattributes","eapmethodauthenticatorapis/EapMethodAuthenticatorSetAttributes"]
old-location: eaphost\eapmethodauthenticatorsetattributes.htm
tech.root: eaphost
ms.assetid: 0cc4df3a-6438-4770-9b13-c9d2a798822c
ms.date: 12/05/2018
ms.keywords: EapMethodAuthenticatorSetAttributes, EapMethodAuthenticatorSetAttributes function [EAPHost], eaphost.eapmethodauthenticatorsetattributes, eapmethodauthenticatorapis/EapMethodAuthenticatorSetAttributes
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
 - EapMethodAuthenticatorSetAttributes
 - eapmethodauthenticatorapis/EapMethodAuthenticatorSetAttributes
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
 - EapMethodAuthenticatorSetAttributes
---

# EapMethodAuthenticatorSetAttributes function


## -description

Provides updated EAP authentication attributes to set on the EAP authenticator method.

<b>EapMethodAuthenticatorSetAttributes</b> is a function prototype.

## -parameters

### -param sessionHandle [in]

A pointer to an <b>EAP_SESSION_HANDLE</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionHandle</i> parameter in a previous call to <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession">EapMethodAuthenticatorBeginSession</a>.

### -param pAttribs [in]

A pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes">EapAttributes</a> structure that contains an array of new EAP authentication response attributes to set for the supplicant on EAPHost.

### -param pEapOutput [out]

A pointer to an <a href="/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action">EAP_METHOD_AUTHENTICATOR_RESPONSE_ACTION</a> enumeration that specifies the suggested action the supplicant should take as a response to the updated attributes.

### -param ppEapError [out]

A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorfreeerrormemory">EapMethodAuthenticatorFreeErrorMemory</a>.

## -remarks

This call is performed by a authenticator-based EAPHost using a function pointer to this API. This API must be implemented on the EAP authenticator method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.

## -see-also

[EAPHost Authenticator Method Functions](/windows/win32/eaphost/eap-host-authenticator-method-functions)



<a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession">EapMethodAuthenticatorBeginSession</a>