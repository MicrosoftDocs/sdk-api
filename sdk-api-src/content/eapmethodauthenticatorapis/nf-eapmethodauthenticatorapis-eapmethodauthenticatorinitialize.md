---
UID: NF:eapmethodauthenticatorapis.EapMethodAuthenticatorInitialize
title: EapMethodAuthenticatorInitialize function (eapmethodauthenticatorapis.h)
description: Initializes an EAP authenticator method for the server EAPHost.
helpviewer_keywords: ["EapMethodAuthenticatorInitialize","EapMethodAuthenticatorInitialize function [EAPHost]","eaphost.eapmethodauthenticatorinitialize","eapmethodauthenticatorapis/EapMethodAuthenticatorInitialize"]
old-location: eaphost\eapmethodauthenticatorinitialize.htm
tech.root: eaphost
ms.assetid: 19484962-01fa-4abe-a6b4-c05b8112b0aa
ms.date: 12/05/2018
ms.keywords: EapMethodAuthenticatorInitialize, EapMethodAuthenticatorInitialize function [EAPHost], eaphost.eapmethodauthenticatorinitialize, eapmethodauthenticatorapis/EapMethodAuthenticatorInitialize
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
 - EapMethodAuthenticatorInitialize
 - eapmethodauthenticatorapis/EapMethodAuthenticatorInitialize
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
 - EapMethodAuthenticatorInitialize
---

# EapMethodAuthenticatorInitialize function


## -description

Initializes an EAP authenticator method for the server EAPHost.

<b>EapMethodAuthenticatorInitialize</b> is a function prototype.

## -parameters

### -param pEapType [in]

A pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type">EAP_METHOD_TYPE</a> enumeration that specifies the type of EAP authentication to use for this session.

### -param ppEapError [out]

A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorfreememory">EapMethodAuthenticatorFreeMemory</a>.

## -remarks

This call is performed by a authenticator-based EAPHost using a function pointer to this API. This API must be implemented on the EAP authenticator method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.

## -see-also

[EAPHost Authenticator Method Functions](/windows/win32/eaphost/eap-host-authenticator-method-functions)