---
UID: NF:winuser.GetDpiFromDpiAwarenessContext
title: GetDpiFromDpiAwarenessContext function (winuser.h)
description: Retrieves the DPI from a given DPI_AWARENESS_CONTEXT handle. This enables you to determine the DPI of a thread without needed to examine a window created within that thread.
helpviewer_keywords: ["GetDpiFromDpiAwarenessContext","GetDpiFromDpiAwarenessContext function [High DPI]","hidpi.getdpifromdpiawarenesscontext","winuser/GetDpiFromDpiAwarenessContext"]
old-location: hidpi\getdpifromdpiawarenesscontext.htm
tech.root: hidpi
ms.assetid: E47A7A12-AE11-4E66-AE49-463C9F4A6330
ms.date: 12/05/2018
ms.keywords: GetDpiFromDpiAwarenessContext, GetDpiFromDpiAwarenessContext function [High DPI], hidpi.getdpifromdpiawarenesscontext, winuser/GetDpiFromDpiAwarenessContext
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetDpiFromDpiAwarenessContext
 - winuser/GetDpiFromDpiAwarenessContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - GetDpiFromDpiAwarenessContext
---

# GetDpiFromDpiAwarenessContext function


## -description

Retrieves the DPI from a given <a href="/windows/desktop/hidpi/dpi-awareness-context">DPI_AWARENESS_CONTEXT</a> handle. This enables you to determine the DPI of a thread without needed to examine a window created within that thread.

## -parameters

### -param value

The <b>DPI_AWARENESS_CONTEXT</b> handle to examine.

## -returns

The DPI value associated with the <b>DPI_AWARENESS_CONTEXT</b> handle.

## -remarks

<a href="/windows/desktop/hidpi/dpi-awareness-context">DPI_AWARENESS_CONTEXT</a> handles associated with values of <b>DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE</b> and <b>DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2</b> will return a value of 0 for their DPI. This is because the DPI of a per-monitor-aware window can change, and the actual DPI cannot be returned without the window's HWND.

## -see-also

<a href="/windows/desktop/hidpi/dpi-awareness-context">DPI_AWARENESS_CONTEXT</a>