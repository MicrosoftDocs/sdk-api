---
UID: NF:winuser.CloseWindow
title: CloseWindow function (winuser.h)
description: Minimizes (but does not destroy) the specified window.
helpviewer_keywords: ["CloseWindow","CloseWindow function [Windows and Messages]","_win32_CloseWindow","_win32_closewindow_cpp","winmsg.closewindow","winui._win32_closewindow","winuser/CloseWindow"]
old-location: winmsg\closewindow.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\closewindow.htm
ms.date: 12/05/2018
ms.keywords: CloseWindow, CloseWindow function [Windows and Messages], _win32_CloseWindow, _win32_closewindow_cpp, winmsg.closewindow, winui._win32_closewindow, winuser/CloseWindow
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
 - CloseWindow
 - winuser/CloseWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-window-l1-1-6.dll
 - ext-ms-win-ntuser-window-l1-1-5.dll
 - User32.dll
api_name:
 - CloseWindow
req.apiset: ext-ms-win-ntuser-window-l1-1-4 (introduced in Windows 10, version 10.0.14393)
---

# CloseWindow function


## -description

Minimizes (but does not destroy) the specified window.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window to be minimized.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To destroy a window, an application must use the <a href="/windows/desktop/api/winuser/nf-winuser-destroywindow">DestroyWindow</a> function.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-arrangeiconicwindows">ArrangeIconicWindows</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-destroywindow">DestroyWindow</a>



<a href="/windows/desktop/api/winuser/nf-winuser-isiconic">IsIconic</a>



<a href="/windows/desktop/api/winuser/nf-winuser-openicon">OpenIcon</a>



<b>Reference</b>



<a href="/windows/desktop/winmsg/windows">Windows</a>
