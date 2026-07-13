---
UID: NS:webauthn._WEBAUTHN_CLIENT_DATA
tech.root: webauthn
title: WEBAUTHN_CLIENT_DATA
ms.date: 07/19/2022
targetos: Windows
description: A structure containing the client data that is sent to the authenticator.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: webauthn.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: WEBAUTHN_CLIENT_DATA, *PWEBAUTHN_CLIENT_DATA
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - webauthn.h
api_name:
 - _WEBAUTHN_CLIENT_DATA
 - PWEBAUTHN_CLIENT_DATA
 - WEBAUTHN_CLIENT_DATA
f1_keywords:
 - _WEBAUTHN_CLIENT_DATA
 - webauthn/_WEBAUTHN_CLIENT_DATA
 - PWEBAUTHN_CLIENT_DATA
 - webauthn/PWEBAUTHN_CLIENT_DATA
 - WEBAUTHN_CLIENT_DATA
 - webauthn/WEBAUTHN_CLIENT_DATA
dev_langs:
 - c++
helpviewer_keywords:
 - _WEBAUTHN_CLIENT_DATA
---

## -description

A structure containing the client data that is sent to the authenticator.

## -struct-fields

### -field dwVersion

Version of this structure, to allow for modifications in the future. This field is required and should be set to **CURRENT_VERSION**.

### -field cbClientDataJSON

The size of the **pbClientDataJSON** field.

### -field pbClientDataJSON

UTF-8 encoded JSON serialization of the client data.

### -field pwszHashAlgId

Hash algorithm ID used to hash the **pbClientDataJSON** field.

## -remarks

## -see-also

[WebAuthNAuthenticatorMakeCredential](./nf-webauthn-webauthnauthenticatormakecredential.md)
