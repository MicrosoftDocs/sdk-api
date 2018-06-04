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

# TreeView_InsertItem macro


## -description


Inserts a new item in a tree-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/c5e5f88f-6ec8-4b95-89ea-97f6f1fd735e">TVM_INSERTITEM</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param lpis

Type: <b>LPTVINSERTSTRUCT</b>

Pointer to a <a href="https://msdn.microsoft.com/ff0f4494-f41f-4e21-96e5-8e9aa9ef88bf">TVINSERTSTRUCT</a> structure that specifies the attributes of the tree-view item. 


#### - hwndTV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


## -see-also




<a href="https://msdn.microsoft.com/82eb9fcd-de10-4efb-8501-78c5af5e089e">TVN_ENDLABELEDIT</a>
 

 

