---
UID: NS:webauthn._WEBAUTHN_CREDENTIAL_ATTESTATION
tech.root: webauthn
title: WEBAUTHN_CREDENTIAL_ATTESTATION
ms.date: 07/19/2022
targetos: Windows
description: Contains the attestation data for a credential.
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
req.typenames: WEBAUTHN_CREDENTIAL_ATTESTATION, *PWEBAUTHN_CREDENTIAL_ATTESTATION
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - webauthn.h
api_name:
 - _WEBAUTHN_CREDENTIAL_ATTESTATION
 - PWEBAUTHN_CREDENTIAL_ATTESTATION
 - WEBAUTHN_CREDENTIAL_ATTESTATION
f1_keywords:
 - _WEBAUTHN_CREDENTIAL_ATTESTATION
 - webauthn/_WEBAUTHN_CREDENTIAL_ATTESTATION
 - PWEBAUTHN_CREDENTIAL_ATTESTATION
 - webauthn/PWEBAUTHN_CREDENTIAL_ATTESTATION
 - WEBAUTHN_CREDENTIAL_ATTESTATION
 - webauthn/WEBAUTHN_CREDENTIAL_ATTESTATION
dev_langs:
 - c++
helpviewer_keywords:
 - _WEBAUTHN_CREDENTIAL_ATTESTATION
---

## -description

Contains the attestation data for a credential.

## -struct-fields

### -field dwVersion

Version of this structure, to allow for modifications in the future. This field is required and should be set to **CURRENT_VERSION**.

### -field pwszFormatType

The attestation format type.

### -field cbAuthenticatorData

The size of **pbAuthenticatorData**.

### -field pbAuthenticatorData

The authenticator data that was created for this credential.

### -field cbAttestation

The size of the CBOR encoded attestation information.

### -field pbAttestation

The encoded CBOR attestation information.

### -field dwAttestationDecodeType

The attestation decode type.

### -field pvAttestationDecode

The attestation decode value.

### -field cbAttestationObject

The size of **pbAttestationObject**.

### -field pbAttestationObject

The CBOR encoded Attestation Object to be returned to the Relying Party.

### -field cbCredentialId

The size of **pbCredentialId**.

### -field pbCredentialId

The CredentialId bytes extracted from the Authenticator Data. Used by Edge to return to the Relying Party.

### -field Extensions

The extensions for this credential.

### -field dwUsedTransport

One of the **WEBAUTHN_CTAP_TRANSPORT** bits is passed, according to the transport that was used.

### -field bEpAtt

The EP attestation flag.

### -field bLargeBlobSupported

Indicates whether the authenticator supports large blob attestation.

### -field bResidentKey

Indicates whether the relying party requires a resident key.

## -remarks

The **pvAttestationDecode** depends on the **dwAttestationDecodeType**:

| **Decode type** | **Decode value** |
|----------|----------|
| **WEBAUTHN_ATTESTATION_DECODE_NONE** | **NULL** - not able to decode the CBOR attestation information |
| **WEBAUTHN_ATTESTATION_DECODE_COMMON** | **PWEBAUTHN_COMMON_ATTESTATION** |

## -see-also

[WebAuthNAuthenticatorMakeCredential](./nf-webauthn-webauthnauthenticatormakecredential.md)
