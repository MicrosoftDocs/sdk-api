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

# ImageList_SetDragCursorImage function


## -description


Creates a new drag image by combining the specified image (typically a mouse cursor image) with the current drag image. 


## -parameters




### -param himlDrag

Type: <b>HIMAGELIST</b>

A handle to the image list that contains the new image to combine with the drag image.


### -param iDrag

Type: <b>int</b>

The index of the new image to combine with the drag image.


### -param dxHotspot

Type: <b>int</b>

The x-position of the hot spot within the new image.


### -param dyHotspot

Type: <b>int</b>

The y-position of the hot spot within the new image.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns nonzero if successful, or zero otherwise.



