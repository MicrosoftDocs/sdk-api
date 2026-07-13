---
UID: NF:webauthn.WebAuthNDeletePlatformCredential
tech.root: webauthn
title: WebAuthNDeletePlatformCredential
ms.date: 07/19/2022
targetos: Windows
description: Removes a credential source stored on an authenticator.
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
 - WebAuthNDeletePlatformCredential
f1_keywords:
 - WebAuthNDeletePlatformCredential
 - webauthn/WebAuthNDeletePlatformCredential
dev_langs:
 - c++
helpviewer_keywords:
 - WebAuthNDeletePlatformCredential
---

## -description

Removes a Public Key Credential Source stored on a Virtual Authenticator.

## -parameters

### -param cbCredentialId

The ID of the credential to be removed.

### -param pbCredentialId

A pointer to the credential ID to be removed.

## -returns

Returns an **HRESULT** indicating success or failure.

## -remarks

## -see-also

[WebAuthNGetPlatformCredentialList](./nf-webauthn-webauthngetplatformcredentiallist.md)
