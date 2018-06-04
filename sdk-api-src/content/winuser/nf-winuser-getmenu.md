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

# GetMenu function


## -description


Retrieves a handle to the menu assigned to the specified window. 


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window whose menu handle is to be retrieved. 


## -returns



Type: <b>HMENU</b>

The return value is a handle to the menu. If the specified window has no menu, the return value is <b>NULL</b>. If the window is a child window, the return value is undefined. 




## -remarks



<b>GetMenu</b> does not work on floating menu bars. Floating menu bars are custom controls that mimic standard menus; they are not menus. To get the handle on a floating menu bar, use the <a href="https://msdn.microsoft.com/4681b5df-59fd-435f-957c-892ea3dbeaaf">Active Accessibility</a> APIs.


#### Examples

For an example, see <a href="using_menus.htm">Adding Lines and Graphs to a Menu</a>. 

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/009ede3f-da6e-4195-90e0-9f046146fd5c">GetSubMenu</a>



<a href="https://msdn.microsoft.com/f00c0b76-fabb-4451-bd4e-30b465d4d235">Menus</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/86d61b87-99ad-45e1-bcff-af892b4bb51b">SetMenu</a>
 

 

