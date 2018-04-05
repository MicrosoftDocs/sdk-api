---
UID: NS:ddraw._DDSURFACEDESC
title: "_DDSURFACEDESC"
author: windows-driver-content
description: Do not use. This structure is superseded by the DDSURFACEDESC2 structure that is used with the IDirectDraw7 and IDirectDrawSurface7 interfaces.
old-location: directdraw\ddsurfacedesc.htm
old-project: directdraw
ms.assetid: a88f37bc-b5c0-4bc1-b6ee-30923362c1ca
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: "*LPDDSURFACEDESC, DDSD_ALL, DDSD_ALPHABITDEPTH, DDSD_BACKBUFFERCOUNT, DDSD_CAPS, DDSD_CKDESTBLT, DDSD_CKDESTOVERLAY, DDSD_CKSRCBLT, DDSD_CKSRCOVERLAY, DDSD_HEIGHT, DDSD_LINEARSIZE, DDSD_LPSURFACE, DDSD_MIPMAPCOUNT, DDSD_PITCH, DDSD_PIXELFORMAT, DDSD_REFRESHRATE, DDSD_WIDTH, DDSD_ZBUFFERBITDEPTH, DDSURFACEDESC, DDSURFACEDESC structure [DirectDraw], LPDDSURFACEDESC, LPDDSURFACEDESC structure pointer [DirectDraw], _DDSURFACEDESC, ddraw/DDSURFACEDESC, ddraw/LPDDSURFACEDESC, directdraw.ddsurfacedesc"
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
req.typenames: "*LPDDSURFACEDESC, DDSURFACEDESC"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ddraw.h
api_name:
-	DDSURFACEDESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DDSURFACEDESC structure


## -description


Do not use. This structure is superseded by the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550340">DDSURFACEDESC2</a> structure that is used with the <a href="https://msdn.microsoft.com/1a1164fe-00c2-4469-8346-f86f7f48781e">IDirectDraw7</a> and <a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a> interfaces.


## -struct-fields




### -field DUMMYUNIONNAMEN

 


### -field dwSize

Size of the structure, in bytes. This member must be initialized before the structure is used.


### -field dwFlags

The following flags to describe optional controls for this structure:



#### DDSD_ALL

All input members are valid.



#### DDSD_ALPHABITDEPTH

The <b>dwAlphaBitDepth</b> member is valid.



#### DDSD_BACKBUFFERCOUNT

The <b>dwBackBufferCount</b> member is valid.



#### DDSD_CAPS

The <b>ddsCaps</b> member is valid.



#### DDSD_CKDESTBLT

The <b>ddckCKDestBlt</b> member is valid.



#### DDSD_CKDESTOVERLAY

The <b>ddckCKDestOverlay</b> member is valid.



#### DDSD_CKSRCBLT

The <b>ddckCKSrcBlt</b> member is valid.



#### DDSD_CKSRCOVERLAY

The <b>ddckCKSrcOverlay</b> member is valid.



#### DDSD_HEIGHT

The <b>dwHeight</b> member is valid.



#### DDSD_LINEARSIZE

The <b>dwLinearSize</b> member is valid.



#### DDSD_LPSURFACE

The <b>lpSurface</b> member is valid.



#### DDSD_MIPMAPCOUNT

The <b>dwMipMapCount</b> member is valid.



#### DDSD_PITCH

The <b>lPitch</b> member is valid.



#### DDSD_PIXELFORMAT

The <b>ddpfPixelFormat</b> member is valid.



#### DDSD_REFRESHRATE

The <b>dwRefreshRate</b> member is valid.



#### DDSD_WIDTH

The <b>dwWidth</b> member is valid.



#### DDSD_ZBUFFERBITDEPTH

The <b>dwZBufferBitDepth</b> member is valid.


### -field dwHeight

Height of the surface to be created, in pixels.


### -field dwWidth

Width of the surface to be created, in pixels.


### -field dwBackBufferCount

Number of back buffers.


### -field dwAlphaBitDepth

Depth of the alpha buffer.


### -field dwReserved

Reserved


### -field lpSurface

Address of the associated surface memory. When calling <a href="https://msdn.microsoft.com/0267ad70-e7cc-41e8-8325-7ede4a662d13">IDirectDrawSurface7::Lock</a>, this member contains a valid pointer to surface memory after the call returns. When creating a surface from existing memory or using the <a href="https://msdn.microsoft.com/541bd833-20c4-4b47-a3ed-c29f228a0626">IDirectDrawSurface7::SetSurfaceDesc</a> method, this member is an input value that is the address of system memory allocated by the calling application. Do not set this member if your application needs DirectDraw to allocate and manage surface memory.


### -field ddckCKDestOverlay

A <a href="https://msdn.microsoft.com/c520e649-86f9-4c4a-bb67-22d75aa3c8b0">DDCOLORKEY</a> structure that describes the destination color key for an overlay surface.


### -field ddckCKDestBlt

A <a href="https://msdn.microsoft.com/c520e649-86f9-4c4a-bb67-22d75aa3c8b0">DDCOLORKEY</a> structure that describes the destination color key for bit-block transfer (bitblt) operations.


### -field ddckCKSrcOverlay

A <a href="https://msdn.microsoft.com/c520e649-86f9-4c4a-bb67-22d75aa3c8b0">DDCOLORKEY</a> structure that describes the source color key for an overlay surface.


### -field ddckCKSrcBlt

A <a href="https://msdn.microsoft.com/c520e649-86f9-4c4a-bb67-22d75aa3c8b0">DDCOLORKEY</a> structure that describes the source color key for bitblt operations.


### -field ddpfPixelFormat

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff550274">DDPIXELFORMAT</a> structure that describes the surface's pixel format.


### -field ddsCaps

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff550286">DDSCAPS</a> structure that contains the surface's capabilities.


#### - DUMMYUNIONNAMEN(1)



#### lPitch

Distance, in bytes, to the start of the next line. When used with the <a href="https://msdn.microsoft.com/4c36685e-8eb7-4d91-a479-8f099d5e712b">IDirectDrawSurface7::GetSurfaceDesc</a> method, this is a return value. When creating a surface from existing memory or when calling the <a href="https://msdn.microsoft.com/541bd833-20c4-4b47-a3ed-c29f228a0626">IDirectDrawSurface7::SetSurfaceDesc</a> method, this is an input value that must be a DWORD multiple.



#### dwLinearSize

Size of the buffer. Currently returned only for compressed texture surfaces.


#### - DUMMYUNIONNAMEN(2)



#### dwMipMapCount

Number of mipmap levels.



#### dwZBufferBitDepth

Depth of the z-buffer. This member is obsolete for DirectX 6.0 and later. Use the <b>IDirect3D7::EnumZBufferFormats</b> method to retrieve information about supported depth-buffer formats.



#### dwRefreshRate

Refresh rate (used when the display mode is described). The value of 0 indicates an adapter default.


## -remarks



This structure is similar to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550340">DDSURFACEDESC2</a> structure, but contains a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550286">DDSCAPS</a> structure as the <b>ddsCaps</b> member, rather than a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550292">DDSCAPS2</a> structure. Unlike <b>DDSURFACEDESC2</b>, this structure contains the <b>dwZBufferBitDepth</b> member.





