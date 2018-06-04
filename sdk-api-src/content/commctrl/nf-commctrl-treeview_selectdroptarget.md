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

# TreeView_SelectDropTarget macro


## -description


Redraws a specified tree-view control item in the style used to indicate the target of a drag-and-drop operation. You can use this macro or the <a href="https://msdn.microsoft.com/e23ef98b-7db7-4e61-aace-05e6520f8b5c">TreeView_Select</a> macro, or you can send the <a href="https://msdn.microsoft.com/8b943958-7b93-4e54-99de-200121cf0752">TVM_SELECTITEM</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param hitem

Type: <b>HTREEITEM</b>

Handle to an item. If the <i>hitem</i> parameter is <b>NULL</b>, the control is set to have no selected item. 


#### - hwndTV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


## -remarks



If the specified item is the child of a collapsed parent item, the parent's list of child items is expanded to reveal the specified item. In this case, the parent window receives the <a href="https://msdn.microsoft.com/5ce256df-49e5-4fbf-9cdc-79dd2edbd8ec">TVN_ITEMEXPANDING</a> and <a href="https://msdn.microsoft.com/18d9d61d-6ec5-4d3b-9c02-36d0e61ed232">TVN_ITEMEXPANDED</a> notification codes. 

Using the <b>TreeView_SelectDropTarget</b> macro is equivalent to sending the <a href="https://msdn.microsoft.com/8b943958-7b93-4e54-99de-200121cf0752">TVM_SELECTITEM</a> message with its 
				<i>flag</i> parameter set to the TVGN_DROPHILITE value. 



