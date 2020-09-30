---
UID: NF:eapmethodauthenticatorapis.EapMethodAuthenticatorFreeErrorMemory
title: EapMethodAuthenticatorFreeErrorMemory function (eapmethodauthenticatorapis.h)
description: Releases error-specific memory allocated by the EAP authenticator method.
helpviewer_keywords: ["EapMethodAuthenticatorFreeErrorMemory","EapMethodAuthenticatorFreeErrorMemory function [EAPHost]","eaphost.eapmethodauthenticatorfreeerrormemory","eapmethodauthenticatorapis/EapMethodAuthenticatorFreeErrorMemory"]
old-location: eaphost\eapmethodauthenticatorfreeerrormemory.htm
tech.root: eaphost
ms.assetid: 8fcf82d6-9809-4a28-a694-1f7494216f82
ms.date: 12/05/2018
ms.keywords: EapMethodAuthenticatorFreeErrorMemory, EapMethodAuthenticatorFreeErrorMemory function [EAPHost], eaphost.eapmethodauthenticatorfreeerrormemory, eapmethodauthenticatorapis/EapMethodAuthenticatorFreeErrorMemory
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
 - EapMethodAuthenticatorFreeErrorMemory
 - eapmethodauthenticatorapis/EapMethodAuthenticatorFreeErrorMemory
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
 - EapMethodAuthenticatorFreeErrorMemory
---

# EapMethodAuthenticatorFreeErrorMemory function


## -description

Releases error-specific memory allocated by the EAP authenticator method.

<b>EapMethodAuthenticatorFreeErrorMemory</b> is a function prototype.

## -parameters

### -param pEapError [in]

A pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains the error data to free.

## -see-also

[EAPHost Authenticator Method Functions](/windows/win32/eaphost/eap-host-authenticator-method-functions)