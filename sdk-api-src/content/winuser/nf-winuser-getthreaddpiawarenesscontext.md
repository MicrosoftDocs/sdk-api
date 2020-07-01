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
f1_keywords:
- winuser/GetThreadDpiAwarenessContext
dev_langs:
- c++
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: None supported
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- User32.dll
- Ext-MS-Win-NTUser-Window-l1-1-0.dll
- Ext-MS-Win-NTUser-Window-l1-1-1.dll
- Ext-MS-Win-NTUser-Window-l1-1-2.dll
- ext-ms-win-ntuser-window-l1-1-3.dll
- Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
- GetThreadDpiAwarenessContext
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetThreadDpiAwarenessContext function


## -description


Gets the <a href="https://docs.microsoft.com/windows/desktop/hidpi/dpi-awareness-context">DPI_AWARENESS_CONTEXT</a> for the current thread.


## -parameters






## -returns



The current <a href="https://docs.microsoft.com/windows/desktop/hidpi/dpi-awareness-context">DPI_AWARENESS_CONTEXT</a> for the thread.




## -remarks



This method will return the latest <a href="https://docs.microsoft.com/windows/desktop/hidpi/dpi-awareness-context">DPI_AWARENESS_CONTEXT</a> sent to <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext">SetThreadDpiAwarenessContext</a>. If <b>SetThreadDpiAwarenessContext</b> was never called for this thread, then the return value will equal the default <b>DPI_AWARENESS_CONTEXT</b> for the process.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/windef/ne-windef-dpi_awareness">DPI_AWARENESS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getawarenessfromdpiawarenesscontext">GetAwarenessFromDpiAwarenessContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext">SetThreadDpiAwarenessContext</a>
 

 

