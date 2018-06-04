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

# DragQueryPoint function


## -description


Retrieves the position of the mouse pointer at the time a file was dropped during a drag-and-drop operation.


## -parameters




### -param hDrop [in]

Type: <b>HDROP</b>

Handle of the drop structure that describes the dropped file.


### -param ppt

TBD




#### - lppt [out]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structure that, when this function returns successfully, receives the coordinates of the mouse pointer at the time the file was dropped.


## -returns



Type: <b>BOOL</b>

<b>TRUE</b> if the drop occurred in the client area of the window; otherwise <b>FALSE</b>.




## -remarks



The window for which coordinates are returned is the window that received the <a href="https://msdn.microsoft.com/07dc2df7-4699-4e9c-b1a5-4ce877116268">WM_DROPFILES</a> message.




## -see-also




<a href="https://msdn.microsoft.com/93fab381-9035-46c4-ba9d-efb2d0801d84">DragQueryFile</a>
 

 

