---
UID: NF:webauthn.WebAuthNGetW3CExceptionDOMError
tech.root: webauthn
title: WebAuthNGetW3CExceptionDOMError
ms.date: 07/19/2022
targetos: Windows
description: Gets the W3C DOM error code for the last failed operation.
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
 - WebAuthNGetW3CExceptionDOMError
f1_keywords:
 - WebAuthNGetW3CExceptionDOMError
 - webauthn/WebAuthNGetW3CExceptionDOMError
dev_langs:
 - c++
helpviewer_keywords:
 - WebAuthNGetW3CExceptionDOMError
---

## -description

Gets the W3C DOM error code for the last failed operation in the authenticator session.

## -parameters

### -param hr

The **HRESULT** returned by the last failed operation in the session.

## -returns

An **HRESULT** with the failure status.

## -remarks

## -see-also

[WebAuthNGetErrorName](./nf-webauthn-webauthngeterrorname.md)
