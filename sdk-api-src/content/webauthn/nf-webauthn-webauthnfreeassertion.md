---
UID: NF:webauthn.WebAuthNFreeAssertion
tech.root: webauthn
title: WebAuthNFreeAssertion
ms.date: 07/19/2022
targetos: Windows
description: Frees a previously allocated WebAuthN assertion.
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
 - WebAuthNFreeAssertion
f1_keywords:
 - WebAuthNFreeAssertion
 - webauthn/WebAuthNFreeAssertion
dev_langs:
 - c++
helpviewer_keywords:
 - WebAuthNFreeAssertion
---

## -description

Frees an assertion previously allocated by calling [WebAuthNAuthenticatorGetAssertion](./nf-webauthn-webauthnauthenticatorgetassertion.md).

## -parameters

### -param pWebAuthNAssertion

The **WEBAUTHN_ASSERTION** to be freed.

## -remarks

## -see-also

[WebAuthNAuthenticatorGetAssertion](./nf-webauthn-webauthnauthenticatorgetassertion.md)

[WEBAUTHN_ASSERTION](./ns-webauthn-webauthn_assertion.md)
