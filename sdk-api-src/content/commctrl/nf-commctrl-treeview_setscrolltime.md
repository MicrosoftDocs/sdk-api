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

# TreeView_SetScrollTime macro


## -description


Sets the maximum scroll time for the tree-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/b0ad81ba-0621-42b7-8fe1-f3bd5bc16d6a">TVM_SETSCROLLTIME</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param uTime

TBD






#### - hwndTV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a tree-view control. 


#### - uMaxScrollTime

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

New maximum scroll time, in milliseconds. If this value is less than 100, it will be rounded up to 100. 


## -remarks



The maximum scroll time is the longest amount of time that a scroll operation can take. Scrolling will be adjusted so that the scroll will take place within the maximum scroll time. A scroll operation may take less time than the maximum.




## -see-also




<a href="https://msdn.microsoft.com/992d1906-cda3-4ac7-ba90-c681c551ac2e">TVM_GETSCROLLTIME</a>
 

 

