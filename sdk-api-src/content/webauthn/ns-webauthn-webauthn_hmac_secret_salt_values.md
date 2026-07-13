---
UID: NS:webauthn._WEBAUTHN_HMAC_SECRET_SALT_VALUES
tech.root: webauthn
title: WEBAUTHN_HMAC_SECRET_SALT_VALUES
ms.date: 07/19/2022
targetos: Windows
description: Contains the SALT values for the HMAC secret.
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
req.typenames: WEBAUTHN_HMAC_SECRET_SALT_VALUES, *PWEBAUTHN_HMAC_SECRET_SALT_VALUES
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - webauthn.h
api_name:
 - _WEBAUTHN_HMAC_SECRET_SALT_VALUES
 - PWEBAUTHN_HMAC_SECRET_SALT_VALUES
 - WEBAUTHN_HMAC_SECRET_SALT_VALUES
f1_keywords:
 - _WEBAUTHN_HMAC_SECRET_SALT_VALUES
 - webauthn/_WEBAUTHN_HMAC_SECRET_SALT_VALUES
 - PWEBAUTHN_HMAC_SECRET_SALT_VALUES
 - webauthn/PWEBAUTHN_HMAC_SECRET_SALT_VALUES
 - WEBAUTHN_HMAC_SECRET_SALT_VALUES
 - webauthn/WEBAUTHN_HMAC_SECRET_SALT_VALUES
dev_langs:
 - c++
helpviewer_keywords:
 - _WEBAUTHN_HMAC_SECRET_SALT_VALUES
---

## -description

The structure that contains the SALT values for the HMAC secret.

## -struct-fields

### -field pGlobalHmacSalt

The global HMAC SALT.

### -field cCredWithHmacSecretSaltList

The size of **pCredWithHmacSecretSaltList**.

### -field pCredWithHmacSecretSaltList

The list of credentials with HMAC secret SALT.

## -remarks

## -see-also

[WEBAUTHN_HMAC_SECRET_SALT](./ns-webauthn-webauthn_hmac_secret_salt.md)
