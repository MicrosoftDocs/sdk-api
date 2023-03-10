---
UID: NF:winuser.DestroyMenu
title: DestroyMenu function (winuser.h)
description: Destroys the specified menu and frees any memory that the menu occupies.
helpviewer_keywords: ["DestroyMenu","DestroyMenu function [Menus and Other Resources]","_win32_DestroyMenu","_win32_destroymenu_cpp","menurc.destroymenu","winui._win32_destroymenu","winuser/DestroyMenu"]
old-location: menurc\destroymenu.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\destroymenu.htm
ms.date: 12/05/2018
ms.keywords: DestroyMenu, DestroyMenu function [Menus and Other Resources], _win32_DestroyMenu, _win32_destroymenu_cpp, menurc.destroymenu, winui._win32_destroymenu, winuser/DestroyMenu
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
 - DestroyMenu
 - winuser/DestroyMenu
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
 - DestroyMenu
req.apiset: ext-ms-win-ntuser-menu-l1-1-0 (introduced in Windows 8)
---

# DestroyMenu function


## -description

Destroys the specified menu and frees any memory that the menu occupies.

## -parameters

### -param hMenu [in]

Type: <b>HMENU</b>

A handle to the menu to be destroyed.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Before closing, an application must use the <b>DestroyMenu</b> function to destroy a menu not assigned to a window. A menu that is assigned to a window is automatically destroyed when the application closes.

<b>DestroyMenu</b> is recursive, that is, it will destroy the menu and all its submenus.


#### Examples

For an example, see <a href="/windows/desktop/menurc/using-menus">Displaying a Shortcut Menu</a>.

<div class="code"></div>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-createmenu">CreateMenu</a>



<a href="/windows/desktop/api/winuser/nf-winuser-deletemenu">DeleteMenu</a>



<a href="/windows/desktop/menurc/menus">Menus</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-removemenu">RemoveMenu</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setmenuiteminfoa">SetMenuItemInfo</a>
