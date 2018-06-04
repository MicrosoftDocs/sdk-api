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

# ScreenSaverProc function


## -description


Receives messages sent to the specified screen saver window.


## -parameters




### -param hWnd

Type: <b>HWND</b>

An identifier of the window.


### -param message

Type: <b>UINT</b>

A message sent to the screen saver window.


### -param wParam

Type: <b>WPARAM</b>

Additional message-specific information.


### -param lParam

Type: <b>LPARAM</b>

Additional message-specific information.


## -returns



Type: <b>LONG</b>

The return value is the result of the message processing and depends on the message sent.




## -remarks



A screen saver's <b>ScreenSaverProc</b> window procedure should use the <a href="https://msdn.microsoft.com/eda5c4d4-0484-4c81-a699-5fedea0bd1c2">DefScreenSaverProc</a> function instead of the <a href="https://msdn.microsoft.com/fcc6b242-e152-4364-a977-b0441bec425f">DefWindowProc</a> function to provide default message processing. The <b>DefScreenSaverProc</b> function passes any messages that do not affect screen saver operations to <b>DefWindowProc</b>.

The <b>ScreenSaverProc</b> function must be exported by including it in the EXPORTS statement in the application's module-definition (.def) file.



