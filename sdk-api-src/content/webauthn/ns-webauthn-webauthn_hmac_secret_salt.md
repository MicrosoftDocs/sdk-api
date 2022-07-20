---
UID: NS:webauthn._WEBAUTHN_HMAC_SECRET_SALT
tech.root: webauthn
title: WEBAUTHN_HMAC_SECRET_SALT
ms.date: 07/19/2022
targetos: Windows
description: Contains the SALT values for the Hmac-Secret.
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
req.typenames: WEBAUTHN_HMAC_SECRET_SALT, *PWEBAUTHN_HMAC_SECRET_SALT
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - webauthn.h
api_name:
 - _WEBAUTHN_HMAC_SECRET_SALT
 - PWEBAUTHN_HMAC_SECRET_SALT
 - WEBAUTHN_HMAC_SECRET_SALT
f1_keywords:
 - _WEBAUTHN_HMAC_SECRET_SALT
 - webauthn/_WEBAUTHN_HMAC_SECRET_SALT
 - PWEBAUTHN_HMAC_SECRET_SALT
 - webauthn/PWEBAUTHN_HMAC_SECRET_SALT
 - WEBAUTHN_HMAC_SECRET_SALT
 - webauthn/WEBAUTHN_HMAC_SECRET_SALT
dev_langs:
 - c++
helpviewer_keywords:
 - _WEBAUTHN_HMAC_SECRET_SALT
---

## -description

Contains the SALT values for the Hmac-Secret.

## -struct-fields

### -field cbFirst

The size of pbFirst.

### -field pbFirst

The first SALT value.

### -field cbSecond

THe size of pbSecond.

### -field pbSecond

The second SALT value.

## -remarks

SALT values, by default, are converted into RAW Hmac-Secret values as per PRF extension.

## -see-also

[WEBAUTHN_CRED_WITH_HMAC_SECRET_SALT](./ns-webauthn-webauthn_cred_with_hmac_secret_salt.md)

[WEBAUTHN_HMAC_SECRET_SALT_VALUES](./ns-webauthn-webauthn_hmac_secret_salt_values.md)
