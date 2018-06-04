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

# MenuHelp function


## -description


Processes <a href="https://msdn.microsoft.com/57684a19-dfaa-4e0c-a8ff-010533322cb0">WM_MENUSELECT</a> and <a href="https://msdn.microsoft.com/5516098e-fd90-49c8-afb0-78164b028376">WM_COMMAND</a> messages and displays Help text about the current menu in the specified status window.


## -parameters




### -param uMsg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Message being processed. This can be either <a href="https://msdn.microsoft.com/57684a19-dfaa-4e0c-a8ff-010533322cb0">WM_MENUSELECT</a> or <a href="https://msdn.microsoft.com/5516098e-fd90-49c8-afb0-78164b028376">WM_COMMAND</a>. 


### -param wParam

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">WPARAM</a></b>

wParam of the message specified in 
					<i>uMsg</i>. 


### -param lParam

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

lParam of the message specified in 
					<i>uMsg</i>. 


### -param hMainMenu

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HMENU</a></b>

Handle to the application's main menu. 


### -param hInst

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HINSTANCE</a></b>

Handle to the module that contains the string resources. 


### -param hwndStatus

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the status window. 


### -param lpwIDs

Type: <b>LPUINT</b>

Pointer to an array of values that contains pairs of string resource identifiers and menu handles. The function searches the array for the handle to the selected menu and, if found, uses the corresponding resource identifier to load the appropriate Help string. 


## -returns



No return value.




## -remarks




		The <b>MenuHelp</b> function is a helper function. Helper functions are available as a convenience to programming. They combine into one call a sequence of frequently used calls. You use <b>MenuHelp</b> to send <a href="https://msdn.microsoft.com/57684a19-dfaa-4e0c-a8ff-010533322cb0">WM_MENUSELECT</a> and <a href="https://msdn.microsoft.com/5516098e-fd90-49c8-afb0-78164b028376">WM_COMMAND</a> messages.
		



