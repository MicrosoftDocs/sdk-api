---
UID: NF:webauthn.WebAuthNGetPlatformCredentialList
tech.root: webauthn
title: WebAuthNGetPlatformCredentialList
ms.date: 07/19/2022
targetos: Windows
description: Gets the list of stored credentials.
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
 - WebAuthNGetPlatformCredentialList
f1_keywords:
 - WebAuthNGetPlatformCredentialList
 - webauthn/WebAuthNGetPlatformCredentialList
dev_langs:
 - c++
helpviewer_keywords:
 - WebAuthNGetPlatformCredentialList
---

## -description

Gets the list of **WEBAUTHN_CREDENTIAL_DETAILS_LIST** currently stored for the user.

## -parameters

### -param pGetCredentialsOptions

The options for the operation.

### -param ppCredentialDetailsList

The credentials list returned by the operation.

## -returns

An **HRESULT** indicating success or failure.

## -remarks

## -see-also

[WEBAUTHN_CREDENTIAL_DETAILS_LIST](./ns-webauthn-webauthn_credential_details_list.md)

[WebAuthNFreePlatformCredentialList](./nf-webauthn-webauthnfreeplatformcredentiallist.md)
