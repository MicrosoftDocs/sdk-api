---
UID: NF:sspi.SspiGetAsyncCallStatus
title: SspiGetAsyncCallStatus function
ms.date: 11/4/2019
targetos: Windows
description: Gets the current status of an async call associated with the provided context.
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
 - SspiGetAsyncCallStatus
f1_keywords:
 - SspiGetAsyncCallStatus
 - sspi/SspiGetAsyncCallStatus
dev_langs:
 - c++
---

## -description

Gets the current status of an async call associated with the provided context.

## -parameters

### -param Handle

The async call context to get status for.

## -returns

When complete, returns the status of the async request. If the function succeeded, SspiGetAsyncCallStatus will return **SEC_E_OK**. Otherwise, refer to the respective API called to see return error codes and their respective descriptions.

Until the call is completed, status is **SEC_I_ASYNC_CALL_PENDING**.

## -remarks

## -see-also

[SspiAcceptSecurityContextAsync](nf-sspi-sspiacceptsecuritycontextasync.md)

[SspiAcquireCredentialsHandleAsyncA](nf-sspi-sspiacquirecredentialshandleasynca.md)

[SspiAcquireCredentialsHandleAsyncW](nf-sspi-sspiacquirecredentialshandleasyncw.md)

[SspiDeleteSecurityContextAsync](nf-sspi-sspideletesecuritycontextasync.md)

[SspiFreeAsyncContext](nf-sspi-sspifreeasynccontext.md)

[SspiFreeCredentialsHandleAsync](nf-sspi-sspifreecredentialshandleasync.md)

[SspiInitializeSecurityContextAsyncA](nf-sspi-sspiinitializesecuritycontextasynca.md)

[SspiInitializeSecurityContextAsyncW](nf-sspi-sspiinitializesecuritycontextasyncw.md)

