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

# ListView_SetItemPosition32 macro


## -description


Moves an item to a specified position in a list-view control (in icon or small icon view). This macro differs from the <a href="https://msdn.microsoft.com/8965e972-f547-41dc-b742-a6ac757f0f76">ListView_SetItemPosition</a> macro in that it uses 32-bit coordinates. You can use the <b>ListView_SetItemPosition32</b> macro or send the <a href="https://msdn.microsoft.com/77db5fd0-bbc3-47ad-95ef-61ef4ac022bc">LVM_SETITEMPOSITION32</a> message explicitly. 


## -parameters




### -param hwndLV

TBD


### -param i

TBD


### -param x0

TBD


### -param y0

TBD






#### - hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


#### - iItem

Type: <b>int</b>

The index of the list-view item for which to set the position. 


#### - x

Type: <b>int</b>

New horizontal coordinates of the item. 


#### - y

Type: <b>int</b>

New vertical coordinates of the item. 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a>
 

 

