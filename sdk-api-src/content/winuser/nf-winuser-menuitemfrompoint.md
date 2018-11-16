---
UID: NF:winuser.MenuItemFromPoint
title: MenuItemFromPoint function
author: windows-sdk-content
description: Determines which menu item, if any, is at the specified location.
old-location: menurc\menuitemfrompoint.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\menuitemfrompoint.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: MenuItemFromPoint, MenuItemFromPoint function [Menus and Other Resources], _win32_MenuItemFromPoint, _win32_menuitemfrompoint_cpp, menurc.menuitemfrompoint, winui._win32_menuitemfrompoint, winuser/MenuItemFromPoint
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
 - MenuItemFromPoint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- MenuItemFromPoint
: 
---

# MenuItemFromPoint function


## -description


Determines which menu item, if any, is at the specified location.


## -parameters




### -param hWnd [in, optional]

Type: <b>HWND</b>

A handle to the window containing the menu. If this value is <b>NULL</b> and the <i>hMenu</i> parameter represents a popup menu, the function will find the menu window. 


### -param hMenu [in]

Type: <b>HMENU</b>

A handle to the menu containing the menu items to hit test. 


### -param ptScreen [in]

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a></b>

A structure that specifies the location to test. If <i>hMenu</i> specifies a menu bar, this parameter is in window coordinates. Otherwise, it is in client coordinates. 


## -returns



Type: <b>int</b>

Returns the zero-based position of the menu item at the specified location or -1 if no menu item is at the specified location.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms646977(v=VS.85).aspx">Menus</a>
 

 

