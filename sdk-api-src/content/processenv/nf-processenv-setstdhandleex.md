---
UID: NF:processenv.SetStdHandleEx
title: SetStdHandleEx
ms.date: 4/26/2019
ms.keywords: SetStdHandleEx
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: processenv.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - SetStdHandleEx
 - processenv/SetStdHandleEx
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - api-ms-win-core-processenvironment-l1-1-0.dll
api_name:
 - SetStdHandleEx
---

## -description

Sets the handle for the input, output, or error streams.

## -parameters

### -param nStdHandle

A DWORD indicating the stream for which the handle is being set.

### -param hHandle

The handle.

### -param phPrevValue

Optional. Receives the previous handle.

## -returns

Returns S_OK on success.

## -remarks

## -see-also

