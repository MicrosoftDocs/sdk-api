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

# TreeView_SetTextColor macro


## -description


Sets the text color of the control. You can use this macro or send the <a href="https://msdn.microsoft.com/eb57dfd5-3e7b-4cda-a659-be9e03470a44">TVM_SETTEXTCOLOR</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param clr

TBD






#### - clrText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>


<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> value that contains the new text color. If this argument is -1, the control will revert to using the system color for the text color. 


#### - hwndTV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a tree-view control. 


## -see-also




<a href="https://msdn.microsoft.com/a4c003eb-0e0e-496a-a048-ce733e8fcd45">TreeView_GetTextColor</a>
 

 

