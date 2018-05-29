---
UID: NF:winuser.DestroyMenu
title: DestroyMenu function
author: windows-sdk-content
description: Destroys the specified menu and frees any memory that the menu occupies.
old-location: menurc\destroymenu.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\destroymenu.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
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
req.typenames: AR_STATE, *PAR_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	User32.dll
-	Ext-MS-Win-NTUser-Menu-l1-1-0.dll
-	Ext-MS-Win-NTUser-Menu-l1-1-1.dll
-	ext-ms-win-ntuser-menu-l1-1-2.dll
-	Ext-MS-Win-NTUser-Menu-L1-1-3.dll
api_name:
-	DestroyMenu
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

For an example, see <a href="using_menus.htm">Displaying a Shortcut Menu</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/dd7e59f6-7d31-46d3-9606-0f9346ff2979">CreateMenu</a>



<a href="https://msdn.microsoft.com/0054bf62-cb70-4d6e-805d-58206fa2d297">DeleteMenu</a>



<a href="https://msdn.microsoft.com/f00c0b76-fabb-4451-bd4e-30b465d4d235">Menus</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/9557d6dd-44a2-4c26-b939-8ae88b48956a">RemoveMenu</a>



<a href="https://msdn.microsoft.com/e1c669c7-7b56-428a-8433-d926330e42e1">SetMenuItemInfo</a>
 

 

