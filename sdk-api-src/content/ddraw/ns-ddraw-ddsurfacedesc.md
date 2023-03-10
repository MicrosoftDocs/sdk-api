---
UID: NS:ddraw._DDSURFACEDESC
title: DDSURFACEDESC
description: The DDSURFACEDESC structure contains a description of a surface to be created by the driver.
tech.root: directdraw
ms.date: 07/11/2022
targetos: Windows
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: ddraw.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: DDSURFACEDESC, *LPDDSURFACEDESC
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - ddraw.h
api_name:
 - _DDSURFACEDESC
 - LPDDSURFACEDESC
 - DDSURFACEDESC
f1_keywords:
 - _DDSURFACEDESC
 - ddraw/_DDSURFACEDESC
 - LPDDSURFACEDESC
 - ddraw/LPDDSURFACEDESC
 - DDSURFACEDESC
 - ddraw/DDSURFACEDESC
dev_langs:
 - c++
helpviewer_keywords:
 - _DDSURFACEDESC
---

## -description

The DDSURFACEDESC structure contains a description of a surface to be created by the driver.

## -struct-fields

### -field dwSize

Specifies the size in bytes of this DDSURFACEDESC structure. This member must be initialized before the structure is used.

### -field dwFlags

Specifies a set of flags that determine what members of the DDSURFACEDESC structure contain valid data. This member can be one or more of the following flags:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Flag</th>
<th>Meaning</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>DDSD_ALL</p></td>
<td><p>All input members contain valid data.</p></td>
</tr>
<tr class="even">
<td><p>DDSD_ALPHABITDEPTH</p></td>
<td><p>The <strong>dwAlphaBitDepth</strong> member is valid.</p></td>
</tr>
<tr class="odd">
<td><p>DDSD_BACKBUFFERCOUNT</p></td>
<td><p>The <strong>dwBackBufferCount</strong> member is valid.</p></td>
</tr>
<tr class="even">
<td><p>DDSD_CAPS</p></td>
<td><p>The <strong>ddsCaps</strong> member is valid.</p></td>
</tr>
<tr class="odd">
<td><p>DDSD_CKDESTBLT</p></td>
<td><p>The <strong>ddckCKDestBlt</strong> member is valid.</p></td>
</tr>
<tr class="even">
<td><p>DDSD_CKDESTOVERLAY</p></td>
<td><p>The <strong>ddckCKDestOverlay</strong> member is valid.</p></td>
</tr>
<tr class="odd">
<td><p>DDSD_CKSRCBLT</p></td>
<td><p>The <strong>ddckCKSrcBlt</strong> member is valid.</p></td>
</tr>
<tr class="even">
<td><p>DDSD_CKSRCOVERLAY</p></td>
<td><p>The <strong>ddckCKSrcOverlay</strong> member is valid.</p></td>
</tr>
<tr class="odd">
<td><p>DDSD_HEIGHT</p></td>
<td><p>The <strong>dwHeight</strong> member is valid.</p></td>
</tr>
<tr class="even">
<td><p>DDSD_LINEARSIZE</p></td>
<td><p>The <strong>dwLinearSize</strong> member is valid.</p></td>
</tr>
<tr class="odd">
<td><p>DDSD_MIPMAPCOUNT</p></td>
<td><p>The <strong>dwMipMapCount</strong> member is valid.</p></td>
</tr>
<tr class="even">
<td><p>DDSD_PITCH</p></td>
<td><p>The <strong>lPitch</strong> member is valid.</p></td>
</tr>
<tr class="odd">
<td><p>DDSD_PIXELFORMAT</p></td>
<td><p>The <strong>ddpfPixelFormat</strong> member is valid.</p></td>
</tr>
<tr class="even">
<td><p>DDSD_REFRESHRATE</p></td>
<td><p>The <strong>dwRefreshRate</strong> member is valid.</p></td>
</tr>
<tr class="odd">
<td><p>DDSD_WIDTH</p></td>
<td><p>The <strong>dwWidth</strong> member is valid.</p></td>
</tr>
<tr class="even">
<td><p>DDSD_ZBUFFERBITDEPTH</p></td>
<td><p>The <strong>dwZBufferBitDepth</strong> member is valid.</p></td>
</tr>
</tbody>
</table>

### -field dwHeight

Specifies the height of surface, in pixels.

### -field dwWidth

Specifies the width of the surface, in pixels.

### -field DUMMYUNIONNAMEN

N/A

### -field DUMMYUNIONNAMEN.lPitch

Specifies the number of bytes between the beginnings of two adjacent scan lines; that is, the number of bytes to add to the beginning address of one scan line to reach the beginning address of the next scan line below it. The driver's [DdCreateSurface](/windows/win32/api/ddrawint/nc-ddrawint-pdd_createsurface) callback must return this value.

### -field DUMMYUNIONNAMEN.dwLinearSize

Specifies the size in bytes of a formless, late-allocated, optimized surface.

### -field dwBackBufferCount

Specifies the number of back buffers associated with the surface.

### -field DUMMYUNIONNAMEN.dwMipMapCount

Specifies the number of mipmap levels.

### -field DUMMYUNIONNAMEN.dwZBufferBitDepth

Specifies the depth of z-buffer in bits per pixel.

### -field DUMMYUNIONNAMEN.dwRefreshRate

Specifies the refresh rate in hertz of the monitor (used when the display mode is described).

### -field dwAlphaBitDepth

Specifies the depth of the alpha buffer in bits per pixel.

### -field dwReserved

Reserved, and should be set to zero.

### -field lpSurface

Specifies the address of the associated surface memory.

### -field ddckCKDestOverlay

Specifies the color key for destination overlay use.

### -field ddckCKDestBlt

Specifies the color key for destination blt use.

### -field ddckCKSrcOverlay

Specifies the color key for source overlay use.

### -field ddckCKSrcBlt

Specifies the color key for source blt use.

### -field ddpfPixelFormat

Specifies a [DDPIXELFORMAT](/windows/win32/api/ddraw/ns-ddraw-ddpixelformat) structure that describes the pixel format of the surface.

### -field ddsCaps

Specifies a [DDSCAPS](ns-ddraw-ddscaps.md) structure that contains the Microsoft DirectDrawMicrosoft surface capabilities.

## -remarks

The relevant members differ for each potential type of surface. This structure is typically created and initialized by an application.

## -see-also

* [DdCreateSurface](/windows/win32/api/ddrawint/nc-ddrawint-pdd_createsurface)
* [DDPIXELFORMAT](/windows/win32/api/ddraw/ns-ddraw-ddpixelformat)
* [DDSCAPS](ns-ddraw-ddscaps.md)
