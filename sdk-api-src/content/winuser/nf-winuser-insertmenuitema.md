---
UID: NF:winuser.InsertMenuItemA
title: InsertMenuItemA function
author: windows-sdk-content
description: Inserts a new menu item at the specified position in a menu.
old-location: menurc\insertmenuitem.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\insertmenuitem.htm
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: InsertMenuItem, InsertMenuItem function [Menus and Other Resources], InsertMenuItemA, InsertMenuItemW, _win32_InsertMenuItem, _win32_insertmenuitem_cpp, menurc.insertmenuitem, winui._win32_insertmenuitem, winuser/InsertMenuItem, winuser/InsertMenuItemA, winuser/InsertMenuItemW
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
req.unicode-ansi: InsertMenuItemW (Unicode) and InsertMenuItemA (ANSI)
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
 - Ext-MS-Win-NTUser-Menu-l1-1-1.dll
 - ext-ms-win-ntuser-menu-l1-1-2.dll
 - Ext-MS-Win-NTUser-Menu-L1-1-3.dll
api_name:
 - InsertMenuItem
 - InsertMenuItemA
 - InsertMenuItemW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# InsertMenuItemA function


## -description


Inserts a new menu item at the specified position in a menu.


## -parameters




### -param hmenu

TBD


### -param item

TBD


### -param fByPosition [in]

Type: <b>BOOL</b>

Controls the meaning of <i>uItem</i>. If this parameter is <b>FALSE</b>, <i>uItem</i> is a menu item identifier. Otherwise, it is a menu item position. See <a href="https://msdn.microsoft.com/library/ms647553(v=VS.85).aspx">Accessing Menu Items Programmatically</a> for more information.


### -param lpmi

TBD




#### - hMenu [in]

Type: <b>HMENU</b>

A handle to the menu in which the new menu item is inserted. 


#### - lpmii [in]

Type: <b>LPCMENUITEMINFO</b>

A pointer to a <a href="https://msdn.microsoft.com/library/ms647578(v=VS.85).aspx">MENUITEMINFO</a> structure that contains information about the new menu item. 


#### - uItem [in]

Type: <b>UINT</b>

The identifier or position of the menu item before which to insert the new item. The meaning of this parameter depends on the value of <i>fByPosition</i>. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, use the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -remarks



The application must call the <a href="https://msdn.microsoft.com/library/ms647633(v=VS.85).aspx">DrawMenuBar</a> function whenever a menu changes, whether the menu is in a displayed window.

In order for keyboard accelerators to work with bitmap or owner-drawn menu items, the owner of the menu must process the <a href="https://msdn.microsoft.com/library/ms646349(v=VS.85).aspx">WM_MENUCHAR</a> message. See <a href="https://msdn.microsoft.com/library/ms647558(v=VS.85).aspx">Owner-Drawn Menus and the WM_MENUCHAR Message</a> for more information.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/library/ms647558(v=VS.85).aspx">Example of Menu-Item Bitmaps</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/library/ms647633(v=VS.85).aspx">DrawMenuBar</a>



<a href="https://msdn.microsoft.com/library/ms647578(v=VS.85).aspx">MENUITEMINFO</a>



<a href="https://msdn.microsoft.com/library/ms646977(v=VS.85).aspx">Menus</a>



<b>Reference</b>
 

 

