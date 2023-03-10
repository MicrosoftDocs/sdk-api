---
UID: NF:sspi.SspiFreeCredentialsHandleAsync
title: SspiFreeCredentialsHandleAsync function
ms.date: 11/4/2019
targetos: Windows
description: Frees up a credential handle.
tech.root: security
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: sspi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 1607 [kernel-mode drivers only]
req.target-min-winversvr: Windows Server 2016 [kernel-mode drivers only]
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
api_location:
 - sspi.h
api_name:
 - SspiFreeCredentialsHandleAsync
f1_keywords:
 - SspiFreeCredentialsHandleAsync
 - sspi/SspiFreeCredentialsHandleAsync
dev_langs:
 - c++
---

## -description

Frees up a credential handle.

## -parameters

### -param AsyncContext

The async call context.

### -param phCredential

The credential handle to free.

## -returns

Returns **SEC_E_OK** if the async request to free the credential handle was successfully queued for execution. Otherwise, it returns the error generated attempting to queue it. To retrieve the status of the operation, use [SspiGetAsyncCallStatus](nf-sspi-sspigetasynccallstatus.md).

SspiGetAsyncCallStatus returns **SEC_E_OK** on completion. Otherwise, it may return **SEC_I_ASYNC_CALL_PENDING** if the call is still in progress.

## -remarks

## -see-also

[FreeCredentialsHandle](nf-sspi-freecredentialshandle.md)

