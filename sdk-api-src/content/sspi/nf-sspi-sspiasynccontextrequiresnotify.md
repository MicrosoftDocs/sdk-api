---
UID: NF:sspi.SspiAsyncContextRequiresNotify
title: SspiAsyncContextRequiresNotify function
ms.date: 11/4/2019
targetos: Windows
description: Determines whether a given async context requires notification on completion of the call.
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
 - SspiAsyncContextRequiresNotify
f1_keywords:
 - SspiAsyncContextRequiresNotify
 - sspi/SspiAsyncContextRequiresNotify
dev_langs:
 - c++
---

## -description

Determines whether the given async context requires notification on completion of the call.

## -parameters

### -param AsyncContext

The async call context.

## -returns

Returns **True** if the async context requires notification on call completion. Otherwise, **False**.

## -remarks

## -see-also

