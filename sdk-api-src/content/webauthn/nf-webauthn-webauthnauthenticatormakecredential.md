---
UID: NF:webauthn.WebAuthNAuthenticatorMakeCredential
tech.root: webauthn
title: WebAuthNAuthenticatorMakeCredential
ms.date: 07/18/2022
targetos: Windows
description: Creates a public key credential source bound to a managing authenticator and returns the credential public key associated with its credential private key.
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
 - WebAuthNAuthenticatorMakeCredential
f1_keywords:
 - WebAuthNAuthenticatorMakeCredential
 - webauthn/WebAuthNAuthenticatorMakeCredential
dev_langs:
 - c++
helpviewer_keywords:
 - WebAuthNAuthenticatorMakeCredential
---

## -description

The WebAuthNAuthenticatorMakeCredential operation creates a public key credential source bound to a managing authenticator and returns the credential public key associated with its credential private key. The Relying Party can use this credential public key to verify the authentication assertions created by this public key credential source.

## -parameters

### -param hWnd

The handle for the window that will be used to display the UI.

### -param pRpInformation

The Relying Party's **WEBAUTHN_RP_ENTITY_INFORMATION**.

### -param pUserInformation

The user account’s **WEBAUTHN_USER_ENTITY_INFORMATION**, containing the user handle given by the Relying Party.

### -param pPubKeyCredParams

A sequence of pairs of public key credential type and public key algorithms requested by the Relying Party. This sequence is ordered from most preferred to least preferred. The authenticator makes a best-effort to create the most preferred credential that it can.

### -param pWebAuthNClientData

The client data to be sent to the authenticator for the Relying Party.

### -param pWebAuthNMakeCredentialOptions

Provides the options to use when creating the public key credential source.

### -param ppWebAuthNCredentialAttestation

On successful completion of this operation, the authenticator returns the attestation object to the client.

## -returns

Returns an **HRESULT** indicating success or failure.

## -remarks

## -see-also

[WEBAUTHN_USER_ENTITY_INFORMATION](./ns-webauthn-webauthn_user_entity_information.md)

[WebAuthNGetPlatformCredentialList](./nf-webauthn-webauthngetplatformcredentiallist.md)
