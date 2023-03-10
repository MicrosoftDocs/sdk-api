---
UID: NS:webauthn._WEBAUTHN_USER_ENTITY_INFORMATION
tech.root: webauthn
title: WEBAUTHN_USER_ENTITY_INFORMATION
ms.date: 07/19/2022
targetos: Windows
description: Information about a user entity.
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
req.typenames: WEBAUTHN_USER_ENTITY_INFORMATION, *PWEBAUTHN_USER_ENTITY_INFORMATION
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - webauthn.h
api_name:
 - _WEBAUTHN_USER_ENTITY_INFORMATION
 - PWEBAUTHN_USER_ENTITY_INFORMATION
 - WEBAUTHN_USER_ENTITY_INFORMATION
f1_keywords:
 - _WEBAUTHN_USER_ENTITY_INFORMATION
 - webauthn/_WEBAUTHN_USER_ENTITY_INFORMATION
 - PWEBAUTHN_USER_ENTITY_INFORMATION
 - webauthn/PWEBAUTHN_USER_ENTITY_INFORMATION
 - WEBAUTHN_USER_ENTITY_INFORMATION
 - webauthn/WEBAUTHN_USER_ENTITY_INFORMATION
dev_langs:
 - c++
helpviewer_keywords:
 - _WEBAUTHN_USER_ENTITY_INFORMATION
---

## -description

Information about a user entity.

## -struct-fields

### -field dwVersion

Version of this structure, to allow for modifications in the future. This field is required and should be set to **CURRENT_VERSION**.

### -field cbId

The size of **pbId**.

### -field pbId

Identifier for the user. This field is required.

### -field pwszName

Contains a detailed name for this account, such as "john.p.smith@example.com".

### -field pwszIcon

Optional URL that can be used to retrieve an image containing the user's current avatar or a data URI that contains the image data.

### -field pwszDisplayName

Contains the friendly name associated with the user account by the Relying Party, such as "John P. Smith".

## -remarks

## -see-also

[WEBAUTHN_CREDENTIAL_DETAILS](./ns-webauthn-webauthn_credential_details.md)
