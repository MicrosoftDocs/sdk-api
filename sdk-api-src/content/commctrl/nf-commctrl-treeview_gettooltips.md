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

# TreeView_GetToolTips macro


## -description


Retrieves the handle to the child tooltip control used by a tree-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/65e8189e-ae3e-4268-b1ed-bb0d88f2cbe3">TVM_GETTOOLTIPS</a> message explicitly. 


## -parameters




### -param hwnd

TBD






#### - hwndTV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a tree-view control. 


## -remarks



When created, tree-view controls automatically create a child tooltip control. To prevent a tree-view control from using tooltips, create the control with the <a href="Tree_View_Control_Window_Styles.htm">TVS_NOTOOLTIPS</a> style. 




## -see-also




<a href="https://msdn.microsoft.com/2a0e3776-9a07-4a7f-a2cc-68a273efff26">TreeView_SetToolTips</a>
 

 

