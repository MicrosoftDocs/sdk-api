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

# Shell_MergeMenus function


## -description


<p class="CCE_Message">[<b>Shell_MergeMenus</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Merges two menus.


## -parameters




### -param hmDst [in]

Type: <b>HMENU</b>

The destination menu to which <i>hmSrc</i> is added.


### -param hmSrc [in]

Type: <b>HMENU</b>

The source menu which is added to <i>hmDst</i>.


### -param uInsert

Type: <b>UINT</b>

The point in <i>hmDst</i> after which the entries in <i>hmSrc</i> are inserted.


### -param uIDAdjust

Type: <b>UINT</b>

This number is added to each menu's ID to give an adjusted ID. Set to <code>0</code> for no adjustment. The value for <i>uIDAdjust</i> would typically be the number of items in <i>hmDst</i>. This number can be obtained using the <a href="https://msdn.microsoft.com/6a1d542e-b955-48aa-a3b8-e348fefd6f14">GetMenuItemCount</a>.


### -param uIDAdjustMax

Type: <b>UINT</b>

The maximum adjusted ID to add to the menu. Any adjusted ID greater than this value is not added. To allow all IDs, set this parameter to 0xFFFF.


### -param uFlags

Type: <b>ULONG</b>

One or more of the following flags.



#### MM_ADDSEPARATOR

Add a separator between the items from the two menus if one does not exist already. If you are inserting the entries from <i>hmSrc</i> into the middle of <i>hmDst</i>, a separator is added above and below the <i>hmSrc</i> material.



#### MM_DONTREMOVESEPS

Do not remove any existing separators in the two menus. Note that this could result in two separators in a row.



#### MM_SUBMENUSHAVEIDS

Set this flag if the submenus have IDs which should be adjusted.


## -returns



Type: <b>UINT</b>

Returns the next open ID at the end of the menu (the maximum adjusted ID + 1).



