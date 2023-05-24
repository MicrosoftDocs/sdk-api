---
UID: NS:webauthn._WEBAUTHN_GET_CREDENTIALS_OPTIONS
tech.root: webauthn
title: WEBAUTHN_GET_CREDENTIALS_OPTIONS
ms.date: 07/19/2022
targetos: Windows
description: Contains the options for the WebAuthNGetPlatformCredentialsList function.
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
req.typenames: WEBAUTHN_GET_CREDENTIALS_OPTIONS, *PWEBAUTHN_GET_CREDENTIALS_OPTIONS
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - webauthn.h
api_name:
 - _WEBAUTHN_GET_CREDENTIALS_OPTIONS
 - PWEBAUTHN_GET_CREDENTIALS_OPTIONS
 - WEBAUTHN_GET_CREDENTIALS_OPTIONS
f1_keywords:
 - _WEBAUTHN_GET_CREDENTIALS_OPTIONS
 - webauthn/_WEBAUTHN_GET_CREDENTIALS_OPTIONS
 - PWEBAUTHN_GET_CREDENTIALS_OPTIONS
 - webauthn/PWEBAUTHN_GET_CREDENTIALS_OPTIONS
 - WEBAUTHN_GET_CREDENTIALS_OPTIONS
 - webauthn/WEBAUTHN_GET_CREDENTIALS_OPTIONS
dev_langs:
 - c++
helpviewer_keywords:
 - _WEBAUTHN_GET_CREDENTIALS_OPTIONS
---

## -description

Contains the options for the [WebAuthNGetPlatformCredentialsList](./nf-webauthn-webauthngetplatformcredentiallist.md) function.

## -struct-fields

### -field dwVersion

Version of this structure, to allow for modifications in the future. This field is required and should be set to **CURRENT_VERSION**.

### -field pwszRpId

The Id of the relying party that is making the request. This field is _optional_.

### -field bBrowserInPrivateMode

Is browser in-private mode. This field is _optional_ and defaults to **FALSE**.

## -remarks

## -see-also

[WebAuthNGetPlatformCredentialsList](./nf-webauthn-webauthngetplatformcredentiallist.md)
