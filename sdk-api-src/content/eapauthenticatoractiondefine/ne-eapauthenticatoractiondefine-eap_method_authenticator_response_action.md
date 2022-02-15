---
UID: NE:eapauthenticatoractiondefine._EAP_METHOD_AUTHENTICATOR_RESPONSE_ACTION
title: EAP_METHOD_AUTHENTICATOR_RESPONSE_ACTION (eapauthenticatoractiondefine.h)
description: Defines the set of response instructions sent by the authenticator to the supplicant or EAP peer method.
helpviewer_keywords: ["EAP_METHOD_AUTHENTICATOR_RESPONSE_ACTION","EAP_METHOD_AUTHENTICATOR_RESPONSE_ACTION enumeration [EAPHost]","EAP_METHOD_AUTHENTICATOR_RESPONSE_AUTHENTICATE","EAP_METHOD_AUTHENTICATOR_RESPONSE_DISCARD","EAP_METHOD_AUTHENTICATOR_RESPONSE_HANDLE_IDENTITY","EAP_METHOD_AUTHENTICATOR_RESPONSE_RESPOND","EAP_METHOD_AUTHENTICATOR_RESPONSE_RESULT","EAP_METHOD_AUTHENTICATOR_RESPONSE_SEND","eapauthenticatoractiondefine/EAP_METHOD_AUTHENTICATOR_RESPONSE_ACTION","eapauthenticatoractiondefine/EAP_METHOD_AUTHENTICATOR_RESPONSE_AUTHENTICATE","eapauthenticatoractiondefine/EAP_METHOD_AUTHENTICATOR_RESPONSE_DISCARD","eapauthenticatoractiondefine/EAP_METHOD_AUTHENTICATOR_RESPONSE_HANDLE_IDENTITY","eapauthenticatoractiondefine/EAP_METHOD_AUTHENTICATOR_RESPONSE_RESPOND","eapauthenticatoractiondefine/EAP_METHOD_AUTHENTICATOR_RESPONSE_RESULT","eapauthenticatoractiondefine/EAP_METHOD_AUTHENTICATOR_RESPONSE_SEND","eaphost.eap_method_authenticator_response_action"]
old-location: eaphost\eap_method_authenticator_response_action.htm
tech.root: eaphost
ms.assetid: 992336ec-65ef-48bf-947f-1d569c9bd4aa
ms.date: 12/05/2018
ms.keywords: EAP_METHOD_AUTHENTICATOR_RESPONSE_ACTION, EAP_METHOD_AUTHENTICATOR_RESPONSE_ACTION enumeration [EAPHost], EAP_METHOD_AUTHENTICATOR_RESPONSE_AUTHENTICATE, EAP_METHOD_AUTHENTICATOR_RESPONSE_DISCARD, EAP_METHOD_AUTHENTICATOR_RESPONSE_HANDLE_IDENTITY, EAP_METHOD_AUTHENTICATOR_RESPONSE_RESPOND, EAP_METHOD_AUTHENTICATOR_RESPONSE_RESULT, EAP_METHOD_AUTHENTICATOR_RESPONSE_SEND, eapauthenticatoractiondefine/EAP_METHOD_AUTHENTICATOR_RESPONSE_ACTION, eapauthenticatoractiondefine/EAP_METHOD_AUTHENTICATOR_RESPONSE_AUTHENTICATE, eapauthenticatoractiondefine/EAP_METHOD_AUTHENTICATOR_RESPONSE_DISCARD, eapauthenticatoractiondefine/EAP_METHOD_AUTHENTICATOR_RESPONSE_HANDLE_IDENTITY, eapauthenticatoractiondefine/EAP_METHOD_AUTHENTICATOR_RESPONSE_RESPOND, eapauthenticatoractiondefine/EAP_METHOD_AUTHENTICATOR_RESPONSE_RESULT, eapauthenticatoractiondefine/EAP_METHOD_AUTHENTICATOR_RESPONSE_SEND, eaphost.eap_method_authenticator_response_action
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
req.typenames: EAP_METHOD_AUTHENTICATOR_RESPONSE_ACTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EAP_METHOD_AUTHENTICATOR_RESPONSE_ACTION
 - eapauthenticatoractiondefine/_EAP_METHOD_AUTHENTICATOR_RESPONSE_ACTION
 - EAP_METHOD_AUTHENTICATOR_RESPONSE_ACTION
 - eapauthenticatoractiondefine/EAP_METHOD_AUTHENTICATOR_RESPONSE_ACTION
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
 - EAP_METHOD_AUTHENTICATOR_RESPONSE_ACTION
---

# EAP_METHOD_AUTHENTICATOR_RESPONSE_ACTION enumeration


## -description

Defines the set of response instructions sent by the  authenticator to the supplicant or EAP peer method.

## -enum-fields

### -field EAP_METHOD_AUTHENTICATOR_RESPONSE_DISCARD:0

The supplicant should discard the response as it is not usable by EAPHost.

### -field EAP_METHOD_AUTHENTICATOR_RESPONSE_SEND

The supplicant should send the indicated packet to the authenticator.

### -field EAP_METHOD_AUTHENTICATOR_RESPONSE_RESULT

The supplicant should act on EAP attributes returned by the authenticator.

### -field EAP_METHOD_AUTHENTICATOR_RESPONSE_RESPOND

The supplicant should generate a  context-specific response to the authenticator request.

### -field EAP_METHOD_AUTHENTICATOR_RESPONSE_AUTHENTICATE

The authenticator method has started authentication of the supplicant.

### -field EAP_METHOD_AUTHENTICATOR_RESPONSE_HANDLE_IDENTITY

The peer method should return the handle for the user identity of the supplicant.

### -field v1_enum

## -see-also

[EAP Host Authenticator Method Enumerations](/windows/win32/eaphost/eap-host-authenticator-method-enumerations)

