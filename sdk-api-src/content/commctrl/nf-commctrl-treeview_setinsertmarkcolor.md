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

# TreeView_SetInsertMarkColor macro


## -description


Sets the color used to draw the insertion mark for the tree view. You can use this macro or send the <a href="https://msdn.microsoft.com/c82304a8-3726-42c0-81e7-90d8f8205ead">TVM_SETINSERTMARKCOLOR</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param clr

TBD






#### - clrInsertMark

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>


<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> value that contains the new insertion mark color. 


#### - hwndTV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a tree-view control. 


## -see-also




<a href="https://msdn.microsoft.com/958ec5ff-9b6e-44de-940a-fbbb2e2857a8">TreeView_GetInsertMarkColor</a>
 

 

