---
UID: NS:webauthn._WEBAUTHN_CREDENTIAL
tech.root: webauthn
title: WEBAUTHN_CREDENTIAL
ms.date: 07/19/2022
targetos: Windows
description: Contains information about a credential.
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
req.typenames: WEBAUTHN_CREDENTIAL, *PWEBAUTHN_CREDENTIAL
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - webauthn.h
api_name:
 - _WEBAUTHN_CREDENTIAL
 - PWEBAUTHN_CREDENTIAL
 - WEBAUTHN_CREDENTIAL
f1_keywords:
 - _WEBAUTHN_CREDENTIAL
 - webauthn/_WEBAUTHN_CREDENTIAL
 - PWEBAUTHN_CREDENTIAL
 - webauthn/PWEBAUTHN_CREDENTIAL
 - WEBAUTHN_CREDENTIAL
 - webauthn/WEBAUTHN_CREDENTIAL
dev_langs:
 - c++
helpviewer_keywords:
 - _WEBAUTHN_CREDENTIAL
---

## -description

Contains information about a credential.

## -struct-fields

### -field dwVersion

Version of this structure, to allow for modifications in the future. This field is required and should be set to **CURRENT_VERSION**.

### -field cbId

The size of **pbId**.

### -field pbId

Unique ID for this particular credential.

### -field pwszCredentialType

Well-known credential type specifying the type of this particular credential.

## -remarks

## -see-also

[WEBAUTHN_CREDENTIALS](./ns-webauthn-webauthn_credentials.md)
