---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

Controls the meaning of <i>uItem</i>. If this parameter is <b>FALSE</b>, <i>uItem</i> is a menu item identifier. Otherwise, it is a menu item position. See <a href="about_menus.htm">Accessing Menu Items Programmatically</a> for more information.


### -param lpmi

TBD




#### - hMenu [in]

Type: <b>HMENU</b>

A handle to the menu in which the new menu item is inserted. 


#### - lpmii [in]

Type: <b>LPCMENUITEMINFO</b>

A pointer to a <a href="https://msdn.microsoft.com/43d30b39-c1e1-4711-97a2-b5bc29dad9df">MENUITEMINFO</a> structure that contains information about the new menu item. 


#### - uItem [in]

Type: <b>UINT</b>

The identifier or position of the menu item before which to insert the new item. The meaning of this parameter depends on the value of <i>fByPosition</i>. 


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
 

 

