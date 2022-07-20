---
UID: NS:webauthn._WEBAUTHN_RP_ENTITY_INFORMATION
tech.root: webauthn
title: WEBAUTHN_RP_ENTITY_INFORMATION
ms.date: 07/19/2022
targetos: Windows
description: Information about the Relying Party.
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
req.typenames: WEBAUTHN_RP_ENTITY_INFORMATION, *PWEBAUTHN_RP_ENTITY_INFORMATION
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - webauthn.h
api_name:
 - _WEBAUTHN_RP_ENTITY_INFORMATION
 - PWEBAUTHN_RP_ENTITY_INFORMATION
 - WEBAUTHN_RP_ENTITY_INFORMATION
f1_keywords:
 - _WEBAUTHN_RP_ENTITY_INFORMATION
 - webauthn/_WEBAUTHN_RP_ENTITY_INFORMATION
 - PWEBAUTHN_RP_ENTITY_INFORMATION
 - webauthn/PWEBAUTHN_RP_ENTITY_INFORMATION
 - WEBAUTHN_RP_ENTITY_INFORMATION
 - webauthn/WEBAUTHN_RP_ENTITY_INFORMATION
dev_langs:
 - c++
helpviewer_keywords:
 - _WEBAUTHN_RP_ENTITY_INFORMATION
---

## -description

Information about the Relying Party entity.

## -struct-fields

### -field dwVersion

Version of this structure, to allow for modifications in the future. This field is required and should be set to **CURRENT_VERSION**.

### -field pwszId

Identifier for the Relying Party. This field is required.

### -field pwszName

Contains the friendly name of the Relying Party, such as "Acme Corporation", "Widgets Inc", or "Contoso". This field is required.

### -field pwszIcon

Optional URL pointing to the Relying Party's logo.

## -remarks

## -see-also

[WEBAUTHN_CREDENTIAL_DETAILS](./ns-webauthn-webauthn_credential_details.md)
