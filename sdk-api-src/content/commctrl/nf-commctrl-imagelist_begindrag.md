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

# ImageList_BeginDrag function


## -description


Begins dragging an image. 


## -parameters




### -param himlTrack

Type: <b>HIMAGELIST</b>

A handle to the image list. 


### -param iTrack

Type: <b>int</b>

The index of the image to drag. 


### -param dxHotspot

Type: <b>int</b>

The x-coordinate of the location of the drag position relative to the upper-left corner of the image. 


### -param dyHotspot

Type: <b>int</b>

The y-coordinate of the location of the drag position relative to the upper-left corner of the image. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns nonzero if successful, or zero otherwise. 




## -remarks



This function creates a temporary image list that is used for dragging. In response to subsequent <a href="https://msdn.microsoft.com/9b99387e-e176-4b20-a05a-bc75928a1367">WM_MOUSEMOVE</a> messages, you can move the drag image by using the <a href="https://msdn.microsoft.com/a7d7fcd4-ba03-43ba-ae37-df8d4173c64d">ImageList_DragMove</a> function. To end the drag operation, you can use the <a href="https://msdn.microsoft.com/54465b0d-6bbe-4c50-8124-cbf3115d0848">ImageList_EndDrag</a> function. 



