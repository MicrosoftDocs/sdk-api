---
UID: NF:winuser.CreateMenu
title: CreateMenu function (winuser.h)
description: Creates a menu. The menu is initially empty, but it can be filled with menu items by using the InsertMenuItem, AppendMenu, and InsertMenu functions.
helpviewer_keywords: ["CreateMenu","CreateMenu function [Menus and Other Resources]","_win32_CreateMenu","_win32_createmenu_cpp","menurc.createmenu","winui._win32_createmenu","winuser/CreateMenu"]
old-location: menurc\createmenu.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\createmenu.htm
ms.date: 12/05/2018
ms.keywords: CreateMenu, CreateMenu function [Menus and Other Resources], _win32_CreateMenu, _win32_createmenu_cpp, menurc.createmenu, winui._win32_createmenu, winuser/CreateMenu
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
 - CreateMenu
 - winuser/CreateMenu
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - ext-ms-win-ntuser-menu-l1-1-2.dll
 - Ext-MS-Win-NTUser-Menu-L1-1-3.dll
api_name:
 - CreateMenu
req.apiset: ext-ms-win-ntuser-menu-l1-1-2 (introduced in Windows 10, version 10.0.10240)
---

# CreateMenu function


## -description

Creates a menu. The menu is initially empty, but it can be filled with menu items by using the <a href="/windows/desktop/api/winuser/nf-winuser-insertmenuitema">InsertMenuItem</a>, <a href="/windows/desktop/api/winuser/nf-winuser-appendmenua">AppendMenu</a>, and <a href="/windows/desktop/api/winuser/nf-winuser-insertmenua">InsertMenu</a> functions.



## -returns

Type: <b>HMENU</b>

If the function succeeds, the return value is a handle to the newly created menu.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Resources associated with a menu that is assigned to a window are freed automatically. If the menu is not assigned to a window, an application must free system resources associated with the menu before closing. An application frees menu resources by calling the <a href="/windows/desktop/api/winuser/nf-winuser-destroymenu">DestroyMenu</a> function.

## -see-also

<a href="/windows/desktop/menurc/u">AppendMenu</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-createpopupmenu">CreatePopupMenu</a>



<a href="/windows/desktop/api/winuser/nf-winuser-destroymenu">DestroyMenu</a>



<a href="/windows/desktop/api/winuser/nf-winuser-insertmenua">InsertMenu</a>



<a href="/windows/desktop/api/winuser/nf-winuser-insertmenuitema">InsertMenuItem</a>



<a href="/windows/desktop/menurc/menus">Menus</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setmenu">SetMenu</a>
