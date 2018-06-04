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

# TreeView_GetItem macro


## -description


Retrieves some or all of a tree-view item's attributes. You can use this macro or send the <a href="https://msdn.microsoft.com/e26ec000-967d-46de-8f71-6ebc36fefe5e">TVM_GETITEM</a> message explicitly.


## -parameters




### -param hwnd

TBD


### -param pitem

Type: <b>LPTVITEM</b>

Pointer to a <a href="https://msdn.microsoft.com/8e97f293-3cfb-4320-9781-639dfda1bbfe">TVITEM</a> structure that specifies the information to retrieve and receives information about the item. With <a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">version 4.71</a> and later, you can use a <a href="https://msdn.microsoft.com/a1112639-fe6d-432a-8b0a-b914bcb30e11">TVITEMEX</a> structure instead. 


#### - hwndTV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


## -remarks



When the <a href="https://msdn.microsoft.com/e26ec000-967d-46de-8f71-6ebc36fefe5e">TVM_GETITEM</a> message is sent, the 
				<b>hItem</b> member of the <a href="https://msdn.microsoft.com/8e97f293-3cfb-4320-9781-639dfda1bbfe">TVITEM</a> or <a href="https://msdn.microsoft.com/a1112639-fe6d-432a-8b0a-b914bcb30e11">TVITEMEX</a> structure identifies the item to retrieve information about, and the <b>mask</b> member specifies the attributes to retrieve.

If the TVIF_TEXT flag is set in the 
				<b>mask</b> member of the <a href="https://msdn.microsoft.com/8e97f293-3cfb-4320-9781-639dfda1bbfe">TVITEM</a> or <a href="https://msdn.microsoft.com/a1112639-fe6d-432a-8b0a-b914bcb30e11">TVITEMEX</a> structure, the <b>pszText</b> member must point to a valid buffer and the <b>cchTextMax</b> member must be set to the number of characters in that buffer. The returned text will not necessarily be stored in the original buffer passed by the application. It is possible that <b>pszText</b> will point to text in a new buffer rather than place it in the old buffer. 



