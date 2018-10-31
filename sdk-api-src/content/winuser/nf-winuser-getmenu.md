---
UID: NF:winuser.GetMenu
title: GetMenu function
author: windows-sdk-content
description: Retrieves a handle to the menu assigned to the specified window.
old-location: menurc\getmenu.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\getmenu.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetMenu, GetMenu function [Menus and Other Resources], _win32_GetMenu, _win32_getmenu_cpp, menurc.getmenu, winui._win32_getmenu, winuser/GetMenu
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
 - GetMenu
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



<b>GetMenu</b> does not work on floating menu bars. Floating menu bars are custom controls that mimic standard menus; they are not menus. To get the handle on a floating menu bar, use the <a href="https://msdn.microsoft.com/en-us/library/ms971350(v=MSDN.10).aspx">Active Accessibility</a> APIs.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/en-us/library/ms647558(v=VS.85).aspx">Adding Lines and Graphs to a Menu</a>. 

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms647984(v=VS.85).aspx">GetSubMenu</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646977(v=VS.85).aspx">Menus</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms647995(v=VS.85).aspx">SetMenu</a>
 

 

