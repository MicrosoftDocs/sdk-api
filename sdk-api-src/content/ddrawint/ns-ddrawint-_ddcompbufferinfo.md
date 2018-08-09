---
UID: NS:ddrawint._DDCOMPBUFFERINFO
title: "_DDCOMPBUFFERINFO"
author: windows-sdk-content
description: The DDCOMPBUFFERINFO structure contains driver-supplied information regarding compression buffers.
old-location: display\ddcompbufferinfo.htm
old-project: display
ms.assetid: 73dad759-499f-45b2-9345-4577deb01492
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: "*LPDDCOMPBUFFERINFO, DDCOMPBUFFERINFO, DDCOMPBUFFERINFO structure [Display Devices], LPDDCOMPBUFFERINFO, LPDDCOMPBUFFERINFO structure pointer [Display Devices], _DDCOMPBUFFERINFO, ddrawint/DDCOMPBUFFERINFO, ddrawint/LPDDCOMPBUFFERINFO, ddstrcts_b9871578-f3de-49fb-95f3-2668598e575a.xml, display.ddcompbufferinfo"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ddrawint.h
req.include-header: Winddi.h
req.target-type: Windows
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
tech.root: 
req.typenames: DDCOMPBUFFERINFO, *LPDDCOMPBUFFERINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddrawint.h
api_name:
 - DDCOMPBUFFERINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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



