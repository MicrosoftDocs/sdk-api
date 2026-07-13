---
UID: NF:winuser.GetThreadDpiAwarenessContext
title: GetThreadDpiAwarenessContext function (winuser.h)
description: Gets the DPI_AWARENESS_CONTEXT for the current thread.
helpviewer_keywords: ["GetThreadDpiAwarenessContext","GetThreadDpiAwarenessContext function [High DPI]","hidpi.getthreaddpiawarenesscontext","winuser/GetThreadDpiAwarenessContext"]
old-location: hidpi\getthreaddpiawarenesscontext.htm
tech.root: hidpi
ms.assetid: DE86D551-974F-4A03-BDBE-348592CAB81F
ms.date: 12/05/2018
ms.keywords: GetThreadDpiAwarenessContext, GetThreadDpiAwarenessContext function [High DPI], hidpi.getthreaddpiawarenesscontext, winuser/GetThreadDpiAwarenessContext
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
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
 - GetThreadDpiAwarenessContext
 - winuser/GetThreadDpiAwarenessContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-dpi-l1-2-2.dll
 - ext-ms-win-rtcore-ntuser-dpi-l1-2-1.dll
 - ext-ms-win-rtcore-ntuser-dpi-l1-2-0.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - GetThreadDpiAwarenessContext
---

# GetThreadDpiAwarenessContext function


## -description

Gets the <a href="/windows/desktop/hidpi/dpi-awareness-context">DPI_AWARENESS_CONTEXT</a> for the current thread.



## -returns

The current <a href="/windows/desktop/hidpi/dpi-awareness-context">DPI_AWARENESS_CONTEXT</a> for the thread.

## -remarks

This method will return the latest <a href="/windows/desktop/hidpi/dpi-awareness-context">DPI_AWARENESS_CONTEXT</a> sent to <a href="/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext">SetThreadDpiAwarenessContext</a>. If <b>SetThreadDpiAwarenessContext</b> was never called for this thread, then the return value will equal the default <b>DPI_AWARENESS_CONTEXT</b> for the process.

## -see-also

<a href="/windows/desktop/api/windef/ne-windef-dpi_awareness">DPI_AWARENESS</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getawarenessfromdpiawarenesscontext">GetAwarenessFromDpiAwarenessContext</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext">SetThreadDpiAwarenessContext</a>
