---
UID: NS:webauthn._WEBAUTHN_CREDENTIAL_EX
tech.root: webauthn
title: WEBAUTHN_CREDENTIAL_EX
ms.date: 07/19/2022
targetos: Windows
description: Data about a credential with extra information.
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
req.typenames: WEBAUTHN_CREDENTIAL_EX, *PWEBAUTHN_CREDENTIAL_EX
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - webauthn.h
api_name:
 - _WEBAUTHN_CREDENTIAL_EX
 - PWEBAUTHN_CREDENTIAL_EX
 - WEBAUTHN_CREDENTIAL_EX
f1_keywords:
 - _WEBAUTHN_CREDENTIAL_EX
 - webauthn/_WEBAUTHN_CREDENTIAL_EX
 - PWEBAUTHN_CREDENTIAL_EX
 - webauthn/PWEBAUTHN_CREDENTIAL_EX
 - WEBAUTHN_CREDENTIAL_EX
 - webauthn/WEBAUTHN_CREDENTIAL_EX
dev_langs:
 - c++
helpviewer_keywords:
 - _WEBAUTHN_CREDENTIAL_EX
---

## -description

Data about a credential with extra information, such as *dwTransports**.

## -struct-fields

### -field dwVersion

Version of this structure, to allow for modifications in the future. This field is required and should be set to **CURRENT_VERSION**.

### -field cbId

The size of **pbID**.

### -field pbId

Unique ID for this particular credential.

### -field pwszCredentialType

Well-known credential type specifying the type of this particular credential.

### -field dwTransports

The transports. **0** implies no transport restrictions.

## -remarks

## -see-also

[WEBAUTHN_CREDENTIAL](./ns-webauthn-webauthn_credential.md)
