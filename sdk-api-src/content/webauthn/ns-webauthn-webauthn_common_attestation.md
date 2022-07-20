---
UID: NS:webauthn._WEBAUTHN_COMMON_ATTESTATION
tech.root: webauthn
title: WEBAUTHN_COMMON_ATTESTATION
ms.date: 07/19/2022
targetos: Windows
description: The structure containing the common data for an attestation.
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
req.typenames: WEBAUTHN_COMMON_ATTESTATION, *PWEBAUTHN_COMMON_ATTESTATION
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - webauthn.h
api_name:
 - _WEBAUTHN_COMMON_ATTESTATION
 - PWEBAUTHN_COMMON_ATTESTATION
 - WEBAUTHN_COMMON_ATTESTATION
f1_keywords:
 - _WEBAUTHN_COMMON_ATTESTATION
 - webauthn/_WEBAUTHN_COMMON_ATTESTATION
 - PWEBAUTHN_COMMON_ATTESTATION
 - webauthn/PWEBAUTHN_COMMON_ATTESTATION
 - WEBAUTHN_COMMON_ATTESTATION
 - webauthn/WEBAUTHN_COMMON_ATTESTATION
dev_langs:
 - c++
helpviewer_keywords:
 - _WEBAUTHN_COMMON_ATTESTATION
---

## -description

The structure containing the common data for an attestation.

## -struct-fields

### -field dwVersion

Version of this structure, to allow for modifications in the future. This field is required and should be set to **CURRENT_VERSION**.

### -field pwszAlg

The hash and padding algorithm. This won't be set for _fido-u2f_ which assumes **"ES256"**.

### -field lAlg

The COSE algorithm identifier. This value is a number identifying a cryptographic algorithm. The algorithm identifiers _should_ be values registered in the [IANA COSE Algorithms registry](https://w3c.github.io/webauthn/#biblio-iana-cose-algs-reg), for instance, -7 for "ES256" and -257 for "RS256".

### -field cbSignature

The signature that was generated for this attestation.

### -field pbSignature

A pointer to the signature that was generated for this attestation.

### -field cX5c

Array of X.509 DER encoded certificates. The first certificate is the signer, leaf certificate. This is set for **Full Basic Attestation**. If not set, then this is a **Self Attestation**.

### -field pX5c

A pointer to the array of X.509 certificates.

### -field pwszVer

A pointer to the version of the attestation statement. (This is set for tpm.)

### -field cbCertInfo

The size of the certificate information. (This is set for tpm.)

### -field pbCertInfo

A pointer to the certificate information. (This is set for tpm.)

### -field cbPubArea

The size of the public key area. (This is set for tpm.)

### -field pbPubArea

A pointer to the public key area. (This is set for tpm.)

## -remarks

## -see-also

[WEBAUTHN_CREDENTIAL_ATTESTATION](./ns-webauthn-webauthn_credential_attestation.md)

[WEBAUTHN_X5C](./ns-webauthn-webauthn_x5c.md)
