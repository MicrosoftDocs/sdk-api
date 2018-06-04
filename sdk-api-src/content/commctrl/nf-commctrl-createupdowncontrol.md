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

# CreateUpDownControl function


## -description


Creates an up-down control. 
			 Note: This function is obsolete. It is a 16 bit function and cannot handle 32 bit values for range and position.


## -parameters




### -param dwStyle

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Window styles for the control. This parameter should include the <a href="https://msdn.microsoft.com/bfc146f1-bebd-4e68-a29e-a73ff3e8f35b">WS_CHILD</a>, <a href="https://msdn.microsoft.com/bfc146f1-bebd-4e68-a29e-a73ff3e8f35b">WS_BORDER</a>, and <a href="https://msdn.microsoft.com/bfc146f1-bebd-4e68-a29e-a73ff3e8f35b">WS_VISIBLE</a> styles, and it may include any of the window styles specific to the up-down control. 


### -param x

Type: <b>int</b>

Horizontal coordinate, in client coordinates, of the upper-left corner of the control. 


### -param y

Type: <b>int</b>

Vertical coordinate, in client coordinates, of the upper-left corner of the control. 


### -param cx

Type: <b>int</b>

Width, in pixels, of the up-down control. 


### -param cy

Type: <b>int</b>

Height, in pixels, of the up-down control. 


### -param hParent

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the parent window of the up-down control. 


### -param nID

Type: <b>int</b>

Identifier for the up-down control. 


### -param hInst

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HINSTANCE</a></b>

Handle to the module instance of the application creating the up-down control. 


### -param hBuddy

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the window associated with the up-down control. If this parameter is <b>NULL</b>, the control has no buddy window. 


### -param nUpper

Type: <b>int</b>

Upper limit (range) of the up-down control. 


### -param nLower

Type: <b>int</b>

Lower limit (range) of the up-down control. 


### -param nPos

Type: <b>int</b>

Position of the control. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

If the function succeeds, the return value is the window handle to the up-down control. If the function fails, the return value is <b>NULL</b>.



