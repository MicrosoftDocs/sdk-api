---
UID: NF:processenv.SetStdHandleEx
title: SetStdHandleEx
description: The SetStdHandleEx function (processenv.h) sets the handle for the input, output, or error streams.
ms.date: 08/05/2022
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
req.lib: kernel32.Lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - api-ms-win-core-processenvironment-l1-2-0.dll
 - api-ms-win-core-processenvironment-l1-1-0.dll
 - kernel32.dll
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

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## -remarks

## -see-also

