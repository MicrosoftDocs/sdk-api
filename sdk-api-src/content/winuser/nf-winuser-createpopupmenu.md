---
UID: NF:winuser.CreatePopupMenu
title: CreatePopupMenu function
author: windows-sdk-content
description: Creates a drop-down menu, submenu, or shortcut menu.
old-location: menurc\createpopupmenu.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\createpopupmenu.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
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
---

# CreatePopupMenu function


## -description


Creates a drop-down menu, submenu, or shortcut menu. The menu is initially empty. You can insert or append menu items by using the <a href="https://msdn.microsoft.com/en-us/library/ms647988(v=VS.85).aspx">InsertMenuItem</a> function. You can also use the <a href="https://msdn.microsoft.com/en-us/library/ms647987(v=VS.85).aspx">InsertMenu</a> function to insert menu items and the <a href="https://msdn.microsoft.com/en-us/library/ms647616(v=VS.85).aspx">AppendMenu</a> function to append menu items.


## -parameters






## -returns



Type: <b>HMENU</b>

If the function succeeds, the return value is a handle to the newly created menu.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The application can add the new menu to an existing menu, or it can display a shortcut menu by calling the <a href="https://msdn.microsoft.com/en-us/library/ms648003(v=VS.85).aspx">TrackPopupMenuEx</a> or <a href="https://msdn.microsoft.com/en-us/library/ms648002(v=VS.85).aspx">TrackPopupMenu</a> functions. 

Resources associated with a menu that is assigned to a window are freed automatically. If the menu is not assigned to a window, an application must free system resources associated with the menu before closing. An application frees menu resources by calling the <a href="https://msdn.microsoft.com/en-us/library/ms647631(v=VS.85).aspx">DestroyMenu</a> function. 


#### Examples

For an example, see <a href="https://msdn.microsoft.com/en-us/library/ms647558(v=VS.85).aspx">Adding Lines and Graphs to a Menu</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms647616(v=VS.85).aspx">AppendMenu</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms647624(v=VS.85).aspx">CreateMenu</a>



<a href="https://msdn.microsoft.com/en-us/library/ms647631(v=VS.85).aspx">DestroyMenu</a>



<a href="https://msdn.microsoft.com/en-us/library/ms647987(v=VS.85).aspx">InsertMenu</a>



<a href="https://msdn.microsoft.com/en-us/library/ms647988(v=VS.85).aspx">InsertMenuItem</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646977(v=VS.85).aspx">Menus</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms647995(v=VS.85).aspx">SetMenu</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648002(v=VS.85).aspx">TrackPopupMenu</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648003(v=VS.85).aspx">TrackPopupMenuEx</a>
 

 

