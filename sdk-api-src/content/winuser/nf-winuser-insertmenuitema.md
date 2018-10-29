---
UID: NF:winuser.InsertMenuItemA
title: InsertMenuItemA function
author: windows-sdk-content
description: Inserts a new menu item at the specified position in a menu.
old-location: menurc\insertmenuitem.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\insertmenuitem.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: InsertMenuItem, InsertMenuItem function [Menus and Other Resources], InsertMenuItemA, InsertMenuItemW, _win32_InsertMenuItem, _win32_insertmenuitem_cpp, menurc.insertmenuitem, winui._win32_insertmenuitem, winuser/InsertMenuItem, winuser/InsertMenuItemA, winuser/InsertMenuItemW
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
req.unicode-ansi: InsertMenuItemW (Unicode) and InsertMenuItemA (ANSI)
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
 - Ext-MS-Win-NTUser-Menu-l1-1-1.dll
 - ext-ms-win-ntuser-menu-l1-1-2.dll
 - Ext-MS-Win-NTUser-Menu-L1-1-3.dll
api_name:
 - InsertMenuItem
 - InsertMenuItemA
 - InsertMenuItemW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# InsertMenuItemA function


## -description


Inserts a new menu item at the specified position in a menu.


## -parameters




### -param hmenu [in]

Type: <b>HMENU</b>

A handle to the menu in which the new menu item is inserted. 


### -param item [in]

Type: <b>UINT</b>

The identifier or position of the menu item before which to insert the new item. The meaning of this parameter depends on the value of <i>fByPosition</i>. 


### -param fByPosition [in]

Type: <b>BOOL</b>

Controls the meaning of <i>uItem</i>. If this parameter is <b>FALSE</b>, <i>uItem</i> is a menu item identifier. Otherwise, it is a menu item position. See <a href="about_menus.htm">Accessing Menu Items Programmatically</a> for more information.


### -param lpmi [in]

Type: <b>LPCMENUITEMINFO</b>

A pointer to a <a href="https://msdn.microsoft.com/43d30b39-c1e1-4711-97a2-b5bc29dad9df">MENUITEMINFO</a> structure that contains information about the new menu item. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, use the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -remarks



The application must call the <a href="https://msdn.microsoft.com/3b17db02-5059-4182-bd5b-2fb67eecd1d7">DrawMenuBar</a> function whenever a menu changes, whether the menu is in a displayed window.

In order for keyboard accelerators to work with bitmap or owner-drawn menu items, the owner of the menu must process the <a href="https://msdn.microsoft.com/de6c91bb-80fd-44b2-8d96-d016477a6547">WM_MENUCHAR</a> message. See <a href="using_menus.htm">Owner-Drawn Menus and the WM_MENUCHAR Message</a> for more information.


#### Examples

For an example, see <a href="using_menus.htm">Example of Menu-Item Bitmaps</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/3b17db02-5059-4182-bd5b-2fb67eecd1d7">DrawMenuBar</a>



<a href="https://msdn.microsoft.com/43d30b39-c1e1-4711-97a2-b5bc29dad9df">MENUITEMINFO</a>



<a href="https://msdn.microsoft.com/f00c0b76-fabb-4451-bd4e-30b465d4d235">Menus</a>



<b>Reference</b>
 

 

