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

# ListView_GetItem macro


## -description


Gets some or all of a list-view item's attributes. You can use this macro or send the <a href="https://msdn.microsoft.com/684ad96a-2c3b-4148-b66c-41f8322500bb">LVM_GETITEM</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param pitem

Type: <b>LPLVITEM</b>

A pointer to an <a href="https://msdn.microsoft.com/4141a2ee-9016-4d76-8758-a36fc6eedb44">LVITEM</a> structure that specifies the information to retrieve and receives information about the list-view item. 


## -remarks



When the <a href="https://msdn.microsoft.com/684ad96a-2c3b-4148-b66c-41f8322500bb">LVM_GETITEM</a> message is sent, the 
				<b>iItem</b> and <b>iSubItem</b> members identify the item or subitem to retrieve information about and the <b>mask</b> member specifies which attributes to retrieve. For a list of possible values, see the description of the <a href="https://msdn.microsoft.com/4141a2ee-9016-4d76-8758-a36fc6eedb44">LVITEM</a> structure.

If the LVIF_TEXT flag is set in the <b>mask</b> member of the <a href="https://msdn.microsoft.com/4141a2ee-9016-4d76-8758-a36fc6eedb44">LVITEM</a> structure, the <b>pszText</b> member must point to a valid buffer and the <b>cchTextMax</b> member must be set to the number of characters in that buffer. Applications should not assume that the text will necessarily be placed in the specified buffer. The control may instead change the <b>pszText</b> member of the structure to point to the new text rather than place it in the buffer.

If the <b>mask</b> member specifies the LVIF_STATE value, the <b>stateMask</b> member must specify the item state bits to retrieve. On output, the <b>state</b> member contains the values of the specified state bits.



