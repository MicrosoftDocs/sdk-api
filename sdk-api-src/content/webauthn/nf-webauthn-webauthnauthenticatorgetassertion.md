---
UID: NF:webauthn.WebAuthNAuthenticatorGetAssertion
tech.root: webauthn
title: WebAuthNAuthenticatorGetAssertion
ms.date: 07/18/2022
targetos: Windows
description: Produces an assertion signature representing an assertion by the authenticator that the user has consented to a specific transaction.
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
 - WebAuthNAuthenticatorGetAssertion
f1_keywords:
 - WebAuthNAuthenticatorGetAssertion
 - webauthn/WebAuthNAuthenticatorGetAssertion
dev_langs:
 - c++
helpviewer_keywords:
 - WebAuthNAuthenticatorGetAssertion
---

## -description

Produces an assertion signature representing an assertion by the authenticator that the user has consented to a specific transaction, such as logging in or completing a purchase.

## -parameters

### -param hWnd

The handle for the window that will be used to display the UI.

### -param pwszRpId

The ID of the Relying Party.

### -param pWebAuthNClientData

The client data to be sent to the authenticator for the Relying Party.

### -param pWebAuthNGetAssertionOptions

The options for the **WebAuthNAuthenticatorGetAssertion** operation.

### -param ppWebAuthNAssertion

A pointer to a **WEBAUTHN_ASSERTION** that receives the assertion.

## -returns

Returns an **HRESULT** indicating success or failure.

## -remarks

> Note:
> Before performing this operation, all other operations in progress in the authenticator session MUST be aborted by running the [WebAuthNCancelCurrentOperation](./nf-webauthn-webauthncancelcurrentoperation.md) operation.

If the authenticator cannot find any credential corresponding to the specified Relying Party that matches the specified criteria, it terminates the operation and returns an error.

## -see-also

[WebAuthNCancelCurrentOperation](./nf-webauthn-webauthncancelcurrentoperation.md)

[WEBAUTHN_ASSERTION](./ns-webauthn-webauthn_assertion.md)
