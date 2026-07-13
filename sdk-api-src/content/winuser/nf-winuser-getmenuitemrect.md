---
UID: NF:winuser.GetMenuItemRect
title: GetMenuItemRect function (winuser.h)
description: Retrieves the bounding rectangle for the specified menu item.
helpviewer_keywords: ["GetMenuItemRect","GetMenuItemRect function [Menus and Other Resources]","_win32_GetMenuItemRect","_win32_getmenuitemrect_cpp","menurc.getmenuitemrect","winui._win32_getmenuitemrect","winuser/GetMenuItemRect"]
old-location: menurc\getmenuitemrect.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\getmenuitemrect.htm
ms.date: 12/05/2018
ms.keywords: GetMenuItemRect, GetMenuItemRect function [Menus and Other Resources], _win32_GetMenuItemRect, _win32_getmenuitemrect_cpp, menurc.getmenuitemrect, winui._win32_getmenuitemrect, winuser/GetMenuItemRect
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
 - GetMenuItemRect
 - winuser/GetMenuItemRect
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
 - GetMenuItemRect
---

# GetMenuItemRect function


## -description

Retrieves the bounding rectangle 
		for the specified menu item.

## -parameters

### -param hWnd [in, optional]

Type: <b>HWND</b>

A handle to the window containing the menu.

If this value is <b>NULL</b> and the <i>hMenu</i> 
						parameter represents a popup menu, the function will find the menu window.

### -param hMenu [in]

Type: <b>HMENU</b>

A handle to a menu.

### -param uItem [in]

Type: <b>UINT</b>

The zero-based position of the menu item.

### -param lprcItem [out]

Type: <b>LPRECT</b>

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that receives the 
				bounding rectangle of the specified menu item expressed in screen coordinates.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error 
					information, use the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

In order for the returned rectangle to be meaningful, the menu must be popped 
		up if a popup menu or attached to a window if a menu bar. Menu item positions are not 
		determined until the menu is displayed.

## -see-also

<a href="/windows/desktop/menurc/menus">Menus</a>