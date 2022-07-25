---
UID: NF:eapmethodauthenticatorapis.EapMethodAuthenticatorGetAttributes
title: EapMethodAuthenticatorGetAttributes function (eapmethodauthenticatorapis.h)
description: Obtains an array of EAP authentication attributes from the EAP authenticator method.
helpviewer_keywords: ["EapMethodAuthenticatorGetAttributes","EapMethodAuthenticatorGetAttributes function [EAPHost]","eaphost.eapmethodauthenticatorgetattributes","eapmethodauthenticatorapis/EapMethodAuthenticatorGetAttributes"]
old-location: eaphost\eapmethodauthenticatorgetattributes.htm
tech.root: eaphost
ms.assetid: 531a95c9-b804-4151-b571-163f870672bb
ms.date: 12/05/2018
ms.keywords: EapMethodAuthenticatorGetAttributes, EapMethodAuthenticatorGetAttributes function [EAPHost], eaphost.eapmethodauthenticatorgetattributes, eapmethodauthenticatorapis/EapMethodAuthenticatorGetAttributes
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
 - EapMethodAuthenticatorGetAttributes
 - eapmethodauthenticatorapis/EapMethodAuthenticatorGetAttributes
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
 - EapMethodAuthenticatorGetAttributes
---

# EapMethodAuthenticatorGetAttributes function


## -description

Obtains an array of EAP authentication attributes from the EAP authenticator method.

<b>EapMethodAuthenticatorGetAttributes</b> is a function prototype.

## -parameters

### -param sessionHandle [in]

A pointer to an <b>EAP_SESSION_HANDLE</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionHandle</i> parameter in a previous call to <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession">EapMethodAuthenticatorBeginSession</a>.

### -param pAttribs [out]

A pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes">EapAttributes</a> structure that contains an array of EAP authentication response attributes for the supplicant.

### -param ppEapError [out]

A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorfreeerrormemory">EapMethodAuthenticatorFreeErrorMemory</a>.

## -remarks

This call is performed by a authenticator-based EAPHost using a function pointer to this API. This API must be implemented on the EAP authenticator method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.

## -see-also

[EAPHost Authenticator Method Functions](/windows/win32/eaphost/eap-host-authenticator-method-functions)



<a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession">EapMethodAuthenticatorBeginSession</a>