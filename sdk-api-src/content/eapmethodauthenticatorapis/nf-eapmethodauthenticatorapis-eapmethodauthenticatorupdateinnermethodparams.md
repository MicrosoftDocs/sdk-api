---
UID: NF:eapmethodauthenticatorapis.EapMethodAuthenticatorUpdateInnerMethodParams
title: EapMethodAuthenticatorUpdateInnerMethodParams function (eapmethodauthenticatorapis.h)
description: Updates the EAP authentication session settings previous established by a call to EapMethodAuthenticatorBeginSession from the server EAPHost.
helpviewer_keywords: ["EapMethodAuthenticatorUpdateInnerMethodParams","EapMethodAuthenticatorUpdateInnerMethodParams function [EAPHost]","eaphost.eapmethodauthenticatorupdateinnermethodparams","eapmethodauthenticatorapis/EapMethodAuthenticatorUpdateInnerMethodParams"]
old-location: eaphost\eapmethodauthenticatorupdateinnermethodparams.htm
tech.root: eaphost
ms.assetid: 13ca6504-63c6-4dd6-a3bf-0f3929bc527f
ms.date: 12/05/2018
ms.keywords: EapMethodAuthenticatorUpdateInnerMethodParams, EapMethodAuthenticatorUpdateInnerMethodParams function [EAPHost], eaphost.eapmethodauthenticatorupdateinnermethodparams, eapmethodauthenticatorapis/EapMethodAuthenticatorUpdateInnerMethodParams
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
 - EapMethodAuthenticatorUpdateInnerMethodParams
 - eapmethodauthenticatorapis/EapMethodAuthenticatorUpdateInnerMethodParams
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
 - EapMethodAuthenticatorUpdateInnerMethodParams
---

# EapMethodAuthenticatorUpdateInnerMethodParams function


## -description

Updates the EAP authentication session settings previous established by a call to <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession">EapMethodAuthenticatorBeginSession</a> from the server EAPHost.

<b>EapMethodAuthenticatorUpdateInnerMethodParams</b> is a function prototype.

## -parameters

### -param sessionHandle [in]

A pointer to an <b>EAP_SESSION_HANDLE</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionHandle</i> parameter in a previous call to <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession">EapMethodAuthenticatorBeginSession</a>.

### -param dwFlags [in]

A combination of [EAP flags](/windows/win32/eaphost/eap-method-flags) that describe the  updated EAP authentication session behavior.

### -param pwszIdentity [in]

A zero-terminated Unicode string that contains the  updated identity of the user to authenticate.

### -param pAttributeArray [in]

A pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes">EapAttributes</a> array structure that specifies the updated EAP attributes of the entity to authenticate.

### -param ppEapError [out]

A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorfreeerrormemory">EapMethodAuthenticatorFreeErrorMemory</a>.

## -see-also

[EAPHost Authenticator Method Functions](/windows/win32/eaphost/eap-host-authenticator-method-functions)



<a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession">EapMethodAuthenticatorBeginSession</a>