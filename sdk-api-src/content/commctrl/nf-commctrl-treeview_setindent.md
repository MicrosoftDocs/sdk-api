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

# TreeView_SetIndent macro


## -description


Sets the width of indentation for a tree-view control and redraws the control to reflect the new width. You can use this macro or send the <a href="https://msdn.microsoft.com/377da8fe-c8e6-479b-a283-f1811cbc3e58">TVM_SETINDENT</a> message explicitly.


## -parameters




### -param hwnd

TBD


### -param indent

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

Width, in pixels, of the indentation. If this parameter is less than the system-defined minimum width, the new width is set to the system-defined minimum. 


#### - hwndTV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


## -remarks



The system-defined minimum indent value is typically five pixels, but it is not fixed. To retrieve the exact value of the minimum indent on a particular system, use the <b>TreeView_SetIndent</b> macro with <i>indent</i> set to zero. Then use the <a href="https://msdn.microsoft.com/19cade42-8a21-457e-866e-ca8cf3696feb">TreeView_GetIndent</a> macro to retrieve the minimum indent value.




## -see-also




<a href="https://msdn.microsoft.com/377da8fe-c8e6-479b-a283-f1811cbc3e58">TVM_SETINDENT</a>
 

 

