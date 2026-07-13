---
UID: NF:webauthn.WebAuthNCancelCurrentOperation
tech.root: webauthn
title: WebAuthNCancelCurrentOperation
ms.date: 07/18/2022
targetos: Windows
description: Terminates operation currently in progress in the authenticator session.
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
 - WebAuthNCancelCurrentOperation
f1_keywords:
 - WebAuthNCancelCurrentOperation
 - webauthn/WebAuthNCancelCurrentOperation
dev_langs:
 - c++
helpviewer_keywords:
 - WebAuthNCancelCurrentOperation
---

## -description

When this operation is invoked by the client in an authenticator session, it has the effect of terminating any [WebAuthNAuthenticatorMakeCredential](./nf-webauthn-webauthnauthenticatormakecredential.md) or [WebAuthNAuthenticatorGetAssertion](./nf-webauthn-webauthnauthenticatorgetassertion.md) operation currently in progress in that authenticator session. The authenticator stops prompting for, or accepting, any user input related to authorizing the canceled operation. The client ignores any further responses from the authenticator for the canceled operation.

## -parameters

### -param pCancellationId

The **GUID** returned, representing the ID of the cancelled operation.

## -returns

Returns an **HRESULT** indicating success or failure.

## -remarks

This operation is ignored if it is invoked in an authenticator session which does not have an **WebAuthNAuthenticatorMakeCredential** or **WebAuthNAuthenticatorGetAssertion** operation currently in progress.

## -see-also

[WebAuthNGetCancellationId](./nf-webauthn-webauthngetcancellationid.md)

[WebAuthNAuthenticatorMakeCredential](./nf-webauthn-webauthnauthenticatormakecredential.md)

[WebAuthNAuthenticatorGetAssertion](./nf-webauthn-webauthnauthenticatorgetassertion.md)
