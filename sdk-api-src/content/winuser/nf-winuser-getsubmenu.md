---
UID: NF:winuser.GetSubMenu
title: GetSubMenu function (winuser.h)
description: Retrieves a handle to the drop-down menu or submenu activated by the specified menu item.
helpviewer_keywords: ["GetSubMenu","GetSubMenu function [Menus and Other Resources]","_win32_GetSubMenu","_win32_getsubmenu_cpp","menurc.getsubmenu","winui._win32_getsubmenu","winuser/GetSubMenu"]
old-location: menurc\getsubmenu.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\getsubmenu.htm
ms.date: 12/05/2018
ms.keywords: GetSubMenu, GetSubMenu function [Menus and Other Resources], _win32_GetSubMenu, _win32_getsubmenu_cpp, menurc.getsubmenu, winui._win32_getsubmenu, winuser/GetSubMenu
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
 - GetSubMenu
 - winuser/GetSubMenu
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-Menu-l1-1-0.dll
 - Ext-MS-Win-NTUser-Menu-l1-1-1.dll
 - ext-ms-win-ntuser-menu-l1-1-2.dll
 - Ext-MS-Win-NTUser-Menu-L1-1-3.dll
api_name:
 - GetSubMenu
req.apiset: ext-ms-win-ntuser-menu-l1-1-0 (introduced in Windows 8)
---

# GetSubMenu function


## -description

Retrieves a handle to the drop-down menu or submenu activated by the specified menu item.

## -parameters

### -param hMenu [in]

Type: <b>HMENU</b>

A handle to the menu.

### -param nPos [in]

Type: <b>int</b>

The zero-based relative position in the specified menu of an item that activates a drop-down menu or submenu.

## -returns

Type: <b>HMENU</b>

If the function succeeds, the return value is a handle to the drop-down menu or submenu activated by the menu item. If the menu item does not activate a drop-down menu or submenu, the return value is <b>NULL</b>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-createpopupmenu">CreatePopupMenu</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getmenu">GetMenu</a>



<a href="/windows/desktop/menurc/menus">Menus</a>



<b>Reference</b>
