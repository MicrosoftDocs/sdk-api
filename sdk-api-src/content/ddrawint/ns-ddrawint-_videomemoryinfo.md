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

# _VIDEOMEMORYINFO structure


## -description


The VIDEOMEMORYINFO structure describes the general format of the display's memory.


## -struct-fields




### -field fpPrimary

Specifies the offset, in bytes, in display memory to the primary surface.


### -field dwFlags

Currently unused and should be set to zero.


### -field dwDisplayWidth

Specifies the current width of the display, in pixels.


### -field dwDisplayHeight

Specifies the current height of the display, in pixels.


### -field lDisplayPitch

Specifies the current pitch of the display, in bytes.


### -field ddpfDisplay

Specifies a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550274">DDPIXELFORMAT</a> structure in which the pixel format of the display is described. 


### -field dwOffscreenAlign

Specifies the byte alignment, in bytes, required when allocating this memory for offscreen surfaces.


### -field dwOverlayAlign

Specifies the byte alignment, in bytes, required when allocating this memory for overlay planes.


### -field dwTextureAlign

Specifies the byte alignment, in bytes, required when allocating this memory for textures.


### -field dwZBufferAlign

Specifies the byte alignment, in bytes, required when allocating this memory for the depth buffer.


### -field dwAlphaAlign

Specifies the byte alignment, in bytes, required when allocating this memory for an alpha buffer.


### -field pvPrimary

(Microsoft Windows 2000 and later only) 

Specifies a kernel-mode pointer to the beginning of the primary surface. 


#### - dwNumHeaps

(Windows 98/Me only)

Specifies the number of memory heaps in <b>pvmList</b>. 


#### - pvmList

(Windows 98/Me only) 

Points to the first heap in an array of heaps.


## -remarks



The VIDEOMEMORYINFO structure has minor differences between Windows 98/Me and Windows 2000 and later. On Windows 2000 and later the data structure is called VIDEOMEMORYINFO and on Windows 98/Me the data structure is called VIDMEMINFO. On Windows 2000 and later, VIDEOMEMORYINFO includes a field <b>pvPrimary</b> that stores a kernel-mode pointer to the primary surface. On Windows 98/Me, VIDMEMINFO includes the fields <b>dwNumHeaps</b> and <b>pvmList</b> that specify an array of memory heaps.

GDI allocates memory for and passes a VIDEOMEMORYINFO structure to the driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff556229">DrvGetDirectDrawInfo</a> function as a member of the DD_HALINFO parameter. The driver should fill in the appropriate members to describe the general characteristics of the device's memory.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550274">DDPIXELFORMAT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556229">DrvGetDirectDrawInfo</a>
 

 

