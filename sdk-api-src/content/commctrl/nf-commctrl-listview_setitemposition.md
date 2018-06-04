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

# ListView_SetItemPosition macro


## -description


Moves an item to a specified position in a list-view control (in icon or small icon view). You can use this macro or send the <a href="https://msdn.microsoft.com/dfb35af4-e6c3-40fc-9d7c-cf0d68a3ea01">LVM_SETITEMPOSITION</a> message explicitly. 


## -parameters




### -param hwndLV

TBD


### -param i

Type: <b>int</b>

The index of the list-view item. 


### -param x

Type: <b>int</b>

The new x-position of the item's upper-left corner, in view coordinates. 


### -param y

Type: <b>int</b>

The new y-position of the item's upper-left corner, in view coordinates. 


#### - hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


## -remarks



If the list-view control has the <a href="List_view_window_styles.htm">LVS_AUTOARRANGE</a> style, the list-view control is arranged after the position of the item is set. 

On Windows Vista, calling this macro on a list-view control with the <a href="List_view_window_styles.htm">LVS_AUTOARRANGE</a> style does nothing, and the return value is <b>FALSE</b>.



