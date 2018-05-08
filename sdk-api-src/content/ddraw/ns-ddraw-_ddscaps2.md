---
UID: NS:ddraw._DDSCAPS2
title: "_DDSCAPS2"
author: windows-driver-content
description: The DDSCAPS2 structure defines the capabilities of a DirectDrawSurface object. This structure is part of the DDSURFACEDESC2 structure.
old-location: directdraw\ddscaps2.htm
old-project: directdraw
ms.assetid: a2fd448c-0ae1-43cd-8561-77d537b741e7
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: "*LPDDSCAPS2, DDSCAPS2, DDSCAPS2 structure [DirectDraw], DDSCAPS2_CUBEMAP, DDSCAPS2_CUBEMAP_ALLFACES, DDSCAPS2_CUBEMAP_NEGATIVEX, DDSCAPS2_CUBEMAP_NEGATIVEY, DDSCAPS2_CUBEMAP_NEGATIVEZ, DDSCAPS2_CUBEMAP_POSITIVEX, DDSCAPS2_CUBEMAP_POSITIVEY, DDSCAPS2_CUBEMAP_POSITIVEZ, DDSCAPS2_D3DTEXTUREMANAGE, DDSCAPS2_DONOTPERSIST, DDSCAPS2_HARDWAREDEINTERLACE, DDSCAPS2_HINTANTIALIASING, DDSCAPS2_HINTDYNAMIC, DDSCAPS2_HINTSTATIC, DDSCAPS2_MIPMAPSUBLEVEL, DDSCAPS2_OPAQUE, DDSCAPS2_STEREOSURFACELEFT, DDSCAPS2_TEXTUREMANAGE, DDSCAPS_3D, DDSCAPS_3DDEVICE, DDSCAPS_ALLOCONLOAD, DDSCAPS_ALPHA, DDSCAPS_BACKBUFFER, DDSCAPS_COMPLEX, DDSCAPS_FLIP, DDSCAPS_FRONTBUFFER, DDSCAPS_HWCODEC, DDSCAPS_LIVEVIDEO, DDSCAPS_LOCALVIDMEM, DDSCAPS_MIPMAP, DDSCAPS_MODEX, DDSCAPS_NONLOCALVIDMEM, DDSCAPS_OFFSCREENPLAIN, DDSCAPS_OPTIMIZED, DDSCAPS_OVERLAY, DDSCAPS_OWNDC, DDSCAPS_PALETTE, DDSCAPS_PRIMARYSURFACE, DDSCAPS_STANDARDVGAMODE, DDSCAPS_SYSTEMMEMORY, DDSCAPS_TEXTURE, DDSCAPS_VIDEOMEMORY, DDSCAPS_VIDEOPORT, DDSCAPS_VISIBLE, DDSCAPS_WRITEONLY, DDSCAPS_ZBUFFER, LPDDSCAPS2, LPDDSCAPS2 structure pointer [DirectDraw], _DDSCAPS2, ddraw/DDSCAPS2, ddraw/LPDDSCAPS2, directdraw.ddscaps2"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: DDSCAPS2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ddraw.h
api_name:
-	DDSCAPS2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DDSCAPS2 structure


## -description


The <b>DDSCAPS2</b> structure defines the capabilities of a DirectDrawSurface object. This structure is part of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550340">DDSURFACEDESC2</a> structure.


<div class="alert"><b>Note</b>  Rather than use this structure to decode files with the DirectDraw Surface (DDS) file format (.dds), you should use an alternative structure that does not rely on Ddraw.h. For more information about alternative structures for DDS, see <a href="https://msdn.microsoft.com/b0f3a1af-e816-4d64-93d9-51e510423869">DDS</a>.</div><div> </div>

## -struct-fields




### -field dwCaps

One or more of the following flag values that represent the capabilities of the surface. (The flags in this member are identical to those in the corresponding member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550286">DDSCAPS</a> structure.)



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


### -field dwCaps2

Additional surface capabilities. This member can contain one or more of the following capability flags, or when you use this structure with the <a href="https://msdn.microsoft.com/541bd833-20c4-4b47-a3ed-c29f228a0626">IDirectDrawSurface7::SetSurfaceDesc</a> method, this member can contain an additional flag to indicate how the surface memory was allocated:



#### DDSCAPS2_CUBEMAP

New for DirectX 7.0. This surface is a cubic environment map. When you use this flag, also specify which face or faces of the cubic environment map to create.



#### DDSCAPS2_CUBEMAP_POSITIVEX

New for DirectX 7.0. This flag is used with the DDSCAPS2_CUBEMAP flag to create the positive X face of a cubic environment map. 




#### DDSCAPS2_CUBEMAP_NEGATIVEX

New for DirectX 7.0. This flag is used with the DDSCAPS2_CUBEMAP flag to create the negative X face of a cubic environment map.



#### DDSCAPS2_CUBEMAP_POSITIVEY

New for DirectX 7.0. This flag is used with the DDSCAPS2_CUBEMAP flag to create the positive Y face of a cubic environment map.



#### DDSCAPS2_CUBEMAP_NEGATIVEY

New for DirectX 7.0. This flag is used with the DDSCAPS2_CUBEMAP flag to create the negative Y face of a cubic environment map.



#### DDSCAPS2_CUBEMAP_POSITIVEZ

New for DirectX 7.0. This flag is used with the DDSCAPS2_CUBEMAP flag to create the positive Z face of a cubic environment map.



#### DDSCAPS2_CUBEMAP_NEGATIVEZ

New for DirectX 7.0. This flag is used with the DDSCAPS2_CUBEMAP flag to create the negative Z face of a cubic environment map.



#### DDSCAPS2_CUBEMAP_ALLFACES

New for DirectX 7.0. This flag is used with the DDSCAPS2_CUBEMAP flag to create all six faces of a cubic environment map.



#### DDSCAPS2_D3DTEXTUREMANAGE

New for DirectX 7.0. The texture is always managed by Direct3D.



#### DDSCAPS2_DONOTPERSIST

New for DirectX 7.0. The managed surface can be safely lost.



#### DDSCAPS2_HARDWAREDEINTERLACE

This surface receives data from a video port, using the de-interlacing hardware. This allows the driver to allocate memory for any extra buffers that might be required. The DDSCAPS_VIDEOPORT and DDSCAPS_OVERLAY flags must also be set.



#### DDSCAPS2_HINTANTIALIASING

The application intends to use antialiasing. Only valid if DDSCAPS_3DDEVICE is also set.



#### DDSCAPS2_HINTDYNAMIC

Indicates to the driver that this surface is locked very frequently (for procedural textures, dynamic light maps, and so on). This flag can only be used for texture surfaces (DDSCAPS_TEXTURE flag set in the <b>dwCaps</b> member). This flag cannot be used with the DDSCAPS2_HINTSTATIC or DDSCAPS2_OPAQUE flags.



#### DDSCAPS2_HINTSTATIC

Indicates to the driver that this surface can be reordered or retiled on load. This operation does not change the size of the texture. It is relatively fast and symmetrical, since the application can lock these bits (although it degrades performance when doing so). This flag can only be used for texture surfaces (DDSCAPS_TEXTURE flag set in the <b>dwCaps</b> member). This flag cannot be used with the DDSCAPS2_HINTDYNAMIC or DDSCAPS2_OPAQUE flags.



#### DDSCAPS2_MIPMAPSUBLEVEL

New for DirectX 7.0. It enables easier use of <a href="https://msdn.microsoft.com/0eae7e55-5ff7-41f6-ac6a-ce7fb6d809b9">GetAttachedSurface</a>, rather than <a href="https://msdn.microsoft.com/7f8e9b53-3aff-491c-ab0c-2f414d1ddb27">EnumAttachedSurfaces</a>, for surface constructs such as cube maps, in which there is more than one mipmap surface attached to the root surface. This should be set on all non-top-level surfaces in a mipmapped cube map so that a call to <b>GetAttachedSurface</b> can distinguish between top-level faces and attached mipmap levels. This capability bit is ignored by <a href="https://msdn.microsoft.com/library/windows/hardware/hh998978">CreateSurface</a>.



#### DDSCAPS2_OPAQUE

Indicates to the driver that this surface will never be locked again. The driver is free to optimize this surface by retiling and compression. Such a surface cannot be locked or used in bit-block transfer (bitblt) operations; attempts to lock or bitblt a surface with this capability fail. This flag can only be used for texture surfaces (DDSCAPS_TEXTURE flag set in the dwCaps member). This flag cannot be used with the DDSCAPS2_HINTDYNAMIC or DDSCAPS2_HINTSTATIC flags.



#### DDSCAPS2_STEREOSURFACELEFT

New for DirectX 7.0. This surface is part of a stereo flipping chain. When this flag is set during a <a href="https://msdn.microsoft.com/4f27e36f-d04f-43ce-9a3d-64c352c8f8d8">IDirectDraw7::CreateSurface</a> call, a pair of stereo surfaces are created for each buffer in the primary flipping chain. You must create a complex flipping chain (with back buffers). You cannot create a single set of stereo surfaces. The <a href="https://msdn.microsoft.com/6c0c23e7-7567-4e07-9ba0-5e50b758f711">IDirectDrawSurface7::Flip</a> method requires back buffers, so at least 4 surfaces must be created.

In addition, when this flag is set in a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550339">DDSURFACEDESC</a> structure as the result of an <a href="https://msdn.microsoft.com/04ed2545-c611-435d-95ef-a0d854380a69">IDirectDraw7::EnumDisplayModes</a> or <a href="https://msdn.microsoft.com/bd31efc8-17c4-4744-a03b-a22a50c7d9c2">IDirectDraw7::GetDisplayMode</a> call, it indicates support for stereo in that mode.



#### DDSCAPS2_TEXTUREMANAGE

The client would like this texture surface to be managed by the driver if the driver is capable; otherwise, it is managed by Direct3D Immediate Mode (new in DirectX 7.0). This flag can be used only for texture surfaces (DDSCAPS_TEXTURE flag set in the <b>dwCaps</b> member). Do not use this flag if your application uses Direct3D Retained Mode. Instead, create textures in system memory, and allow Retained Mode to manage them.


### -field dwCaps3

Not used.


### -field DUMMYUNIONNAMEN

 


### -field DUMMYUNIONNAMEN.dwCaps4

 


### -field DUMMYUNIONNAMEN.dwVolumeDepth

 




#### - DUMMYUNIONNAMEN(1)



#### dwCaps4

Not used.



#### dwVolumeDepth

Not used.

