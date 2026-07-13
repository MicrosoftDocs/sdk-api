---
UID: NF:sspi.SspiDeleteSecurityContextAsync
title: SspiDeleteSecurityContextAsync function
ms.date: 11/4/2019
targetos: Windows
description: Deletes the local data structures associated with the specified security context initiated by a previous call to the SspiInitializeSecurityContextAsync function or the SspiAcceptSecurityContextAsync function.
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
 - SspiDeleteSecurityContextAsync
f1_keywords:
 - SspiDeleteSecurityContextAsync
 - sspi/SspiDeleteSecurityContextAsync
dev_langs:
 - c++
---

## -description

The **SspiDeleteSecurityContextAsync** function deletes the local data structures associated with the specified [security context](/windows/desktop/SecGloss/s-gly) initiated by a previous call to the [SspiInitializeSecurityContextAsync](nf-sspi-sspiinitializesecuritycontextasynca.md) function or the [SspiAcceptSecurityContextAsync](nf-sspi-sspiacceptsecuritycontextasync.md) function.

## -parameters

### -param AsyncContext

The async call context.

### -param phContext

Handle of the security context to delete.

## -returns

Returns **SEC_E_OK** if the async request to delete the security context was successfully queued for execution. Otherwise, it returns the error generated attempting to queue it. To retrieve the status of the operation, use [SspiGetAsyncCallStatus](nf-sspi-sspigetasynccallstatus.md).

SspiGetAsyncCallStatus returns **SEC_E_OK** on completion. Otherwise, it may return **SEC_I_ASYNC_CALL_PENDING** if the call is still in progress, or one of the error codes below.

|<div>Return code</div>|<div>Description</div>|
|---|---|
|**SEC_E_INVALID_HANDLE**|The handle passed to the function is not valid.|

## -remarks

On async call completion, callers can choose to opt out of receiving a notification by avoiding setting a callback for a new SspiAsyncContext or by removing the callback using [SspiSetAsyncNotifyCallback](nf-sspi-sspisetasyncnotifycallback.md) with a null parameter. If opting out, the caller should free the context with [SspiFreeAsyncContext](nf-sspi-sspifreeasynccontext.md) immediately after calling SspiDeleteSecurityContextAsync, unless the context is intended for reuse.

The **SspiDeleteSecurityContextAsync** function terminates a security context and frees associated resources.

The caller must call this function for a security context when that security context is no longer needed. This is true if the security context is partial, incomplete, rejected, or failed. After the security context is successfully deleted, further use of that security context is not permitted and the handle is no longer valid.

## -see-also

[DeleteSecurityContext](nf-sspi-deletesecuritycontext.md)

[SspiAcceptSecurityContextAsync](nf-sspi-sspiacceptsecuritycontextasync.md)

[SspiFreeAsyncContext](nf-sspi-sspifreeasynccontext.md)

[SspiInitializeSecurityContextAsync](nf-sspi-sspiinitializesecuritycontextasynca.md)

[SspiSetAsyncNotifyCallback](nf-sspi-sspisetasyncnotifycallback.md)

[SSPI Functions](/windows/desktop/SecAuthN/authentication-functions)

