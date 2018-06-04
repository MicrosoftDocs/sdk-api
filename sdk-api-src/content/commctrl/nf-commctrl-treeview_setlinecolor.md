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

# TreeView_SetLineColor macro


## -description


Sets the current line color. You can also use the <a href="https://msdn.microsoft.com/c5fc28af-5603-489f-aa6b-73e153f9aebc">TVM_SETLINECOLOR</a> message directly. 


## -parameters




### -param hwnd

TBD


### -param clr

TBD






#### - clrLine

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>

A <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> that specifies the new line color. Use the CLR_DEFAULT value to restore the system default colors. 


#### - hwndTV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


## -remarks



This message only changes line colors. To change the colors of the plus sign (+) and minus sign (-) inside the buttons, use the <a href="https://msdn.microsoft.com/7aacaf9f-2bec-4f5e-84eb-0d51252f0247">TreeView_SetTextColor</a> macro.




## -see-also




<a href="https://msdn.microsoft.com/c5fc28af-5603-489f-aa6b-73e153f9aebc">TVM_SETLINECOLOR</a>
 

 

