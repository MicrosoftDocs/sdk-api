---
UID: NF:winuser.GetWindowDpiAwarenessContext
title: GetWindowDpiAwarenessContext function (winuser.h)
description: Returns the DPI_AWARENESS_CONTEXT associated with a window.
helpviewer_keywords: ["GetWindowDpiAwarenessContext","GetWindowDpiAwarenessContext function [High DPI]","hidpi.getwindowdpiawarenesscontext","winuser/GetWindowDpiAwarenessContext"]
old-location: hidpi\getwindowdpiawarenesscontext.htm
tech.root: hidpi
ms.assetid: BCBC6EC7-9792-43C0-BE0E-D94F00A7CAFD
ms.date: 12/05/2018
ms.keywords: GetWindowDpiAwarenessContext, GetWindowDpiAwarenessContext function [High DPI], hidpi.getwindowdpiawarenesscontext, winuser/GetWindowDpiAwarenessContext
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
 - GetWindowDpiAwarenessContext
 - winuser/GetWindowDpiAwarenessContext
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
 - GetWindowDpiAwarenessContext
---

# GetWindowDpiAwarenessContext function


## -description

Returns the <a href="/windows/desktop/hidpi/dpi-awareness-context">DPI_AWARENESS_CONTEXT</a> associated with a window.

## -parameters

### -param hwnd [in]

The window to query.

## -returns

The <a href="/windows/desktop/hidpi/dpi-awareness-context">DPI_AWARENESS_CONTEXT</a> for the provided window. If the window is not valid, the return value is <b>NULL</b>.

## -remarks

<div class="alert"><b>Important</b>  <p class="note">The return value of <b>GetWindowDpiAwarenessContext</b> is not affected by the <a href="/windows/desktop/api/windef/ne-windef-dpi_awareness">DPI_AWARENESS</a> of the current thread. It only indicates the context of the window specified by the <i>hwnd</i> input parameter.

</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/windef/ne-windef-dpi_awareness">DPI_AWARENESS</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getawarenessfromdpiawarenesscontext">GetAwarenessFromDpiAwarenessContext</a>