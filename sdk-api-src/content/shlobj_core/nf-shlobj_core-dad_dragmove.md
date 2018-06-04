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

# DAD_DragMove function


## -description


<p class="CCE_Message">[<b>DAD_DragMove</b> is available in Windows 2000 and Windows XP. It might be altered or unavailable in subsequent versions. Use <a href="https://msdn.microsoft.com/a7d7fcd4-ba03-43ba-ae37-df8d4173c64d">ImageList_DragMove</a> instead.
      ]

Moves the image that is being dragged during a drag-and-drop operation.


## -parameters




### -param pt

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a></b>

The coordinates at which to display the drag image. The coordinates are relative to the upper-left corner of the window, not the client area.  


## -returns



Type: <b>BOOL</b>

Returns nonzero if successful, or zero otherwise.



