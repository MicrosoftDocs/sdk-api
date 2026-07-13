---
UID: NF:webauthn.WebAuthNGetErrorName
tech.root: webauthn
title: WebAuthNGetErrorName
ms.date: 07/19/2022
targetos: Windows
description: Gets the error name for an error code.
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
 - WebAuthNGetErrorName
f1_keywords:
 - WebAuthNGetErrorName
 - webauthn/WebAuthNGetErrorName
dev_langs:
 - c++
helpviewer_keywords:
 - WebAuthNGetErrorName
---

## -description

Gets the error name for the specified error code.

## -parameters

### -param hr

The **HRESULT** to get the error name for.

## -returns

An error name string.

## -remarks

Returns the following error codes:

| Error Code | Error Name |
|------------|------------|
| **S_OK** | Success |
| **NTE_EXISTS** | InvalidStateError |
| **HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)**<br>**NTE_NOT_SUPPORTED**<br>**NTE_TOKEN_KEYSET_STORAGE_FULL** | ConstraintError |
| **NTE_INVALID_PARAMETER** | NotSupporedError |
| **NTE_DEVICE_NOT_FOUND**<br>**NTE_NOT_FOUND**<br>**HRESULT_FROM_WIN32(ERROR_CANCELLED)**<br>**NTE_USER_CANCELLED**<br>**HRESULT_FROM_WIN32(ERROR_TIMEOUT)** | NotAllowedError |
| All other **HRESULT** values | UnknownError |

## -see-also

[WebAuthNGetW3CExceptionDOMError](./nf-webauthn-webauthngetw3cexceptiondomerror.md)
