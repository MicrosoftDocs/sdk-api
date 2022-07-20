---
UID: NS:webauthn._WEBAUTHN_EXTENSION
tech.root: webauthn
title: WEBAUTHN_EXTENSION
ms.date: 07/19/2022
targetos: Windows
description: Contains information about an extension.
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
req.typenames: WEBAUTHN_EXTENSION, *PWEBAUTHN_EXTENSION
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - webauthn.h
api_name:
 - _WEBAUTHN_EXTENSION
 - PWEBAUTHN_EXTENSION
 - WEBAUTHN_EXTENSION
f1_keywords:
 - _WEBAUTHN_EXTENSION
 - webauthn/_WEBAUTHN_EXTENSION
 - PWEBAUTHN_EXTENSION
 - webauthn/PWEBAUTHN_EXTENSION
 - WEBAUTHN_EXTENSION
 - webauthn/WEBAUTHN_EXTENSION
dev_langs:
 - c++
helpviewer_keywords:
 - _WEBAUTHN_EXTENSION
---

## -description

Contains information about an extension.

## -struct-fields

### -field pwszExtensionIdentifier

The extension identifier.

### -field cbExtension

The size of **pvExtension**.

### -field pvExtension

The extension data.

## -remarks

## -see-also

[WEBAUTHN_EXTENSIONS](./ns-webauthn-webauthn_extensions.md)
