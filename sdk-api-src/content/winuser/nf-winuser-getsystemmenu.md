---
UID: NF:winuser.GetSystemMenu
title: GetSystemMenu function (winuser.h)
description: Enables the application to access the window menu (also known as the system menu or the control menu) for copying and modifying.
helpviewer_keywords: ["GetSystemMenu","GetSystemMenu function [Menus and Other Resources]","_win32_GetSystemMenu","_win32_getsystemmenu_cpp","menurc.getsystemmenu","winui._win32_getsystemmenu","winuser/GetSystemMenu"]
old-location: menurc\getsystemmenu.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\getsystemmenu.htm
ms.date: 12/05/2018
ms.keywords: GetSystemMenu, GetSystemMenu function [Menus and Other Resources], _win32_GetSystemMenu, _win32_getsystemmenu_cpp, menurc.getsystemmenu, winui._win32_getsystemmenu, winuser/GetSystemMenu
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
 - GetSystemMenu
 - winuser/GetSystemMenu
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
 - GetSystemMenu
req.apiset: ext-ms-win-ntuser-menu-l1-1-0 (introduced in Windows 8)
---

# GetSystemMenu function


## -description

Enables the application to access the window menu (also known as the system menu or the control menu) for copying and modifying.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window that will own a copy of the window menu.

### -param bRevert [in]

Type: <b>BOOL</b>

The action to be taken. If this parameter is <b>FALSE</b>, <b>GetSystemMenu</b> returns a handle to the copy of the window menu currently in use. The copy is initially identical to the window menu, but it can be modified. If this parameter is <b>TRUE</b>, <b>GetSystemMenu</b> resets the window menu back to the default state. The previous window menu, if any, is destroyed.

## -returns

Type: <b>HMENU</b>

If the <i>bRevert</i> parameter is <b>FALSE</b>, the return value is a handle to a copy of the window menu. If the <i>bRevert</i> parameter is <b>TRUE</b>, the return value is <b>NULL</b>.

## -remarks

Any window that does not use the <b>GetSystemMenu</b> function to make its own copy of the window menu receives the standard window menu. 

The window menu initially contains items with various identifier values, such as <b>SC_CLOSE</b>, <b>SC_MOVE</b>, and <b>SC_SIZE</b>. 

Menu items on the window menu send <a href="/windows/desktop/menurc/wm-syscommand">WM_SYSCOMMAND</a> messages. 

All predefined window menu items have identifier numbers greater than 0xF000. If an application adds commands to the window menu, it should use identifier numbers less than 0xF000. 

The system automatically grays items on the standard window menu, depending on the situation. The application can perform its own checking or graying by responding to the <a href="/windows/desktop/menurc/wm-initmenu">WM_INITMENU</a> message that is sent before any menu is displayed.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getmenu">GetMenu</a>



<a href="/windows/desktop/api/winuser/nf-winuser-insertmenuitema">InsertMenuItem</a>



<a href="/windows/desktop/menurc/menus">Menus</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setmenuiteminfoa">SetMenuItemInfo</a>



<a href="/windows/desktop/menurc/wm-initmenu">WM_INITMENU</a>



<a href="/windows/desktop/menurc/wm-syscommand">WM_SYSCOMMAND</a>
