---
UID: NS:webauthn._WEBAUTHN_AUTHENTICATOR_MAKE_CREDENTIAL_OPTIONS
tech.root: webauthn
title: WEBAUTHN_AUTHENTICATOR_MAKE_CREDENTIAL_OPTIONS
ms.date: 07/19/2022
targetos: Windows
description: The options for the WebAuthNAuthenticatorMakeCredential operation.
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
req.typenames: WEBAUTHN_AUTHENTICATOR_MAKE_CREDENTIAL_OPTIONS, *PWEBAUTHN_AUTHENTICATOR_MAKE_CREDENTIAL_OPTIONS
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - webauthn.h
api_name:
 - _WEBAUTHN_AUTHENTICATOR_MAKE_CREDENTIAL_OPTIONS
 - PWEBAUTHN_AUTHENTICATOR_MAKE_CREDENTIAL_OPTIONS
 - WEBAUTHN_AUTHENTICATOR_MAKE_CREDENTIAL_OPTIONS
f1_keywords:
 - _WEBAUTHN_AUTHENTICATOR_MAKE_CREDENTIAL_OPTIONS
 - webauthn/_WEBAUTHN_AUTHENTICATOR_MAKE_CREDENTIAL_OPTIONS
 - PWEBAUTHN_AUTHENTICATOR_MAKE_CREDENTIAL_OPTIONS
 - webauthn/PWEBAUTHN_AUTHENTICATOR_MAKE_CREDENTIAL_OPTIONS
 - WEBAUTHN_AUTHENTICATOR_MAKE_CREDENTIAL_OPTIONS
 - webauthn/WEBAUTHN_AUTHENTICATOR_MAKE_CREDENTIAL_OPTIONS
dev_langs:
 - c++
helpviewer_keywords:
 - _WEBAUTHN_AUTHENTICATOR_MAKE_CREDENTIAL_OPTIONS
---

## -description

The options for the [WebAuthNAuthenticatorMakeCredential](./nf-webauthn-webauthnauthenticatormakecredential.md) operation.

## -struct-fields

### -field dwVersion

Version of this structure.

### -field dwTimeoutMilliseconds

Time that the operation is expected to complete within. This is used as guidance, and can be overridden by the platform.

### -field CredentialList

Credentials used for exclusion.

### -field Extensions

_Optional_ extensions to parse when performing the operation.

### -field dwAuthenticatorAttachment

_Optional_ platform vs cross-platform authenticators.

### -field bRequireResidentKey

Require key to be resident or not. This is _optional_ and defaults to **FALSE**.

### -field dwUserVerificationRequirement

The user verification requirement.

### -field dwAttestationConveyancePreference

The attestation conveyance preference.

### -field dwFlags

The flags (_reserved for future use_).

### -field pCancellationId

The _optional_ cancellation Id.  See [WebAuthNGetCancellationId](./nf-webauthn-webauthngetcancellationid.md) for more information.

### -field pExcludeCredentialList

The exclude credential list. If present, **CredentialList** will be ignored.

### -field dwEnterpriseAttestation

The enterprise attestation.

### -field dwLargeBlobSupport

The requested large blob support: **none**, **required** or **preferred**. User will receive **NTE_INVALID_PARAMETER** when large blob is set to **required** or **preferred** and **bRequireResidentKey** isn't set to **TRUE**.

### -field bPreferResidentKey

Prefer key to be resident. Optional parameter, defaulting to **FALSE**. When **TRUE**, overrides **bRequireResidentKey**.

### -field bBrowserInPrivateMode

Indicates whether the client is using in-private mode in the browser. An _optional_ parameter that defaults to **FALSE**.

## -remarks

## -see-also

[WebAuthNAuthenticatorMakeCredential](./nf-webauthn-webauthnauthenticatormakecredential.md)

[WebAuthNGetCancellationId](./nf-webauthn-webauthngetcancellationid.md)
