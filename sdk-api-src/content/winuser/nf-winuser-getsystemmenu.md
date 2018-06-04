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

# GetSystemMenu function


## -description


Enables the application to access the window menu (also known as the system menu or the control menu) for copying and modifying. 


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window that will own a copy of the window menu. 


### -param bRevert [in]

Type: <b>BOOL</b>

The action to be taken. If this parameter is <b>FALSE</b>, <b>GetSystemMenu</b> returns a handle to the copy of the window menu currently in use. The copy is initially identical to the window menu, but it can be modified. If this parameter is <b>TRUE</b>, <b>GetSystemMenu</b> resets the window menu back to the default state. The previous window menu, if any, is destroyed. 


## -returns



Type: <b>HMENU</b>

If the <i>bRevert</i> parameter is <b>FALSE</b>, the return value is a handle to a copy of the window menu. If the <i>bRevert</i> parameter is <b>TRUE</b>, the return value is <b>NULL</b>. 




## -remarks



Any window that does not use the <b>GetSystemMenu</b> function to make its own copy of the window menu receives the standard window menu. 

The window menu initially contains items with various identifier values, such as <b>SC_CLOSE</b>, <b>SC_MOVE</b>, and <b>SC_SIZE</b>. 

Menu items on the window menu send <a href="https://msdn.microsoft.com/82c7cc95-82d5-4f0f-8c78-ab325561b04e">WM_SYSCOMMAND</a> messages. 

All predefined window menu items have identifier numbers greater than 0xF000. If an application adds commands to the window menu, it should use identifier numbers less than 0xF000. 

The system automatically grays items on the standard window menu, depending on the situation. The application can perform its own checking or graying by responding to the <a href="https://msdn.microsoft.com/d0fcc6d8-f57c-4d04-b9e7-4cfab6add173">WM_INITMENU</a> message that is sent before any menu is displayed. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e86b20c6-9a4b-40b7-95d1-ffa57795f5e0">GetMenu</a>



<a href="https://msdn.microsoft.com/be3819c2-8bdc-4a90-a188-ff8b4060eb8f">InsertMenuItem</a>



<a href="https://msdn.microsoft.com/f00c0b76-fabb-4451-bd4e-30b465d4d235">Menus</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/e1c669c7-7b56-428a-8433-d926330e42e1">SetMenuItemInfo</a>



<a href="https://msdn.microsoft.com/d0fcc6d8-f57c-4d04-b9e7-4cfab6add173">WM_INITMENU</a>



<a href="https://msdn.microsoft.com/82c7cc95-82d5-4f0f-8c78-ab325561b04e">WM_SYSCOMMAND</a>
 

 

