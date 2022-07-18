---
UID: NF:webauthn.WebAuthNAuthenticatorGetAssertion
tech.root: 
title: WebAuthNAuthenticatorGetAssertion
ms.date: 
targetos: Windows
description: 
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
req.lib: 
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
 - 
api_location:
 - webauthn.h
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

## -parameters

### -param hWnd

### -param pwszRpId

### -param pWebAuthNClientData

### -param pWebAuthNGetAssertionOptions

### -param ppWebAuthNAssertion

## -returns

## -remarks

> Note:
> Before performing this operation, all other operations in progress in the authenticator session MUST be aborted by running the **WebAuthNCancelCurrentOperation** operation.

## -see-also
