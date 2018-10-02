---
UID: NF:winuser.GetMenuItemRect
title: GetMenuItemRect function
author: windows-sdk-content
description: Retrieves the bounding rectangle for the specified menu item.
old-location: menurc\getmenuitemrect.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\getmenuitemrect.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetMenuItemRect, GetMenuItemRect function [Menus and Other Resources], _win32_GetMenuItemRect, _win32_getmenuitemrect_cpp, menurc.getmenuitemrect, winui._win32_getmenuitemrect, winuser/GetMenuItemRect
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - GetMenuItemRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that receives the 
				bounding rectangle of the specified menu item expressed in screen coordinates. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error 
					information, use the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -remarks



In order for the returned rectangle to be meaningful, the menu must be popped 
		up if a popup menu or attached to a window if a menu bar. Menu item positions are not 
		determined until the menu is displayed.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms646977(v=VS.85).aspx">Menus</a>
 

 

