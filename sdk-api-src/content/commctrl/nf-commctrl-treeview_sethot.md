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

# TreeView_SetHot macro


## -description


<p class="CCE_Message">[Intended for internal use; not recommended for use in applications. This macro may not be supported in future versions of Windows.]

Sets the hot item for a tree-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/5e7368f5-40ce-4e7b-bbe3-5fe0b17181a8">TVM_SETHOT</a> message explicitly.


## -parameters




### -param hwnd

TBD


### -param hitem

Type: <b>HTREEITEM</b>

Handle to the new hot item. If this value is <b>NULL</b>, the tree-view control will be set to have no hot item. 


#### - hwndTV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


## -remarks



The <i>hot item</i> is the item that the mouse is hovering over. The <a href="https://msdn.microsoft.com/5e7368f5-40ce-4e7b-bbe3-5fe0b17181a8">TVM_SETHOT</a> message sent by this macro makes an item look like it is the hot item even if the mouse is not hovering over it.

The <a href="https://msdn.microsoft.com/5e7368f5-40ce-4e7b-bbe3-5fe0b17181a8">TVM_SETHOT</a> message has no visible effect if the <a href="Tree_View_Control_Window_Styles.htm">TVS_TRACKSELECT</a> style is not set.

If it succeeds, the <a href="https://msdn.microsoft.com/5e7368f5-40ce-4e7b-bbe3-5fe0b17181a8">TVM_SETHOT</a> message causes the hot item to be redrawn.

The <a href="https://msdn.microsoft.com/5e7368f5-40ce-4e7b-bbe3-5fe0b17181a8">TVM_SETHOT</a> message is ignored if <i>hitem</i> is <b>NULL</b> and the tree-view control is tracking the mouse.
        
      




## -see-also




<a href="https://msdn.microsoft.com/5e7368f5-40ce-4e7b-bbe3-5fe0b17181a8">TVM_SETHOT</a>
 

 

