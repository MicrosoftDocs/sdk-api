---
UID: NS:webauthn._WEBAUTHN_CRED_PROTECT_EXTENSION_IN
tech.root: webauthn
title: WEBAUTHN_CRED_PROTECT_EXTENSION_IN
ms.date: 07/19/2022
targetos: Windows
description: Contains the credential protect extension information.
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
req.typenames: WEBAUTHN_CRED_PROTECT_EXTENSION_IN, *PWEBAUTHN_CRED_PROTECT_EXTENSION_IN
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - webauthn.h
api_name:
 - _WEBAUTHN_CRED_PROTECT_EXTENSION_IN
 - PWEBAUTHN_CRED_PROTECT_EXTENSION_IN
 - WEBAUTHN_CRED_PROTECT_EXTENSION_IN
f1_keywords:
 - _WEBAUTHN_CRED_PROTECT_EXTENSION_IN
 - webauthn/_WEBAUTHN_CRED_PROTECT_EXTENSION_IN
 - PWEBAUTHN_CRED_PROTECT_EXTENSION_IN
 - webauthn/PWEBAUTHN_CRED_PROTECT_EXTENSION_IN
 - WEBAUTHN_CRED_PROTECT_EXTENSION_IN
 - webauthn/WEBAUTHN_CRED_PROTECT_EXTENSION_IN
dev_langs:
 - c++
helpviewer_keywords:
 - _WEBAUTHN_CRED_PROTECT_EXTENSION_IN
---

## -description

The structure containing the credential protect extension information.

## -struct-fields

### -field dwCredProtect

One of the **WEBAUTHN_USER_VERIFICATION** values.

### -field bRequireCredProtect

Set the this to **TRUE** to require authenticator support for the **credProtect** extension.

## -remarks

## -see-also

[WEBAUTHN_CREDENTIAL](./ns-webauthn-webauthn_credential.md)
