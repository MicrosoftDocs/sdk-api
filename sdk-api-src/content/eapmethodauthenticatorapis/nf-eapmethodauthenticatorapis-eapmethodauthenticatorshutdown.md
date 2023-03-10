---
UID: NF:eapmethodauthenticatorapis.EapMethodAuthenticatorShutdown
title: EapMethodAuthenticatorShutdown function (eapmethodauthenticatorapis.h)
description: Shuts down the EAP authenticator method and prepares to unload it from the server EAPHost.
helpviewer_keywords: ["EapMethodAuthenticatorShutdown","EapMethodAuthenticatorShutdown function [EAPHost]","eaphost.eapmethodauthenticatorshutdown","eapmethodauthenticatorapis/EapMethodAuthenticatorShutdown"]
old-location: eaphost\eapmethodauthenticatorshutdown.htm
tech.root: eaphost
ms.assetid: 7b6f883f-f3ea-48d0-b61c-9056316cd232
ms.date: 12/05/2018
ms.keywords: EapMethodAuthenticatorShutdown, EapMethodAuthenticatorShutdown function [EAPHost], eaphost.eapmethodauthenticatorshutdown, eapmethodauthenticatorapis/EapMethodAuthenticatorShutdown
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
 - EapMethodAuthenticatorShutdown
 - eapmethodauthenticatorapis/EapMethodAuthenticatorShutdown
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
 - EapMethodAuthenticatorShutdown
---

# EapMethodAuthenticatorShutdown function


## -description

Shuts down the EAP authenticator method and prepares to unload it from the server EAPHost.

<b>EapMethodAuthenticatorShutdown</b> is a function prototype.

## -parameters

### -param pEapType [in]

A pointer to an  <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type">EAP_METHOD_TYPE</a> enumeration that specifies the type of EAP authentication used in the session.

### -param ppEapError [out]

A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorfreeerrormemory">EapMethodAuthenticatorFreeErrorMemory</a>.

## -remarks

This call is performed by a authenticator-based EAPHost using a function pointer to this API. This API must be implemented on the EAP authenticator method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.

## -see-also

[EAPHost Authenticator Method Functions](/windows/win32/eaphost/eap-host-authenticator-method-functions)