---
UID: NF:webauthn.WebAuthNGetCancellationId
tech.root: webauthn
title: WebAuthNGetCancellationId
ms.date: 07/19/2022
targetos: Windows
description: Gets the cancellation ID for a canceled operation.
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
 - WebAuthNGetCancellationId
f1_keywords:
 - WebAuthNGetCancellationId
 - webauthn/WebAuthNGetCancellationId
dev_langs:
 - c++
helpviewer_keywords:
 - WebAuthNGetCancellationId
---

## -description

Gets the cancellation ID for the canceled operation.

## -parameters

### -param pCancellationId

The **GUID** returned, representing the ID of the cancelled operation.

## -returns

An **HRESULT** indicating success or failure.

## -remarks

## -see-also

[WebAuthNCancelCurrentOperation](./nf-webauthn-webauthncancelcurrentoperation.md)

[WebAuthNGetErrorName](./nf-webauthn-webauthngeterrorname.md)
