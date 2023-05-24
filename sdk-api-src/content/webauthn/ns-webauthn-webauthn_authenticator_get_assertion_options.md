---
UID: NS:webauthn._WEBAUTHN_AUTHENTICATOR_GET_ASSERTION_OPTIONS
tech.root: webauthn
title: WEBAUTHN_AUTHENTICATOR_GET_ASSERTION_OPTIONS
ms.date: 07/19/2022
targetos: Windows
description: A structure that contains the options to get an assertion.
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
req.typenames: WEBAUTHN_AUTHENTICATOR_GET_ASSERTION_OPTIONS, *PWEBAUTHN_AUTHENTICATOR_GET_ASSERTION_OPTIONS
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - webauthn.h
api_name:
 - _WEBAUTHN_AUTHENTICATOR_GET_ASSERTION_OPTIONS
 - PWEBAUTHN_AUTHENTICATOR_GET_ASSERTION_OPTIONS
 - WEBAUTHN_AUTHENTICATOR_GET_ASSERTION_OPTIONS
f1_keywords:
 - _WEBAUTHN_AUTHENTICATOR_GET_ASSERTION_OPTIONS
 - webauthn/_WEBAUTHN_AUTHENTICATOR_GET_ASSERTION_OPTIONS
 - PWEBAUTHN_AUTHENTICATOR_GET_ASSERTION_OPTIONS
 - webauthn/PWEBAUTHN_AUTHENTICATOR_GET_ASSERTION_OPTIONS
 - WEBAUTHN_AUTHENTICATOR_GET_ASSERTION_OPTIONS
 - webauthn/WEBAUTHN_AUTHENTICATOR_GET_ASSERTION_OPTIONS
dev_langs:
 - c++
helpviewer_keywords:
 - _WEBAUTHN_AUTHENTICATOR_GET_ASSERTION_OPTIONS
---

## -description

A structure that contains the data needed to get an assertion.

## -struct-fields

### -field dwVersion

The version of this structure.

### -field dwTimeoutMilliseconds

Time that the operation is expected to complete within. This is used as guidance and can be overridden by the platform.

### -field CredentialList

The list of allowed credentials to be used in the assertion.

### -field Extensions

A CBOR map from extension identifiers to their authenticator extension inputs, created by the client based on the extensions requested by the Relying Party. These are _optional_ extensions to parse when performing the operation.

### -field dwAuthenticatorAttachment

The attachment for the assertion. _Optional_ platform vs cross-platform authenticators.

### -field dwUserVerificationRequirement

The effective user verification requirement.

### -field dwFlags

The flags for the assertion.

### -field pwszU2fAppId

_Optional_ identifier for the U2F AppId. Converted to UTF8 before being hashed. Not lower-cased.

### -field pbU2fAppId

If this is non-NULL, then, set to **TRUE** if the **pwszU2fAppid** was used instead of **PCWSTR pwszRpId**.

### -field pCancellationId

_Optional_ cancellation Id. See [WebAuthNGetCancellationId](./nf-webauthn-webauthngetcancellationid.md) for more information.

### -field pAllowCredentialList

An _optional_ list of public key credential descriptors describing credentials acceptable to the Relying Party (possibly filtered by the client), if any. If present, **CredentialList** will be ignored.

### -field dwCredLargeBlobOperation

The large blob operation.

### -field cbCredLargeBlob

Size of **pbCredLargeBlob**.

### -field pbCredLargeBlob

A pointer to the large credential blob.

### -field pHmacSecretSaltValues

PRF values which will be converted into HMAC-SECRET values according to the WebAuthN Spec.

### -field bBrowserInPrivateMode

Indicates whether the client is using in-private mode in the browser. An _optional_ parameter that defaults to **FALSE**.

## -remarks

## -see-also

[WebAuthNAuthenticatorGetAssertion](./nf-webauthn-webauthnauthenticatorgetassertion.md)

[WEBAUTHN_HMAC_SECRET_SALT_VALUES](./ns-webauthn-webauthn_hmac_secret_salt_values.md)
