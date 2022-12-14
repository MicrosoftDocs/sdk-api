---
UID: NF:winuser.SetMenu
title: SetMenu function (winuser.h)
description: Assigns a new menu to the specified window.
helpviewer_keywords: ["SetMenu","SetMenu function [Menus and Other Resources]","_win32_SetMenu","_win32_setmenu_cpp","menurc.setmenu","winui._win32_setmenu","winuser/SetMenu"]
old-location: menurc\setmenu.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\setmenu.htm
ms.date: 12/05/2018
ms.keywords: SetMenu, SetMenu function [Menus and Other Resources], _win32_SetMenu, _win32_setmenu_cpp, menurc.setmenu, winui._win32_setmenu, winuser/SetMenu
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
 - SetMenu
 - winuser/SetMenu
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
 - SetMenu
req.apiset: ext-ms-win-ntuser-menu-l1-1-3 (introduced in Windows 10, version 10.0.14393)
---

# SetMenu function


## -description

Assigns a new menu to the specified window.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window to which the menu is to be assigned.

### -param hMenu [in, optional]

Type: <b>HMENU</b>

A handle to the new menu. If this parameter is <b>NULL</b>, the window's current menu is removed.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The window is redrawn to reflect the menu change. A menu can be assigned to any window that is not a child window.

The <b>SetMenu</b> function replaces the previous menu, if any, but it does not destroy it. An application should call the <a href="/windows/desktop/api/winuser/nf-winuser-destroymenu">DestroyMenu</a> function to accomplish this task.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-destroymenu">DestroyMenu</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getmenu">GetMenu</a>



<a href="/windows/desktop/menurc/menus">Menus</a>



<b>Reference</b>
