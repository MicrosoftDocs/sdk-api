---
UID: NF:webauthn.WebAuthNIsUserVerifyingPlatformAuthenticatorAvailable
tech.root: webauthn
title: WebAuthNIsUserVerifyingPlatformAuthenticatorAvailable
ms.date: 07/19/2022
targetos: Windows
description: Determines if the platform authenticator service is available.
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
 - WebAuthNIsUserVerifyingPlatformAuthenticatorAvailable
f1_keywords:
 - WebAuthNIsUserVerifyingPlatformAuthenticatorAvailable
 - webauthn/WebAuthNIsUserVerifyingPlatformAuthenticatorAvailable
dev_langs:
 - c++
helpviewer_keywords:
 - WebAuthNIsUserVerifyingPlatformAuthenticatorAvailable
---

## -description

Determines whether the platform authenticator service is available.

## -parameters

### -param pbIsUserVerifyingPlatformAuthenticatorAvailable

A pointer to a **BOOL** that is set to **TRUE** if the authenticator service is available, or **FALSE** otherwise.

## -returns

AN **HRESULT** indicating success or failure of the operation.

## -remarks

## -see-also

[WebAuthNGetErrorName](./nf-webauthn-webauthngeterrorname.md)
