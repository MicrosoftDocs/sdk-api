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

# MenuItemFromPoint function


## -description


Determines which menu item, if any, is at the specified location.


## -parameters




### -param hWnd [in, optional]

Type: <b>HWND</b>

A handle to the window containing the menu. If this value is <b>NULL</b> and the <i>hMenu</i> parameter represents a popup menu, the function will find the menu window. 


### -param hMenu [in]

Type: <b>HMENU</b>

A handle to the menu containing the menu items to hit test. 


### -param ptScreen [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a></b>

A structure that specifies the location to test. If <i>hMenu</i> specifies a menu bar, this parameter is in window coordinates. Otherwise, it is in client coordinates. 


## -returns



Type: <b>int</b>

Returns the zero-based position of the menu item at the specified location or -1 if no menu item is at the specified location.




## -see-also




<a href="https://msdn.microsoft.com/f00c0b76-fabb-4451-bd4e-30b465d4d235">Menus</a>
 

 

