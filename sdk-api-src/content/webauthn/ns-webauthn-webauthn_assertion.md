---
UID: NS:webauthn._WEBAUTHN_ASSERTION
tech.root: webauthn
title: WEBAUTHN_ASSERTION
ms.date: 07/19/2022
targetos: Windows
description: A structure that contains the data necessary to verify an assertion.
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
req.typenames: WEBAUTHN_ASSERTION, *PWEBAUTHN_ASSERTION
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - webauthn.h
api_name:
 - _WEBAUTHN_ASSERTION
 - PWEBAUTHN_ASSERTION
 - WEBAUTHN_ASSERTION
f1_keywords:
 - _WEBAUTHN_ASSERTION
 - webauthn/_WEBAUTHN_ASSERTION
 - PWEBAUTHN_ASSERTION
 - webauthn/PWEBAUTHN_ASSERTION
 - WEBAUTHN_ASSERTION
 - webauthn/WEBAUTHN_ASSERTION
dev_langs:
 - c++
helpviewer_keywords:
 - _WEBAUTHN_ASSERTION
---

## -description

A structure that contains the data necessary to verify an assertion.

## -struct-fields

### -field dwVersion

The version of this structure.

### -field cbAuthenticatorData

The size of the authenticator data.

### -field pbAuthenticatorData

A pointer to the authenticator data.

### -field cbSignature

The size of the signature that was generated for this assertion.

### -field pbSignature

A pointer to the signature that was generated for this assertion.

### -field Credential

The credential that was used for this assertion.

### -field cbUserId

The size of the user Id.

### -field pbUserId

A pointer to the user Id.

### -field Extensions

A CBOR map from extension identifiers to their authenticator extension inputs, created by the client based on the extensions requested by the Relying Party, if any.

### -field cbCredLargeBlob

The size of **pbCredLargeBlob**.

### -field pbCredLargeBlob

A pointer to the credential blob.

### -field dwCredLargeBlobStatus

The status of the credential blob.

### -field pHmacSecret

A salt used to generate the HMAC secret.

## -remarks

## -see-also

[WebAuthNFreeAssertion](./nf-webauthn-webauthnfreeassertion.md)

[WebAuthNAuthenticatorGetAssertion](./nf-webauthn-webauthnauthenticatorgetassertion.md)
