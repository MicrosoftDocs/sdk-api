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

# GetMenuItemRect function


## -description


Retrieves the bounding rectangle 
		for the specified menu item.


## -parameters




### -param hWnd [in, optional]

Type: <b>HWND</b>

A handle to the window containing the menu.


						 
						If this value is <b>NULL</b> and the <i>hMenu</i> 
						parameter represents a popup menu, the function will find the menu window.


### -param hMenu [in]

Type: <b>HMENU</b>

A handle to a menu. 


### -param uItem [in]

Type: <b>UINT</b>

The zero-based position of the menu item. 


### -param lprcItem [out]

Type: <b>LPRECT</b>

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that receives the 
				bounding rectangle of the specified menu item expressed in screen coordinates. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error 
					information, use the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -remarks



In order for the returned rectangle to be meaningful, the menu must be popped 
		up if a popup menu or attached to a window if a menu bar. Menu item positions are not 
		determined until the menu is displayed.




## -see-also




<a href="https://msdn.microsoft.com/f00c0b76-fabb-4451-bd4e-30b465d4d235">Menus</a>
 

 

