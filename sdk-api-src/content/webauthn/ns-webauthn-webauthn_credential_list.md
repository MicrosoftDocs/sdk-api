---
UID: NS:webauthn._WEBAUTHN_CREDENTIAL_LIST
tech.root: webauthn
title: WEBAUTHN_CREDENTIAL_LIST
ms.date: 03/08/2024
targetos: Windows
description: The list of credentials that the user has registered with the authenticator.
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
req.typenames: WEBAUTHN_CREDENTIAL_LIST, *PWEBAUTHN_CREDENTIAL_LIST
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - webauthn.h
api_name:
 - _WEBAUTHN_CREDENTIAL_LIST
 - PWEBAUTHN_CREDENTIAL_LIST
 - WEBAUTHN_CREDENTIAL_LIST
f1_keywords:
 - _WEBAUTHN_CREDENTIAL_LIST
 - webauthn/_WEBAUTHN_CREDENTIAL_LIST
 - PWEBAUTHN_CREDENTIAL_LIST
 - webauthn/PWEBAUTHN_CREDENTIAL_LIST
 - WEBAUTHN_CREDENTIAL_LIST
 - webauthn/WEBAUTHN_CREDENTIAL_LIST
dev_langs:
 - c++
helpviewer_keywords:
 - _WEBAUTHN_CREDENTIAL_LIST
---

## -description

The list of credentials that the user has registered with the authenticator.

## -syntax

```cpp
typedef struct _WEBAUTHN_CREDENTIAL_LIST {
  DWORD                   cCredentials;
  PWEBAUTHN_CREDENTIAL_EX *ppCredentials;
} WEBAUTHN_CREDENTIAL_LIST, *PWEBAUTHN_CREDENTIAL_LIST;
```

## -struct-fields

### -field cCredentials

The size of *ppCredentials*.

### -field ppCredentials

The array of credentials.

## -remarks

## -see-also

[WEBAUTHN_CREDENTIAL](./ns-webauthn-webauthn_credential.md)
