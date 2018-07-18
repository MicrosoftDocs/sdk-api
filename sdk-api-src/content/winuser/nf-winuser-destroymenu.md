---
UID: NF:winuser.DestroyMenu
title: DestroyMenu function
author: windows-sdk-content
description: Destroys the specified menu and frees any memory that the menu occupies.
old-location: menurc\destroymenu.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\destroymenu.htm
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: DestroyMenu, DestroyMenu function [Menus and Other Resources], _win32_DestroyMenu, _win32_destroymenu_cpp, menurc.destroymenu, winui._win32_destroymenu, winuser/DestroyMenu
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
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
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



Before closing, an application must use the <b>DestroyMenu</b> function to destroy a menu not assigned to a window. A menu that is assigned to a window is automatically destroyed when the application closes.

<b>DestroyMenu</b> is recursive, that is, it will destroy the menu and all its submenus.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/library/ms647558(v=VS.85).aspx">Displaying a Shortcut Menu</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/library/ms647624(v=VS.85).aspx">CreateMenu</a>



<a href="https://msdn.microsoft.com/library/ms647629(v=VS.85).aspx">DeleteMenu</a>



<a href="https://msdn.microsoft.com/library/ms646977(v=VS.85).aspx">Menus</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/ms647994(v=VS.85).aspx">RemoveMenu</a>



<a href="https://msdn.microsoft.com/library/ms648001(v=VS.85).aspx">SetMenuItemInfo</a>
 

 

