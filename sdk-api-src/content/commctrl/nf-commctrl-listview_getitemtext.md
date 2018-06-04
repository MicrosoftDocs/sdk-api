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

# ListView_GetItemText macro


## -description


Gets the text of a list-view item or subitem. You can use this macro or send the <a href="https://msdn.microsoft.com/5711ed18-a766-4e7f-9e9d-b9203231b369">LVM_GETITEMTEXT</a> message explicitly.


## -parameters




### -param hwndLV

TBD


### -param i

TBD


#### - iSubItem_

Type: <b>int</b>

The index of the subitem. To retrieve the item text, set 
					<i>iSubItem</i> to zero. 


#### - pszText_

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPTSTR</a></b>

A pointer to a buffer that receives the item or subitem text. 


#### - cchTextMax_

Type: <b>int</b>

The number of characters in the 
					<i>pszText</i> buffer.


#### - cchTextMax

Type: <b>int</b>

The number of characters in the 
					<i>pszText</i> buffer.


#### - hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


#### - iItem

Type: <b>int</b>

The index of the list-view item. 


#### - iSubItem

Type: <b>int</b>

The index of the subitem. To retrieve the item text, set 
					<i>iSubItem</i> to zero. 


#### - pszText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPTSTR</a></b>

A pointer to a buffer that receives the item or subitem text. 


## -see-also




<a href="https://msdn.microsoft.com/4141a2ee-9016-4d76-8758-a36fc6eedb44">LVITEM</a>
 

 

