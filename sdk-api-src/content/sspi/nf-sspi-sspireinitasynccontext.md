---
UID: NF:sspi.SspiReinitAsyncContext
title: SspiReinitAsyncContext function
ms.date: 11/4/2019
targetos: Windows
description: Marks an async context for reuse.
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
 - SspiReinitAsyncContext
f1_keywords:
 - SspiReinitAsyncContext
 - sspi/SspiReinitAsyncContext
dev_langs:
 - c++
---

## -description

Resets an async context so it can be reused.

## -parameters

### -param Handle

The async context handle.

## -returns

If the context is invalid or currently in use, an error will be returned.

## -remarks

Only the context state is altered. Client notification info, such as callback, is left alone.

## -see-also

