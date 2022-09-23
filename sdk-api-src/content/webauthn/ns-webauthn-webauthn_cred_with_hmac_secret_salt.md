---
UID: NS:webauthn._WEBAUTHN_CRED_WITH_HMAC_SECRET_SALT
tech.root: webauthn
title: WEBAUTHN_CRED_WITH_HMAC_SECRET_SALT
ms.date: 07/19/2022
targetos: Windows
description: The structure containing the credential with SALT values.
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
req.typenames: WEBAUTHN_CRED_WITH_HMAC_SECRET_SALT, *PWEBAUTHN_CRED_WITH_HMAC_SECRET_SALT
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - webauthn.h
api_name:
 - _WEBAUTHN_CRED_WITH_HMAC_SECRET_SALT
 - PWEBAUTHN_CRED_WITH_HMAC_SECRET_SALT
 - WEBAUTHN_CRED_WITH_HMAC_SECRET_SALT
f1_keywords:
 - _WEBAUTHN_CRED_WITH_HMAC_SECRET_SALT
 - webauthn/_WEBAUTHN_CRED_WITH_HMAC_SECRET_SALT
 - PWEBAUTHN_CRED_WITH_HMAC_SECRET_SALT
 - webauthn/PWEBAUTHN_CRED_WITH_HMAC_SECRET_SALT
 - WEBAUTHN_CRED_WITH_HMAC_SECRET_SALT
 - webauthn/WEBAUTHN_CRED_WITH_HMAC_SECRET_SALT
dev_langs:
 - c++
helpviewer_keywords:
 - _WEBAUTHN_CRED_WITH_HMAC_SECRET_SALT
---

## -description

The structure containing the credential with SALT values.

## -struct-fields

### -field cbCredID

The size of **pbCredID**.

### -field pbCredID

The credential Id.

### -field pHmacSecretSalt

PRF Values for the credential.

## -remarks

## -see-also

[WEBAUTHN_CREDENTIAL](./ns-webauthn-webauthn_credential.md)

[WEBAUTHN_HMAC_SECRET_SALT](./ns-webauthn-webauthn_hmac_secret_salt.md)
