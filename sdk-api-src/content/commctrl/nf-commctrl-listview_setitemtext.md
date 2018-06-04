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

# ListView_SetItemText macro


## -description


Changes the text of a list-view item or subitem. You can use this macro or send the <a href="https://msdn.microsoft.com/1a9c7e4d-78e0-44c7-bf4f-d0fc7a0049f3">LVM_SETITEMTEXT</a> message explicitly. 


## -parameters




### -param hwndLV

TBD


### -param i

Type: <b>int</b>

The zero-based index of the list-view item. 


#### - iSubItem_

Type: <b>int</b>

The one-based index of the subitem. To set the item label, set 
					<i>iSubItem</i> to zero. 


#### - pszText_

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCTSTR</a></b>

A pointer to a null-terminated string that contains the new text. This parameter can be LPSTR_TEXTCALLBACK to indicate a callback item for which the parent window stores the text. In this case, the list-view control sends the parent an <a href="https://msdn.microsoft.com/04310e39-69bc-45d7-958c-00452279d7a9">LVN_GETDISPINFO</a> notification code when it needs the text.
This parameter can be <b>NULL</b>.


#### - hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


#### - iSubItem

Type: <b>int</b>

The one-based index of the subitem. To set the item label, set 
					<i>iSubItem</i> to zero. 


#### - pszText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCTSTR</a></b>

A pointer to a null-terminated string that contains the new text. This parameter can be LPSTR_TEXTCALLBACK to indicate a callback item for which the parent window stores the text. In this case, the list-view control sends the parent an <a href="https://msdn.microsoft.com/04310e39-69bc-45d7-958c-00452279d7a9">LVN_GETDISPINFO</a> notification code when it needs the text.
This parameter can be <b>NULL</b>.

