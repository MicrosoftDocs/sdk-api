---
UID: NF:sspi.SspiSetAsyncNotifyCallback
title: SspiSetAsyncNotifyCallback function
ms.date: 11/4/2019
targetos: Windows
description: Registers a callback that is notified on async call completion.
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
 - SspiSetAsyncNotifyCallback
f1_keywords:
 - SspiSetAsyncNotifyCallback
 - sspi/SspiSetAsyncNotifyCallback
dev_langs:
 - c++
---

# SspiSetAsyncNotifyCallback function


## -description

Registers a callback that is notified on async call completion.

## -parameters

### -param Context

The async call context.

### -param Callback

The SspiAsyncNotifyCallback that will be notified on call completion.

### -param CallbackData

An opaque pointer that is passed to [SspiAsyncNotifyCallback](nc-sspi-sspiasyncnotifycallback.md).

## -returns

## -remarks

The *Callback* and *CallbackData* parameters can be set to **null** in order to specify that the caller is not interested in the result of the operation. 

> [!NOTE]
> Setting the callback to null is only supported for [SspiDeleteSecurityContextAsync](nf-sspi-sspideletesecuritycontextasync.md)

## -see-also

[SspiAsyncNotifyCallback](nc-sspi-sspiasyncnotifycallback.md)

