---
UID: NF:winuser.SetWindowRgn
title: SetWindowRgn function (winuser.h)
description: The SetWindowRgn function sets the window region of a window.
helpviewer_keywords: ["SetWindowRgn","SetWindowRgn function [Windows GDI]","_win32_SetWindowRgn","gdi.setwindowrgn","winuser/SetWindowRgn"]
old-location: gdi\setwindowrgn.htm
tech.root: gdi
ms.assetid: 06209d0c-14f9-45ec-ae2c-9cc596b5bbaa
ms.date: 12/05/2018
ms.keywords: SetWindowRgn, SetWindowRgn function [Windows GDI], _win32_SetWindowRgn, gdi.setwindowrgn, winuser/SetWindowRgn
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - SetWindowRgn
 - winuser/SetWindowRgn
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-draw-l1-1-0.dll
 - user32.dll
 - Ext-MS-Win-NTUser-Draw-l1-1-0.dll
 - Ext-MS-Win-NTUser-Draw-l1-1-1.dll
 - ext-ms-win-ntuser-draw-l1-1-2.dll
api_name:
 - SetWindowRgn
req.apiset: ext-ms-win-ntuser-draw-l1-1-0 (introduced in Windows 8)
---

# SetWindowRgn function


## -description

The <b>SetWindowRgn</b> function sets the window region of a window. The window region determines the area within the window where the system permits drawing. The system does not display any portion of a window that lies outside of the window region

## -parameters

### -param hWnd [in]

A handle to the window whose window region is to be set.

### -param hRgn [in]

A handle to a region. The function sets the window region of the window to this region.

If <i>hRgn</i> is <b>NULL</b>, the function sets the window region to <b>NULL</b>.

### -param bRedraw [in]

Specifies whether the system redraws the window after setting the window region. If <i>bRedraw</i> is <b>TRUE</b>, the system does so; otherwise, it does not.

Typically, you set <i>bRedraw</i> to <b>TRUE</b> if the window is visible.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

When this function is called, the system sends the <a href="/windows/desktop/winmsg/wm-windowposchanging">WM_WINDOWPOSCHANGING</a> and <a href="/windows/desktop/winmsg/wm-windowposchanged">WM_WINDOWPOSCHANGED</a> messages to the window.

The coordinates of a window's window region are relative to the upper-left corner of the window, not the client area of the window.

<div class="alert"><b>Note</b>  If the window layout is right-to-left (RTL), the coordinates are relative to the upper-right corner of the window. See <a href="/windows/desktop/winmsg/window-features">Window Layout and Mirroring</a>.</div>
<div> </div>
After a successful call to <b>SetWindowRgn</b>, the system owns the region specified by the region handle <i>hRgn</i>. The system does not make a copy of the region. Thus, you should not make any further function calls with this region handle. In particular, do not delete this region handle. The system deletes the region handle when it no longer needed.

To obtain the window region of a window, call the <a href="/windows/desktop/api/winuser/nf-winuser-getwindowrgn">GetWindowRgn</a> function.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-getwindowrgn">GetWindowRgn</a>



<a href="/windows/desktop/gdi/painting-and-drawing-functions">Painting and Drawing Functions</a>



<a href="/windows/desktop/gdi/painting-and-drawing">Painting and Drawing Overview</a>



<a href="/windows/desktop/winmsg/wm-windowposchanging">WM_WINDOWPOSCHANGING</a>



<a href="/windows/desktop/winmsg/wm-windowposchanging">WM_WINDOWPOSCHANGED</a>
