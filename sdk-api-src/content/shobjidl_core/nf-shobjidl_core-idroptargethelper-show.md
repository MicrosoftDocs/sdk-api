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

# IDropTargetHelper::Show


## -description


Notifies the drag-image manager to show or hide the drag image.


## -parameters




### -param fShow [in]

Type: <b>BOOL</b>

A boolean value that is set to <b>TRUE</b> to show the drag image, and <b>FALSE</b> to hide it.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM error value otherwise.




## -remarks



This method is used when dragging over a target window in a low color-depth video mode. It allows the target to notify the drag-image manager to hide the drag image while it is painting the window. While you are painting a window that is currently being dragged over, hide the drag image by calling <b>Show</b> with <i>fShow</i> set to <b>FALSE</b>. Once the window has been painted, display the drag image again by calling <b>Show</b> with <i>fShow</i> set to <b>TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/b1ddbf7e-edf3-48fb-8983-ae39cb7bb4b0">IDropTargetHelper</a>
 

 

