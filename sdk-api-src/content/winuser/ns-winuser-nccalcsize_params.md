---
UID: NS:winuser.tagNCCALCSIZE_PARAMS
title: NCCALCSIZE_PARAMS (winuser.h)
description: Contains information that an application can use while processing the WM_NCCALCSIZE message to calculate the size, position, and valid contents of the client area of a window.
helpviewer_keywords: ["*LPNCCALCSIZE_PARAMS","LPNCCALCSIZE_PARAMS","LPNCCALCSIZE_PARAMS structure pointer [Windows and Messages]","NCCALCSIZE_PARAMS","NCCALCSIZE_PARAMS structure [Windows and Messages]","_win32_NCCALCSIZE_PARAMS_str","_win32_nccalcsize_params_str_cpp","winmsg.nccalcsize_params","winui._win32_nccalcsize_params_str","winuser/LPNCCALCSIZE_PARAMS","winuser/NCCALCSIZE_PARAMS"]
old-location: winmsg\nccalcsize_params.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowstructures\nccalcsize_params.htm
ms.date: 12/05/2018
ms.keywords: '*LPNCCALCSIZE_PARAMS, LPNCCALCSIZE_PARAMS, LPNCCALCSIZE_PARAMS structure pointer [Windows and Messages], NCCALCSIZE_PARAMS, NCCALCSIZE_PARAMS structure [Windows and Messages], _win32_NCCALCSIZE_PARAMS_str, _win32_nccalcsize_params_str_cpp, winmsg.nccalcsize_params, winui._win32_nccalcsize_params_str, winuser/LPNCCALCSIZE_PARAMS, winuser/NCCALCSIZE_PARAMS'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NCCALCSIZE_PARAMS, *LPNCCALCSIZE_PARAMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNCCALCSIZE_PARAMS
 - winuser/tagNCCALCSIZE_PARAMS
 - LPNCCALCSIZE_PARAMS
 - winuser/LPNCCALCSIZE_PARAMS
 - NCCALCSIZE_PARAMS
 - winuser/NCCALCSIZE_PARAMS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - NCCALCSIZE_PARAMS
---

# NCCALCSIZE_PARAMS structure


## -description

Contains information that an application can use while processing the <a href="/windows/desktop/winmsg/wm-nccalcsize">WM_NCCALCSIZE</a> message to calculate the size, position, and valid contents of the client area of a window.

## -struct-fields

### -field rgrc

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>[3]</b>

An array of rectangles. The meaning of the array of rectangles changes during the processing of the <a href="/windows/desktop/winmsg/wm-nccalcsize">WM_NCCALCSIZE</a> message.

When the window procedure receives the <a href="/windows/desktop/winmsg/wm-nccalcsize">WM_NCCALCSIZE</a> message, the first rectangle contains the new coordinates of a window that has been moved or resized, that is, it is the proposed new window coordinates. The second contains the coordinates of the window before it was moved or resized. The third contains the coordinates of the window's client area before the window was moved or resized. If the window is a child window, the coordinates are relative to the client area of the parent window. If the window is a top-level window, the coordinates are relative to the screen origin.

When the window procedure returns, the first rectangle contains the coordinates of the new client rectangle resulting from the move or resize.  The second rectangle contains the valid destination rectangle, and the third rectangle contains the valid source rectangle.  The last two rectangles are used in conjunction with the return value of the <a href="/windows/desktop/winmsg/wm-nccalcsize">WM_NCCALCSIZE</a> message to determine the area of the window to be preserved.

### -field lppos

Type: <b>PWINDOWPOS</b>

A pointer to a <a href="/windows/desktop/api/winuser/ns-winuser-windowpos">WINDOWPOS</a> structure that contains the size and position values specified in the operation that moved or resized the window.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-movewindow">MoveWindow</a>



<b>Other Resources</b>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setwindowpos">SetWindowPos</a>



<a href="/windows/desktop/api/winuser/ns-winuser-windowpos">WINDOWPOS</a>



<a href="/windows/desktop/winmsg/wm-nccalcsize">WM_NCCALCSIZE</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>