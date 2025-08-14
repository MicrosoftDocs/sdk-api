---
UID: NF:winuser.DrawMenuBar
title: DrawMenuBar function (winuser.h)
description: Redraws the menu bar of the specified window. If the menu bar changes after the system has created the window, this function must be called to draw the changed menu bar.
helpviewer_keywords: ["DrawMenuBar","DrawMenuBar function [Menus and Other Resources]","_win32_DrawMenuBar","_win32_drawmenubar_cpp","menurc.drawmenubar","winui._win32_drawmenubar","winuser/DrawMenuBar"]
old-location: menurc\drawmenubar.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\drawmenubar.htm
ms.date: 12/05/2018
ms.keywords: DrawMenuBar, DrawMenuBar function [Menus and Other Resources], _win32_DrawMenuBar, _win32_drawmenubar_cpp, menurc.drawmenubar, winui._win32_drawmenubar, winuser/DrawMenuBar
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
 - DrawMenuBar
 - winuser/DrawMenuBar
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-misc-l1-7-0.dll
 - ext-ms-win-ntuser-misc-l1-6-0.dll
 - ext-ms-win-ntuser-misc-l1-5-1.dll
 - ext-ms-win-ntuser-misc-l1-5-0.dll
 - ext-ms-win-ntuser-misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-2-0.dll
 - ext-ms-win-ntuser-misc-l1-1-0.dll
 - User32.dll
api_name:
 - DrawMenuBar
---

# DrawMenuBar function


## -description

Redraws the menu bar of the specified window. If the menu bar changes after the system has created the window, this function must be called to draw the changed menu bar.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window whose menu bar is to be redrawn.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-deletemenu">DeleteMenu</a>



<a href="/windows/desktop/api/winuser/nf-winuser-insertmenuitema">InsertMenuItem</a>



<a href="/windows/desktop/menurc/menus">Menus</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-removemenu">RemoveMenu</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setmenuiteminfoa">SetMenuItemInfo</a>