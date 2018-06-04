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

# CheckMenuRadioItem function


## -description


Checks a specified menu item and makes it a radio item. At the same time, the function clears all other menu items in the associated group and clears the radio-item type flag for those items.


## -parameters




### -param hmenu [in]

Type: <b>HMENU</b>

A handle to the menu that contains the group of menu items. 


### -param first

TBD


### -param last

TBD


### -param check

TBD


### -param flags

TBD




#### - idCheck [in]

Type: <b>UINT</b>

The identifier or position of the menu item to check. 


#### - idFirst [in]

Type: <b>UINT</b>

The identifier or position of the first menu item in the group. 


#### - idLast [in]

Type: <b>UINT</b>

The identifier or position of the last menu item in the group. 


#### - uFlags [in]

Type: <b>UINT</b>

Indicates the meaning of <i>idFirst</i>, <i>idLast</i>, and <i>idCheck</i>. If this parameter is <b>MF_BYCOMMAND</b>, the other parameters specify menu item identifiers. If it is <b>MF_BYPOSITION</b>, the other parameters specify the menu item positions. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, use the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -remarks



The <b>CheckMenuRadioItem</b> function sets the <b>MFT_RADIOCHECK</b> type flag and the <b>MFS_CHECKED</b> state for the item specified by <i>idCheck</i> and, at the same time, clears both flags for all other items in the group. The selected item is displayed using a bullet bitmap instead of a check-mark bitmap.

For more information about menu item type and state flags, see the <a href="https://msdn.microsoft.com/43d30b39-c1e1-4711-97a2-b5bc29dad9df">MENUITEMINFO</a> structure.


#### Examples

For an example, see Example of <a href="using_menus.htm">Example of Using Custom Checkmark Bitmaps</a>. 

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/43d30b39-c1e1-4711-97a2-b5bc29dad9df">MENUITEMINFO</a>



<a href="https://msdn.microsoft.com/f00c0b76-fabb-4451-bd4e-30b465d4d235">Menus</a>



<b>Reference</b>
 

 

