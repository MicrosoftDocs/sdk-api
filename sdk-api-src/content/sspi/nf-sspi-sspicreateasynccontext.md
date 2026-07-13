---
UID: NF:sspi.SspiCreateAsyncContext
title: SspiCreateAsyncContext function
ms.date: 11/4/2019
targetos: Windows
description: Creates an instance of SspiAsyncContext which is used to track the async call.
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
 - SspiCreateAsyncContext
f1_keywords:
 - SspiCreateAsyncContext
 - sspi/SspiCreateAsyncContext
dev_langs:
 - c++
---

## -description

Creates an instance of SspiAsyncContext that tracks the async call.



## -returns

Returns the initialized SspiAsyncContext.

## -remarks

When done, the caller must free the async context with [SspiFreeAsyncContext](nf-sspi-sspifreeasynccontext.md)

While the instance's lifetime is the single async operation, it can be reused by calling [SspiReinitAsyncContext](nf-sspi-sspireinitasynccontext.md) after the operation has completed.

## -see-also

[SspiFreeAsyncContext](nf-sspi-sspifreeasynccontext.md)

[SspiReinitAsyncContext](nf-sspi-sspireinitasynccontext.md)

