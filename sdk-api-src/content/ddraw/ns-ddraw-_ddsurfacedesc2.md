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

# _DDSURFACEDESC2 structure


## -description


The <b>DDSURFACEDESC2</b> structure contains a description of a surface. This structure is used to pass surface parameters to the <a href="https://msdn.microsoft.com/4f27e36f-d04f-43ce-9a3d-64c352c8f8d8">IDirectDraw7::CreateSurface</a> and <a href="https://msdn.microsoft.com/541bd833-20c4-4b47-a3ed-c29f228a0626">IDirectDrawSurface7::SetSurfaceDesc</a> methods. It is also used to retrieve information about a surface in calls to <a href="https://msdn.microsoft.com/0267ad70-e7cc-41e8-8325-7ede4a662d13">IDirectDrawSurface7::Lock</a> and <a href="https://msdn.microsoft.com/4c36685e-8eb7-4d91-a479-8f099d5e712b">IDirectDrawSurface7::GetSurfaceDesc</a>. The relevant members differ for each potential type of surface.
<div class="alert"><b>Note</b>  Rather than use this structure to decode files with the DirectDraw Surface (DDS) file format (.dds), you should use an alternative structure that does not rely on Ddraw.h. For more information about alternative structures for DDS, see <a href="https://msdn.microsoft.com/b0f3a1af-e816-4d64-93d9-51e510423869">DDS</a>.</div><div> </div>

## -struct-fields




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



#### DDSD_TEXTURESTAGE

The <b>dwTextureStage</b> member is valid.



#### DDSD_WIDTH

The <b>dwWidth</b> member is valid.



#### DDSD_ZBUFFERBITDEPTH

Obsolete; see Remarks.


### -field dwHeight

Height of the surface to be created, in pixels.


### -field dwWidth

Width of the surface to be created, in pixels.


### -field DUMMYUNIONNAMEN.lPitch

 


### -field DUMMYUNIONNAMEN.dwLinearSize

 


### -field DUMMYUNIONNAMEN.dwBackBufferCount

 


### -field DUMMYUNIONNAMEN.dwDepth

 


### -field DUMMYUNIONNAMEN.dwMipMapCount

 


### -field DUMMYUNIONNAMEN.dwRefreshRate

 


### -field DUMMYUNIONNAMEN.dwSrcVBHandle

 


### -field dwAlphaBitDepth

Depth of the alpha buffer.


### -field dwReserved

Reserved


### -field lpSurface

Address of the associated surface memory. When calling <a href="https://msdn.microsoft.com/0267ad70-e7cc-41e8-8325-7ede4a662d13">IDirectDrawSurface7::Lock</a>, this member contains a valid pointer to surface memory after the call returns. When creating a surface from existing memory or using the <a href="https://msdn.microsoft.com/541bd833-20c4-4b47-a3ed-c29f228a0626">IDirectDrawSurface7::SetSurfaceDesc</a> method, this member is an input value that is the address of system memory allocated by the calling application. Do not set this member if your application needs DirectDraw to allocate and manage surface memory.


### -field DUMMYUNIONNAMEN.ddckCKDestOverlay

 


### -field DUMMYUNIONNAMEN.dwEmptyFaceColor

 


### -field ddckCKDestBlt

A <a href="https://msdn.microsoft.com/c520e649-86f9-4c4a-bb67-22d75aa3c8b0">DDCOLORKEY</a> structure that describes the destination color key for bit-block transfer (bitblt) operations.


### -field ddckCKSrcOverlay

A <a href="https://msdn.microsoft.com/c520e649-86f9-4c4a-bb67-22d75aa3c8b0">DDCOLORKEY</a> structure that describes the source color key for an overlay surface.


### -field ddckCKSrcBlt

A <a href="https://msdn.microsoft.com/c520e649-86f9-4c4a-bb67-22d75aa3c8b0">DDCOLORKEY</a> structure that describes the source color key for bitblt operations.


### -field DUMMYUNIONNAMEN

 


### -field DUMMYUNIONNAMEN.ddpfPixelFormat

 


### -field DUMMYUNIONNAMEN.dwFVF

 


### -field ddsCaps

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff550292">DDSCAPS2</a> structure that contains the surface's capabilities.


### -field dwTextureStage

Stage identifier that is used to bind a texture to a specific stage in a multitexture cascade 3-D device. Although not required for all hardware, you should set this member for best performance on the largest variety of 3-D accelerators. Hardware that requires explicitly assigned textures exposes the D3DDEVCAPS_SEPARATETEXTUREMEMORIES 3-D device capability in the <b>DEVCAPS</b> member of the <a href="https://msdn.microsoft.com/44457b7b-a1f7-4019-b971-8ec2334d3313">D3DCAPS9</a> structure that is filled by the <a href="https://msdn.microsoft.com/9ac080df-963b-4e29-b200-f74ff3bb6db8">GetDeviceCaps</a> method.


#### - DUMMYUNIONNAMEN(1)



#### lPitch

Distance, in bytes, to the start of the next line. When used with the <a href="https://msdn.microsoft.com/4c36685e-8eb7-4d91-a479-8f099d5e712b">IDirectDrawSurface7::GetSurfaceDesc</a> method, this is a return value. When creating a surface from existing memory or when calling the <a href="https://msdn.microsoft.com/541bd833-20c4-4b47-a3ed-c29f228a0626">IDirectDrawSurface7::SetSurfaceDesc</a> method, this is an input value that must be a DWORD multiple. For more information, see Remarks.



#### dwLinearSize

Size of the buffer. Currently returned only for compressed texture surfaces.


#### - DUMMYUNIONNAMEN(2)



#### dwMipMapCount

Number of mipmap levels.



#### dwRefreshRate

Refresh rate (used when the display mode is described). The value of 0 indicates an adapter default.



#### dwSrcVBHandle

Not used.


#### - DUMMYUNIONNAMEN(3)



#### ddckCKDestOverlay

A <a href="https://msdn.microsoft.com/c520e649-86f9-4c4a-bb67-22d75aa3c8b0">DDCOLORKEY</a> structure that describes the destination color key for an overlay surface.



#### dwEmptyFaceColor

Physical color for empty cubemap faces.


#### - DUMMYUNIONNAMEN(4)



#### ddpfPixelFormat

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff550274">DDPIXELFORMAT</a> structure that describes the surface's pixel format.



#### dwFVF

Vertex format description of vertex buffers.


#### - DUMMYUNIONNAMEN(5)



#### dwBackBufferCount

Number of back buffers.



#### dwDepth

The depth, in pixels, of the surface if it is a volume texture.


## -remarks



The <b>lPitch</b> and <b>lpSurface</b> members are output values when you call the <a href="https://msdn.microsoft.com/4c36685e-8eb7-4d91-a479-8f099d5e712b">IDirectDrawSurface7::GetSurfaceDesc</a> method. When you create surfaces from existing memory or update surface characteristics, these members are input values that describe the pitch and location of memory that was allocated by the calling application for use by DirectDraw. DirectDraw does not attempt to manage or free memory that was allocated by the application.

This structure is nearly identical to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550339">DDSURFACEDESC</a> structure, but contains a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550292">DDSCAPS2</a> structure as the <b>ddsCaps</b> member. Unlike <b>DDSURFACEDESC</b>, this structure does not contain the <b>dwZBufferBitDepth</b> member. Z-buffer depth is provided in the <b>ddpfPixelFormat</b> member.

The unions in this structure work with compilers that do not support nameless unions. If your compiler does not support nameless unions, define the NONAMELESSUNION token before including the Ddraw.h header file.





