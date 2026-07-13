---
UID: NF:webauthn.WebAuthNFreeCredentialAttestation
tech.root: webauthn
title: WebAuthNFreeCredentialAttestation
ms.date: 07/19/2022
targetos: Windows
description: Frees a previously allocated credential attestation.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: webauthn.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: OneCoreUAP.Lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - WebAuthn.dll
api_name:
 - WebAuthNFreeCredentialAttestation
f1_keywords:
 - WebAuthNFreeCredentialAttestation
 - webauthn/WebAuthNFreeCredentialAttestation
dev_langs:
 - c++
helpviewer_keywords:
 - WebAuthNFreeCredentialAttestation
---

## -description

Frees a **WEBAUTHN_CREDENTIAL_ATTESTATION** previously allocated by calling [WebAuthNAuthenticatorMakeCredential](./nf-webauthn-webauthnauthenticatormakecredential.md).

## -parameters

### -param pWebAuthNCredentialAttestation

The credential attestation to be freed.

## -remarks

## -see-also

[WebAuthNAuthenticatorMakeCredential](./nf-webauthn-webauthnauthenticatormakecredential.md)

[WEBAUTHN_CREDENTIAL_ATTESTATION](./ns-webauthn-webauthn_credential_attestation.md)
