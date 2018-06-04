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

# GetMenuItemID function


## -description


Retrieves the menu item identifier of a menu item located at the specified position in a menu. 


## -parameters




### -param hMenu [in]

Type: <b>HMENU</b>

A handle to the menu that contains the item whose identifier is to be retrieved. 


### -param nPos [in]

Type: <b>int</b>

The zero-based relative position of the menu item whose identifier is to be retrieved. 


## -returns



Type: <b>UINT</b>

The return value is the identifier of the specified menu item. If the menu item identifier is <b>NULL</b> or if the specified item opens a submenu, the return value is -1. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/6a1d542e-b955-48aa-a3b8-e348fefd6f14">GetMenuItemCount</a>



<a href="https://msdn.microsoft.com/f00c0b76-fabb-4451-bd4e-30b465d4d235">Menus</a>



<b>Reference</b>
 

 

