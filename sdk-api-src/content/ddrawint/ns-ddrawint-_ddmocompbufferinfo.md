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

# _DDMOCOMPBUFFERINFO structure


## -description


The DDMOCOMPBUFFERINFO structure contains the macro block information required to render a frame and passes this information to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551693">DD_RENDERMOCOMPDATA</a> structure. 


## -struct-fields




### -field dwSize

Specifies the size in bytes of this DDMOCOMPBUFFERINFO structure.


### -field lpCompSurface

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551733">DD_SURFACE_LOCAL</a> structure that contains the compressed data. 


### -field dwDataOffset

Indicates the offset to the relevant data, in bytes, from the beginning of the buffer. This value does not allow for pitch.


### -field dwDataSize

Indicates the size of the relevant data in bytes. This value does not allow for pitch.


### -field lpPrivate

Used by Microsoft DirectDraw and should be ignored by the driver.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551693">DD_RENDERMOCOMPDATA</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551733">DD_SURFACE_LOCAL</a>
 

 

