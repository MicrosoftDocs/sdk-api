---
UID: NF:winuser.GetMenu
title: GetMenu function (winuser.h)
description: Retrieves a handle to the menu assigned to the specified window.
helpviewer_keywords: ["GetMenu","GetMenu function [Menus and Other Resources]","_win32_GetMenu","_win32_getmenu_cpp","menurc.getmenu","winui._win32_getmenu","winuser/GetMenu"]
old-location: menurc\getmenu.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\getmenu.htm
ms.date: 12/05/2018
ms.keywords: GetMenu, GetMenu function [Menus and Other Resources], _win32_GetMenu, _win32_getmenu_cpp, menurc.getmenu, winui._win32_getmenu, winuser/GetMenu
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
 - GetMenu
 - winuser/GetMenu
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-menu-l1-1-3.dll
 - ext-ms-win-ntuser-menu-l1-1-2.dll
 - ext-ms-win-ntuser-menu-l1-1-1.dll
 - ext-ms-win-ntuser-menu-l1-1-0.dll
 - User32.dll
api_name:
 - GetMenu
---

# GetMenu function


## -description

Retrieves a handle to the menu assigned to the specified window.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window whose menu handle is to be retrieved.

## -returns

Type: <b>HMENU</b>

The return value is a handle to the menu. If the specified window has no menu, the return value is <b>NULL</b>. If the window is a child window, the return value is undefined.

## -remarks

<b>GetMenu</b> does not work on floating menu bars. Floating menu bars are custom controls that mimic standard menus; they are not menus. To get the handle on a floating menu bar, use the <a href="/previous-versions/ms971350(v=msdn.10)">Active Accessibility</a> APIs.


#### Examples

For an example, see <a href="/windows/desktop/menurc/using-menus">Adding Lines and Graphs to a Menu</a>. 

<div class="code"></div>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getsubmenu">GetSubMenu</a>



<a href="/windows/desktop/menurc/menus">Menus</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setmenu">SetMenu</a>