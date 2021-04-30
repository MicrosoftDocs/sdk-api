---
UID: NC:sspi.SspiAsyncNotifyCallback
title: SspiAsyncNotifyCallback function
ms.date: 11/4/2019
targetos: Windows
description: Callback used for notifying completion of an async SSPI call.
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
req.target-type: 
req.target-min-winverclnt: Windows 10, version 1607 [kernel-mode drivers only]
req.target-min-winversvr: Windows Server 2016 [kernel-mode drivers only]
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - sspi.h
api_name:
 - SspiAsyncNotifyCallback
f1_keywords:
 - SspiAsyncNotifyCallback
 - sspi/SspiAsyncNotifyCallback
dev_langs:
 - c++
---

# SspiAsyncNotifyCallback function


## -description

Callback used for notifying completion of an async SSPI call.

## -parameters

### -param Handle

The async context handle.

### -param CallbackData

Receives the callback data passed by the [SspiSetAsyncNotifyCallback](nf-sspi-sspisetasyncnotifycallback.md) function as "PVOID CallbackData".

## -remarks

## -see-also

[SspiSetAsyncNotifyCallback](nf-sspi-sspisetasyncnotifycallback.md)

