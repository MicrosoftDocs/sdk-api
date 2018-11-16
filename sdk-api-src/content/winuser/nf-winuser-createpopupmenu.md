---
UID: NF:winuser.CreatePopupMenu
title: CreatePopupMenu function
author: windows-sdk-content
description: Creates a drop-down menu, submenu, or shortcut menu.
old-location: menurc\createpopupmenu.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\createpopupmenu.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CreatePopupMenu, CreatePopupMenu function [Menus and Other Resources], _win32_CreatePopupMenu, _win32_createpopupmenu_cpp, menurc.createpopupmenu, winui._win32_createpopupmenu, winuser/CreatePopupMenu
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
 - Ext-MS-Win-NTUser-Menu-l1-1-0.dll
 - Ext-MS-Win-NTUser-Menu-l1-1-1.dll
 - ext-ms-win-ntuser-menu-l1-1-2.dll
 - Ext-MS-Win-NTUser-Menu-L1-1-3.dll
api_name:
 - CreatePopupMenu
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CreatePopupMenu
: 
---

# CreatePopupMenu function


## -description


Creates a drop-down menu, submenu, or shortcut menu. The menu is initially empty. You can insert or append menu items by using the <a href="https://msdn.microsoft.com/be3819c2-8bdc-4a90-a188-ff8b4060eb8f">InsertMenuItem</a> function. You can also use the <a href="https://msdn.microsoft.com/8ca7510a-e035-4ba2-98dd-57d777cae814">InsertMenu</a> function to insert menu items and the <a href="https://msdn.microsoft.com/07da4d45-a816-40c1-a5c5-c7fbe954be57">AppendMenu</a> function to append menu items.


## -parameters






## -returns



Type: <b>HMENU</b>

If the function succeeds, the return value is a handle to the newly created menu.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The application can add the new menu to an existing menu, or it can display a shortcut menu by calling the <a href="https://msdn.microsoft.com/86b8f21b-0dfe-462e-a34a-c80ee5c1d185">TrackPopupMenuEx</a> or <a href="https://msdn.microsoft.com/2e1e4648-e3fd-4d9a-a558-de7b030e3d75">TrackPopupMenu</a> functions. 

Resources associated with a menu that is assigned to a window are freed automatically. If the menu is not assigned to a window, an application must free system resources associated with the menu before closing. An application frees menu resources by calling the <a href="https://msdn.microsoft.com/4fc9e332-09a6-4877-a831-e1128144530d">DestroyMenu</a> function. 


#### Examples

For an example, see <a href="using_menus.htm">Adding Lines and Graphs to a Menu</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/07da4d45-a816-40c1-a5c5-c7fbe954be57">AppendMenu</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/dd7e59f6-7d31-46d3-9606-0f9346ff2979">CreateMenu</a>



<a href="https://msdn.microsoft.com/4fc9e332-09a6-4877-a831-e1128144530d">DestroyMenu</a>



<a href="https://msdn.microsoft.com/8ca7510a-e035-4ba2-98dd-57d777cae814">InsertMenu</a>



<a href="https://msdn.microsoft.com/be3819c2-8bdc-4a90-a188-ff8b4060eb8f">InsertMenuItem</a>



<a href="https://msdn.microsoft.com/f00c0b76-fabb-4451-bd4e-30b465d4d235">Menus</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/86d61b87-99ad-45e1-bcff-af892b4bb51b">SetMenu</a>



<a href="https://msdn.microsoft.com/2e1e4648-e3fd-4d9a-a558-de7b030e3d75">TrackPopupMenu</a>



<a href="https://msdn.microsoft.com/86b8f21b-0dfe-462e-a34a-c80ee5c1d185">TrackPopupMenuEx</a>
 

 

