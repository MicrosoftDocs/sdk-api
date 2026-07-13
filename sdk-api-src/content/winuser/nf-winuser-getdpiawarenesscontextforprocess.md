---
UID: NF:winuser.GetDpiAwarenessContextForProcess
tech.root: hidpi
title: GetDpiAwarenessContextForProcess
ms.date: 04/21/2023
targetos: Windows
description: Gets a DPI_AWARENESS_CONTEXT handle for the specified process.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: User32.dll
req.header: winuser.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: User32.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - user32.dll
api_name:
 - GetDpiAwarenessContextForProcess
f1_keywords:
 - GetDpiAwarenessContextForProcess
 - winuser/GetDpiAwarenessContextForProcess
dev_langs:
 - c++
helpviewer_keywords:
 - GetDpiAwarenessContextForProcess
---

## -description

Gets a <a href="/windows/desktop/hidpi/dpi-awareness-context">DPI_AWARENESS_CONTEXT</a> handle for the specified process.

## -parameters

### -param hProcess

A handle to the process for which the DPI awareness context is retrieved. If NULL is specified, the context is retrieved for the current process.  

## -returns

The **DPI_AWARENESS_CONTEXT** for the specified process.

## -remarks

## -see-also

