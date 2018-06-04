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

# DAD_DragEnterEx2 function


## -description


<p class="CCE_Message">[<b>DAD_DragEnterEx2</b> is available in Windows 2000 and Windows XP. It might be altered or unavailable in subsequent versions. Use <a href="https://msdn.microsoft.com/e12d7dc5-75a0-4537-bfb7-071ff8dfe7d5">ImageList_DragEnter</a> instead.]

Locks updates to the specified window during a drag-and-drop operation and displays the drag image at the specified position within the window.


## -parameters




### -param hwndTarget [in]

Type: <b>HWND</b>

A handle to the window that owns the drag image.


### -param ptStart

Type: <b>const <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a></b>

Specifies the coordinates at which to begin displaying the drag image. The coordinates are relative to the upper-left corner of the window, not the client area.


### -param pdtObject [in, optional]

Type: <b><a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interface on the data object. This data object contains the data being transferred in the drag-and-drop operation. If the drop occurs, this data object will be incorporated into the target. This parameter may be <b>NULL</b>.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful, <b>FALSE</b> otherwise.




## -see-also




<a href="https://msdn.microsoft.com/32f98df7-e357-4d17-9e33-f162a6ffb7ed">DAD_DragEnterEx</a>



<a href="https://msdn.microsoft.com/e12d7dc5-75a0-4537-bfb7-071ff8dfe7d5">ImageList_DragEnter</a>
 

 

