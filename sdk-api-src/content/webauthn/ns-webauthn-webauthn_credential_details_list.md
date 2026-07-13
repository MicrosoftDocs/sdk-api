---
UID: NS:webauthn._WEBAUTHN_CREDENTIAL_DETAILS_LIST
tech.root: webauthn
title: WEBAUTHN_CREDENTIAL_DETAILS_LIST
ms.date: 03/08/2024
targetos: Windows
description: The list of credentials.
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
req.typenames: WEBAUTHN_CREDENTIAL_DETAILS_LIST, *PWEBAUTHN_CREDENTIAL_DETAILS_LIST
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - webauthn.h
api_name:
 - _WEBAUTHN_CREDENTIAL_DETAILS_LIST
 - PWEBAUTHN_CREDENTIAL_DETAILS_LIST
 - WEBAUTHN_CREDENTIAL_DETAILS_LIST
f1_keywords:
 - _WEBAUTHN_CREDENTIAL_DETAILS_LIST
 - webauthn/_WEBAUTHN_CREDENTIAL_DETAILS_LIST
 - PWEBAUTHN_CREDENTIAL_DETAILS_LIST
 - webauthn/PWEBAUTHN_CREDENTIAL_DETAILS_LIST
 - WEBAUTHN_CREDENTIAL_DETAILS_LIST
 - webauthn/WEBAUTHN_CREDENTIAL_DETAILS_LIST
dev_langs:
 - c++
helpviewer_keywords:
 - _WEBAUTHN_CREDENTIAL_DETAILS_LIST
---

## -description

The list of credential details.

## -syntax

```cpp
typedef struct _WEBAUTHN_CREDENTIAL_DETAILS_LIST {
  DWORD                        cCredentialDetails;
  PWEBAUTHN_CREDENTIAL_DETAILS *ppCredentialDetails;
} WEBAUTHN_CREDENTIAL_DETAILS_LIST, *PWEBAUTHN_CREDENTIAL_DETAILS_LIST;
```

## -struct-fields

### -field cCredentialDetails

The size of the credential details array.

### -field ppCredentialDetails

The credential details array.

## -remarks

## -see-also

[WEBAUTHN_CREDENTIAL_DETAILS](./ns-webauthn-webauthn_credential_details.md)
