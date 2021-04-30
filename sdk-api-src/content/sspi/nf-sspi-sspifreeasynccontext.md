---
UID: NF:sspi.SspiFreeAsyncContext
title: SspiFreeAsyncContext function
ms.date: 11/4/2019
targetos: Windows
description: Frees up a context created in the call to the SspiCreateAsyncContext function.
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
 - SspiFreeAsyncContext
f1_keywords:
 - SspiFreeAsyncContext
 - sspi/SspiFreeAsyncContext
dev_langs:
 - c++
---

## -description

The **SspiFreeAsyncContext** function frees up a context created in the call to the [SspiCreateAsyncContext](nf-sspi-sspicreateasynccontext.md) function.

## -parameters

### -param Handle

The async call context to free.

## -remarks

For all operations that require notification of completion, SspiFreeAsyncContext must not be called until the async operation is complete and the callback has been invoked. Calling [SspiGetAsyncCallStatus](nf-sspi-sspigetasynccallstatus.md) will return status != SEC_I_ASYNC_CALL_PENDING to indicate the async operation has not completed.

## -see-also

[SspiCreateAsyncContext](nf-sspi-sspicreateasynccontext.md)

[SspiGetAsyncCallStatus](nf-sspi-sspigetasynccallstatus.md)

