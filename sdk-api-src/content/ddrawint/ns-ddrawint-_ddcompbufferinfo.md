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

# _DDCOMPBUFFERINFO structure


## -description


The DDCOMPBUFFERINFO structure contains driver-supplied information regarding compression buffers.


## -struct-fields




### -field dwSize

Specifies the size in bytes of this DDCOMPBUFFERINFO structure.


### -field dwNumCompBuffers

Indicates the number of surfaces of this type required for decompression.


### -field dwWidthToCreate

Indicates the width in pixels of the surface of this type to create.


### -field dwHeightToCreate

Indicates the height in pixels of the surface of this type to create.


### -field dwBytesToAllocate

Indicates the total number of bytes used by each surface.


### -field ddCompCaps

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550292">DDSCAPS2</a> structure that contains the capabilities to use when creating surfaces of this type. This allows the driver to specify the type of memory to use when creating these surfaces.


### -field ddPixelFormat

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550274">DDPIXELFORMAT</a> structure that contains the pixel formats to use when creating surfaces of this type.


## -remarks



This structure passes this information to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551576">DD_GETMOCOMPCOMPBUFFDATA</a> structure.



