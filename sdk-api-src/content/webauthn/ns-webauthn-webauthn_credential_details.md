---
UID: NS:webauthn._WEBAUTHN_CREDENTIAL_DETAILS
tech.root: webauthn
title: WEBAUTHN_CREDENTIAL_DETAILS
ms.date: 03/06/2024
targetos: Windows
description: Contains the data for a credential.
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
req.typenames: WEBAUTHN_CREDENTIAL_DETAILS, *PWEBAUTHN_CREDENTIAL_DETAILS
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - webauthn.h
api_name:
 - _WEBAUTHN_CREDENTIAL_DETAILS
 - PWEBAUTHN_CREDENTIAL_DETAILS
 - WEBAUTHN_CREDENTIAL_DETAILS
f1_keywords:
 - _WEBAUTHN_CREDENTIAL_DETAILS
 - webauthn/_WEBAUTHN_CREDENTIAL_DETAILS
 - PWEBAUTHN_CREDENTIAL_DETAILS
 - webauthn/PWEBAUTHN_CREDENTIAL_DETAILS
 - WEBAUTHN_CREDENTIAL_DETAILS
 - webauthn/WEBAUTHN_CREDENTIAL_DETAILS
dev_langs:
 - c++
helpviewer_keywords:
 - _WEBAUTHN_CREDENTIAL_DETAILS
---

## -description

The structure containing the credential data.

## -syntax

```cpp
typedef struct _WEBAUTHN_CREDENTIAL_DETAILS {
  DWORD                             dwVersion;
  DWORD                             cbCredentialID;
  PBYTE                             pbCredentialID;
  PWEBAUTHN_RP_ENTITY_INFORMATION   pRpInformation;
  PWEBAUTHN_USER_ENTITY_INFORMATION pUserInformation;
  BOOL                              bRemovable;
  BOOL                              bBackedUp;
} WEBAUTHN_CREDENTIAL_DETAILS, *PWEBAUTHN_CREDENTIAL_DETAILS;
```

## -struct-fields

### -field dwVersion

Version of this structure, to allow for modifications in the future. This field is required and should be set to **CURRENT_VERSION**.

### -field cbCredentialID

The size of pbCredentialID.

### -field pbCredentialID

The credential Id.

### -field pRpInformation

The relying party information.

### -field pUserInformation

The user information.

### -field bRemovable

Indicates if the credential is removable or not.

### -field bBackedUp

Indicates if the credential is backed up or not.

## -remarks

## -see-also

[WEBAUTHN_CREDENTIAL](./ns-webauthn-webauthn_credential.md)

[WEBAUTHN_CREDENTIAL_DETAILS_LIST](./ns-webauthn-webauthn_credential_details_list.md)
