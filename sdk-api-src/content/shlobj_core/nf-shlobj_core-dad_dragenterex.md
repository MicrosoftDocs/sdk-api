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

# DAD_DragEnterEx function


## -description


<p class="CCE_Message">[<b>DAD_DragEnterEx</b> is available in Windows 2000 and Windows XP. It might be altered or unavailable in subsequent versions. Use <a href="https://msdn.microsoft.com/e12d7dc5-75a0-4537-bfb7-071ff8dfe7d5">ImageList_DragEnter</a> instead.
      ]

Locks updates to the specified window during a drag operation and displays the drag image at the specified position within the window.


## -parameters




### -param hwndTarget

Type: <b>HWND</b>

A handle to the window that owns the drag image.


### -param ptStart

Type: <b>const <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a></b>

The coordinates at which to begin displaying the drag image. The coordinates are relative to the upper-left corner of the window, not the client area.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.



