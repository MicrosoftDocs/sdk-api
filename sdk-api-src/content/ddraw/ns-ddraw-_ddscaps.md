---
UID: NS:ddraw._DDSCAPS
title: "_DDSCAPS"
author: windows-sdk-content
description: The DDSCAPS structure defines the capabilities of a DirectDrawSurface object. This structure is part of the DDCAPS and DDSURFACEDESC structures.
old-location: directdraw\ddscaps.htm
old-project: directdraw
ms.assetid: d7c4025c-dbb6-4182-b730-c69abd97f2bb
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: "*LPDDSCAPS, DDSCAPS, DDSCAPS structure [DirectDraw], DDSCAPS_3D, DDSCAPS_3DDEVICE, DDSCAPS_ALLOCONLOAD, DDSCAPS_ALPHA, DDSCAPS_BACKBUFFER, DDSCAPS_COMPLEX, DDSCAPS_FLIP, DDSCAPS_FRONTBUFFER, DDSCAPS_HWCODEC, DDSCAPS_LIVEVIDEO, DDSCAPS_LOCALVIDMEM, DDSCAPS_MIPMAP, DDSCAPS_MODEX, DDSCAPS_NONLOCALVIDMEM, DDSCAPS_OFFSCREENPLAIN, DDSCAPS_OPTIMIZED, DDSCAPS_OVERLAY, DDSCAPS_OWNDC, DDSCAPS_PALETTE, DDSCAPS_PRIMARYSURFACE, DDSCAPS_STANDARDVGAMODE, DDSCAPS_SYSTEMMEMORY, DDSCAPS_TEXTURE, DDSCAPS_VIDEOMEMORY, DDSCAPS_VIDEOPORT, DDSCAPS_VISIBLE, DDSCAPS_WRITEONLY, DDSCAPS_ZBUFFER, LPDDSCAPS, LPDDSCAPS structure pointer [DirectDraw], _DDSCAPS, ddraw/DDSCAPS, ddraw/LPDDSCAPS, directdraw.ddscaps"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ddraw.h
req.include-header: 
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
req.typenames: DDSCAPS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ddraw.h
api_name:
-	DDSCAPS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DDSCAPS structure


## -description


The <b>DDSCAPS</b> structure defines the capabilities of a DirectDrawSurface object. This structure is part of the <a href="https://msdn.microsoft.com/4ddda0a7-c0db-47cf-a908-959aabb530c6">DDCAPS</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff550339">DDSURFACEDESC</a> structures.




## -struct-fields




### -field dwCaps

Capabilities of the surface. The value in this member consists of one or more of the following flags combined with a bitwise OR:



#### DDSCAPS_3D

Unsupported. Use DDSCAPS_3DDEVICE, instead.



#### DDSCAPS_3DDEVICE

This surface can be used for 3-D rendering. Applications can use this flag to ensure that a device that can render only to a certain heap has off-screen surfaces allocated from the correct heap. If this flag is set for a heap, the surface is not allocated from that heap.



#### DDSCAPS_ALLOCONLOAD

Not used.



#### DDSCAPS_ALPHA

This surface contains alpha-only information.



#### DDSCAPS_BACKBUFFER

This surface is the back buffer of a surface flipping structure. Typically, this capability is set by the <a href="https://msdn.microsoft.com/library/windows/hardware/hh998978">CreateSurface</a> method when the DDSCAPS_FLIP flag is used. Only the surface that immediately precedes the DDSCAPS_FRONTBUFFER surface has this capability set. The other surfaces are identified as back buffers by the presence of the DDSCAPS_FLIP flag, their attachment order, and the absence of the DDSCAPS_FRONTBUFFER and DDSCAPS_BACKBUFFER capabilities. If this capability is sent to the <b>CreateSurface</b> method, a stand-alone back buffer is being created. After this method is called, this surface could be attached to a front buffer, another back buffer, or both to form a flipping surface structure. For more information, see <a href="https://msdn.microsoft.com/6d42c5ed-7f05-4450-b1f4-cb9ee6efa7d9">IDirectDrawSurface7::AddAttachedSurface</a>. DirectDraw supports any number of surfaces in a flipping structure.



#### DDSCAPS_COMPLEX

A complex surface is being described. A complex surface results in the creation of more than one surface. The additional surfaces are attached to the root surface. The complex surface can be destroyed only by destroying the root.



#### DDSCAPS_FLIP

This surface is a part of a surface flipping structure. When this capability is passed to the <a href="https://msdn.microsoft.com/library/windows/hardware/hh998978">CreateSurface</a> method, a front buffer and one or more back buffers are created. DirectDraw sets the DDSCAPS_FRONTBUFFER bit on the front-buffer surface and the DDSCAPS_BACKBUFFER bit on the surface adjacent to the front-buffer surface. The <b>dwBackBufferCount</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550339">DDSURFACEDESC</a> structure must be set to at least 1 for <b>CreateSurface</b> to succeed. The DDSCAPS_COMPLEX capability must always be set when creating multiple surfaces by using the <b>CreateSurface</b> method.



#### DDSCAPS_FRONTBUFFER

This surface is the front buffer of a surface flipping structure. This flag is typically set by the <a href="https://msdn.microsoft.com/library/windows/hardware/hh998978">CreateSurface</a> method when the DDSCAPS_FLIP capability is set. If this capability is sent to the <b>CreateSurface</b> method, a stand-alone front buffer is created. This surface does not have the DDSCAPS_FLIP capability. It can be attached to back buffers to form a flipping structure by using <a href="https://msdn.microsoft.com/6d42c5ed-7f05-4450-b1f4-cb9ee6efa7d9">IDirectDrawSurface7::AddAttachedSurface</a>.



#### DDSCAPS_HWCODEC

This surface can have a stream decompressed to it by the hardware.



#### DDSCAPS_LIVEVIDEO

This surface can receive live video.



#### DDSCAPS_LOCALVIDMEM

This surface exists in true, local video memory, rather than nonlocal video memory. If this flag is specified, DDSCAPS_VIDEOMEMORY must be specified, as well. This flag cannot be used with the DDSCAPS_NONLOCALVIDMEM flag.



#### DDSCAPS_MIPMAP

This surface is one level of a mipmap. This surface is attached to other DDSCAPS_MIPMAP surfaces to form the mipmap. This can be done explicitly by creating a number of surfaces and attaching them by using the <a href="https://msdn.microsoft.com/6d42c5ed-7f05-4450-b1f4-cb9ee6efa7d9">IDirectDrawSurface7::AddAttachedSurface</a> method, or implicitly by the <a href="https://msdn.microsoft.com/library/windows/hardware/hh998978">CreateSurface</a> method. If this capability is set, DDSCAPS_TEXTURE must also be set.



#### DDSCAPS_MODEX

This surface is a 320×200 or 320×240 Mode X surface.



#### DDSCAPS_NONLOCALVIDMEM

This surface exists in nonlocal video memory, rather than true, local video memory. If this flag is specified, the DDSCAPS_VIDEOMEMORY flag must be specified, as well. This cannot be used with the DDSCAPS_LOCALVIDMEM flag.



#### DDSCAPS_OFFSCREENPLAIN

This surface is any off-screen surface that is not an overlay, texture, z-buffer, front-buffer, back-buffer, or alpha surface. It is used to identify plain surfaces.



#### DDSCAPS_OPTIMIZED

Not used.



#### DDSCAPS_OVERLAY

This surface is an overlay. It might or might not be directly visible, depending on whether it is currently being overlaid onto the primary surface. DDSCAPS_VISIBLE can be used to determine if it is currently being overlaid.



#### DDSCAPS_OWNDC

This surface has a device context (DC) association for a long period of time.



#### DDSCAPS_PALETTE

This device driver allows unique DirectDrawPalette objects to be created and attached to this surface.



#### DDSCAPS_PRIMARYSURFACE

The surface is the primary surface. It represents what is currently visible.



#### DDSCAPS_STANDARDVGAMODE

This surface is a standard VGA mode surface, and not a Mode X surface. This flag cannot be used in combination with the DDSCAPS_MODEX flag.



#### DDSCAPS_SYSTEMMEMORY

This surface memory was allocated in system memory.



#### DDSCAPS_TEXTURE

This surface can be used as a 3-D texture. It does not indicate whether the surface is currently being used for that purpose.



#### DDSCAPS_VIDEOMEMORY

This surface exists in display memory.



#### DDSCAPS_VIDEOPORT

This surface can receive data from a video port.



#### DDSCAPS_VISIBLE

Changes made to this surface are immediately visible. It is always set for the primary surface, as well as for overlays while they are being overlaid and texture maps while they are being textured.



#### DDSCAPS_WRITEONLY

Only write access is permitted to the surface. Read access from the surface can cause a general protection (GP) fault, but the read results from this surface would be meaningful.



#### DDSCAPS_ZBUFFER

This surface is the z-buffer. The z-buffer contains information that cannot be displayed. Instead, it contains bit-depth information that is used to determine which pixels are visible and which are obscured.

