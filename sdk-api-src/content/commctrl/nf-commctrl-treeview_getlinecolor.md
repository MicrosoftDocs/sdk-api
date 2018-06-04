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

# TreeView_GetLineColor macro


## -description


Gets the current line color. You can also use the <a href="https://msdn.microsoft.com/e74441b3-5d4f-4454-b896-2e96ce649419">TVM_GETLINECOLOR</a> message directly. 


## -parameters




### -param hwnd

TBD






#### - hwndTV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


## -remarks



This message only retrieves line colors. To retrieve the colors of the plus sign (+) and minus sign (-) inside the buttons, use the <a href="https://msdn.microsoft.com/a4c003eb-0e0e-496a-a048-ce733e8fcd45">TreeView_GetTextColor</a> macro.




## -see-also




<a href="https://msdn.microsoft.com/e74441b3-5d4f-4454-b896-2e96ce649419">TVM_GETLINECOLOR</a>
 

 

