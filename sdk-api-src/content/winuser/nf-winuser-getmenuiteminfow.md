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

# GetMenuItemInfoW function


## -description


Retrieves information about a menu item.


## -parameters




### -param hmenu

TBD


### -param item

TBD


### -param fByPosition [in]

Type: <b>BOOL</b>

The meaning of <i>uItem</i>. If this parameter is <b>FALSE</b>, <i>uItem</i> is a menu item identifier. Otherwise, it is a menu item position. See <a href="about_menus.htm">Accessing Menu Items Programmatically</a> for more information. 


### -param lpmii [in, out]

Type: <b>LPMENUITEMINFO</b>

A pointer to a <a href="https://msdn.microsoft.com/43d30b39-c1e1-4711-97a2-b5bc29dad9df">MENUITEMINFO</a> structure that specifies the information to retrieve and receives information about the menu item. Note that you must set the <b>cbSize</b> member to <code>sizeof(MENUITEMINFO)</code> before calling this function. 


#### - hMenu [in]

Type: <b>HMENU</b>

A handle to the menu that contains the menu item. 


#### - uItem [in]

Type: <b>UINT</b>

The identifier or position of the menu item to get information about. The meaning of this parameter depends on the value of <i>fByPosition</i>. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, use the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -remarks



To retrieve a menu item of type <b>MFT_STRING</b>, first find the size of the string by setting the <b>dwTypeData</b> member of <a href="https://msdn.microsoft.com/43d30b39-c1e1-4711-97a2-b5bc29dad9df">MENUITEMINFO</a> to <b>NULL</b> and then calling <b>GetMenuItemInfo</b>. The value of <b>cch</b>+1 is the size needed. Then allocate a buffer of this size, place the pointer to the buffer in <b>dwTypeData</b>, increment <b>cch</b> by one, and then call <b>GetMenuItemInfo</b> once again to fill the buffer with the string.

If the retrieved menu item is of some other type, then <b>GetMenuItemInfo</b> sets the <b>dwTypeData</b> member to a value whose type is specified by the <b>fType</b><b>fType</b> member and sets <b>cch</b> to 0.


#### Examples

For an example, see <a href="using_menus.htm">Example of Owner-Drawn Menu Items</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/f00c0b76-fabb-4451-bd4e-30b465d4d235">Menus</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/e1c669c7-7b56-428a-8433-d926330e42e1">SetMenuItemInfo</a>
 

 

