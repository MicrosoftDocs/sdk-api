---
UID: NS:webauthn._WEBAUTHN_COSE_CREDENTIAL_PARAMETER
tech.root: webauthn
title: WEBAUTHN_COSE_CREDENTIAL_PARAMETER
ms.date: 07/19/2022
targetos: Windows
description: The structure containing the COSE credential parameter information.
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
req.typenames: WEBAUTHN_COSE_CREDENTIAL_PARAMETER, *PWEBAUTHN_COSE_CREDENTIAL_PARAMETER
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - webauthn.h
api_name:
 - _WEBAUTHN_COSE_CREDENTIAL_PARAMETER
 - PWEBAUTHN_COSE_CREDENTIAL_PARAMETER
 - WEBAUTHN_COSE_CREDENTIAL_PARAMETER
f1_keywords:
 - _WEBAUTHN_COSE_CREDENTIAL_PARAMETER
 - webauthn/_WEBAUTHN_COSE_CREDENTIAL_PARAMETER
 - PWEBAUTHN_COSE_CREDENTIAL_PARAMETER
 - webauthn/PWEBAUTHN_COSE_CREDENTIAL_PARAMETER
 - WEBAUTHN_COSE_CREDENTIAL_PARAMETER
 - webauthn/WEBAUTHN_COSE_CREDENTIAL_PARAMETER
dev_langs:
 - c++
helpviewer_keywords:
 - _WEBAUTHN_COSE_CREDENTIAL_PARAMETER
---

## -description

The structure containing the COSE credential parameter that is sent to the authenticator.

## -struct-fields

### -field dwVersion

Version of this structure, to allow for modifications in the future. This field is required and should be set to **CURRENT_VERSION**.

### -field pwszCredentialType

Well-known credential type specifying a credential to create.

### -field lAlg

Well-known COSE algorithm specifying the algorithm to use for the credential.

## -remarks

## -see-also

[WEBAUTHN_COSE_CREDENTIAL_PARAMETERS](./ns-webauthn-webauthn_cose_credential_parameters.md)
