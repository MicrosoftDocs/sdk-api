---
UID: NS:eapauthenticatoractiondefine._EAP_METHOD_AUTHENTICATOR_RESULT
title: EAP_METHOD_AUTHENTICATOR_RESULT (eapauthenticatoractiondefine.h)
description: Contains authentication results returned by an EAP authenticator method.
helpviewer_keywords: ["EAP_METHOD_AUTHENTICATOR_RESULT","EAP_METHOD_AUTHENTICATOR_RESULT structure [EAPHost]","eapauthenticatoractiondefine/EAP_METHOD_AUTHENTICATOR_RESULT","eaphost.eap_method_authenticator_result"]
old-location: eaphost\eap_method_authenticator_result.htm
tech.root: eaphost
ms.assetid: 8367fd35-852b-4cdf-9a86-7d07a5a1a2ef
ms.date: 12/05/2018
ms.keywords: EAP_METHOD_AUTHENTICATOR_RESULT, EAP_METHOD_AUTHENTICATOR_RESULT structure [EAPHost], eapauthenticatoractiondefine/EAP_METHOD_AUTHENTICATOR_RESULT, eaphost.eap_method_authenticator_result
req.header: eapauthenticatoractiondefine.h
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
req.typenames: EAP_METHOD_AUTHENTICATOR_RESULT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EAP_METHOD_AUTHENTICATOR_RESULT
 - eapauthenticatoractiondefine/_EAP_METHOD_AUTHENTICATOR_RESULT
 - EAP_METHOD_AUTHENTICATOR_RESULT
 - eapauthenticatoractiondefine/EAP_METHOD_AUTHENTICATOR_RESULT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - EapAuthenticatorActionDefine.h
api_name:
 - EAP_METHOD_AUTHENTICATOR_RESULT
---

# EAP_METHOD_AUTHENTICATOR_RESULT structure


## -description

Contains authentication results returned by an EAP authenticator method.

## -struct-fields

### -field fIsSuccess

If <b>TRUE</b>, the supplicant was successfully authenticated; if <b>FALSE</b>, it was not.

### -field dwFailureReason

Contains a reason code if the supplicant could not be authenticated. Reason codes are generally expected to originate from winerror.h.

### -field pAuthAttribs

A pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes">EAP_ATTRIBUTES</a> structure that contains the EAP attributes  returned by the authentication session.

## -see-also

[EAPHost Authenticator Method Structures](/windows/win32/eaphost/eap-host-authenticator-method-structures)