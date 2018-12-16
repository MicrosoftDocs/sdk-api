---
UID: NF:winuser.SetMenu
title: SetMenu function
author: windows-sdk-content
description: Assigns a new menu to the specified window.
old-location: menurc\setmenu.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\setmenu.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SetMenu, SetMenu function [Menus and Other Resources], _win32_SetMenu, _win32_setmenu_cpp, menurc.setmenu, winui._win32_setmenu, winuser/SetMenu
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
 - SetMenu
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The window is redrawn to reflect the menu change. A menu can be assigned to any window that is not a child window.

The <b>SetMenu</b> function replaces the previous menu, if any, but it does not destroy it. An application should call the <a href="https://msdn.microsoft.com/en-us/library/ms647631(v=VS.85).aspx">DestroyMenu</a> function to accomplish this task. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms647631(v=VS.85).aspx">DestroyMenu</a>



<a href="https://msdn.microsoft.com/en-us/library/ms647640(v=VS.85).aspx">GetMenu</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646977(v=VS.85).aspx">Menus</a>



<b>Reference</b>
 

 

