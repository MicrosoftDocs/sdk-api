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

# DragAcceptFiles function


## -description


Registers whether a window accepts dropped files.


## -parameters




### -param hWnd

Type: <b>HWND</b>

The identifier of the window that is registering whether it will accept dropped files.


### -param fAccept

Type: <b>BOOL</b>

A value that indicates if the window identified by the <i>hWnd</i> parameter accepts dropped files. This value is <b>TRUE</b> to accept dropped files or <b>FALSE</b> to discontinue accepting dropped files.


## -returns



No return value.




## -remarks



An application that calls <b>DragAcceptFiles</b> with the <i>fAccept</i> parameter set to <b>TRUE</b> has identified itself as able to process the <a href="https://msdn.microsoft.com/07dc2df7-4699-4e9c-b1a5-4ce877116268">WM_DROPFILES</a> message from File Manager.



