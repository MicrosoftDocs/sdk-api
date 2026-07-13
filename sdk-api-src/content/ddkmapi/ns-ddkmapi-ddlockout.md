---
UID: NS:ddkmapi._DDLOCKOUT
title: DDLOCKOUT (ddkmapi.h)
description: The DDLOCKOUT structure contains a description of the surface.
helpviewer_keywords: ["*LPDDLOCKOUT","DDLOCKOUT","DDLOCKOUT structure [Display Devices]","LPDDLOCKOUT","LPDDLOCKOUT structure pointer [Display Devices]","ddkmapi/DDLOCKOUT","ddkmapi/LPDDLOCKOUT","ddstrcts_7125d1f6-8fc5-460b-bc11-089053f77b83.xml","display.ddlockout"]
old-location: display\ddlockout.htm
tech.root: display
ms.assetid: b6046c49-828d-4b92-aab7-e872e1905929
ms.date: 12/05/2018
ms.keywords: '*LPDDLOCKOUT, DDLOCKOUT, DDLOCKOUT structure [Display Devices], LPDDLOCKOUT, LPDDLOCKOUT structure pointer [Display Devices], ddkmapi/DDLOCKOUT, ddkmapi/LPDDLOCKOUT, ddstrcts_7125d1f6-8fc5-460b-bc11-089053f77b83.xml, display.ddlockout'
req.header: ddkmapi.h
req.include-header: Ddkmapi.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DDLOCKOUT, *LPDDLOCKOUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDLOCKOUT
 - ddkmapi/_DDLOCKOUT
 - LPDDLOCKOUT
 - ddkmapi/LPDDLOCKOUT
 - DDLOCKOUT
 - ddkmapi/DDLOCKOUT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddkmapi.h
api_name:
 - DDLOCKOUT
---

# DDLOCKOUT structure


## -description

The DDLOCKOUT structure contains a description of the surface.

## -struct-fields

### -field ddRVal

Specifies the location in which Microsoft DirectDraw writes the return value of the <a href="/previous-versions/windows/drivers/display/nf-dxapi-dxapi">DxApi</a> function for <a href="/previous-versions/windows/hardware/drivers/ff550695(v=vs.85)">DD_DXAPI_LOCK</a> operations. A return code of DD_OK indicates success.

### -field dwSurfHeight

### -field dwSurfWidth

Specify the dimensions of the surface, in pixels.

### -field lSurfPitch

Specifies the distance, in bytes, to the start of the next line.

### -field lpSurface

Points to the surface memory.

### -field SurfaceCaps

Indicates a set of flags that specify the capabilities of the surface. This member can be set to one or more of the following flags: 

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDSCAPS_3DDEVICE

</td>
<td>
This surface can be used for 3D rendering. Applications can use this flag to ensure that a device that can only render to a certain heap has offscreen surfaces allocated from the correct heap. If this flag is set for a heap, the surface is not allocated from that heap.

</td>
</tr>
<tr>
<td>
DDSCAPS_ALLOCONLOAD

</td>
<td>
Memory for the surface is not allocated until the surface is loaded by the application using the <b>IDirect3DDevice7::Load</b> method.

</td>
</tr>
<tr>
<td>
DDSCAPS_ALPHA

</td>
<td>
This surface contains alpha information. The pixel format must be queried to determine whether this surface contains only alpha information or alpha information interlaced with pixel color data (such as RGBA or YUVA).

</td>
</tr>
<tr>
<td>
DDSCAPS_BACKBUFFER

</td>
<td>
This surface is the back buffer of a surface flipping structure. Typically, this capability is set by the application's <b>CreateSurface</b> method when the DDSCAPS_FLIP flag is used. Only the surface that immediately precedes the DDSCAPS_FRONTBUFFER surface has this capability set. The other surfaces are identified as back buffers by the presence of the DDSCAPS_FLIP flag, their attachment order, and the absence of the DDSCAPS_FRONTBUFFER and DDSCAPS_BACKBUFFER capabilities. If this capability is sent to the application's <b>CreateSurface</b> method, a stand-alone back buffer is being created. After this method is called, this surface could be attached to a front buffer, another back buffer, or both to form a flipping surface structure. For more information, see the <b>AddAttachedSurface</b> method in the DirectX SDK documentation. DirectDraw supports an arbitrary number of surfaces in a flipping structure.

</td>
</tr>
<tr>
<td>
DDSCAPS_COMPLEX

</td>
<td>
A complex surface is being described. A complex surface results in the creation of more than one surface. The additional surfaces are attached to the root surface. The complex structure can be destroyed only by destroying the root.

</td>
</tr>
<tr>
<td>
DDSCAPS_FLIP

</td>
<td>
This surface is a part of a surface flipping structure. When this capability is passed to the application's <b>CreateSurface</b> method, a front buffer and one or more back buffers are created. DirectDraw sets the DDSCAPS_FRONTBUFFER bit on the front-buffer surface and the DDSCAPS_BACKBUFFER bit on the surface adjacent to the front-buffer surface. The <b>dwBackBufferCount</b> member of the <a href="/windows/win32/api/ddraw/ns-ddraw-ddsurfacedesc">DDSURFACEDESC</a> structure must be set to at least 1 in order for the method call to succeed. The DDSCAPS_COMPLEX capability must always be set when creating multiple surfaces by using the <b>CreateSurface</b> method. 

</td>
</tr>
<tr>
<td>
DDSCAPS_FRONTBUFFER

</td>
<td>
This surface is the front buffer of a surface flipping structure. This flag is typically set by the application's <b>CreateSurface</b> method when the DDSCAPS_FLIP capability is set. If this capability is sent to the <b>CreateSurface</b> method, a stand-alone front buffer is created. This surface will not have the DDSCAPS_FLIP capability. It can be attached to other back buffers to form a flipping structure by using the application's <b>AddAttachedSurface</b> method.

</td>
</tr>
<tr>
<td>
DDSCAPS_HWCODEC

</td>
<td>
This surface should be able to have a stream decompressed to it by the hardware.

</td>
</tr>
<tr>
<td>
DDSCAPS_LIVEVIDEO

</td>
<td>
This surface should be able to receive live video.

</td>
</tr>
<tr>
<td>
DDSCAPS_LOCALVIDMEM

</td>
<td>
This surface exists in true, local display memory rather than nonlocal display memory. If this flag is specified then DDSCAPS_VIDEOMEMORY must be specified as well. This flag cannot be used with the DDSCAPS_NONLOCALVIDMEM flag.

</td>
</tr>
<tr>
<td>
DDSCAPS_MIPMAP

</td>
<td>
This surface is one level of a mipmap. This surface will be attached to other DDSCAPS_MIPMAP surfaces to form the mipmap. This can be done explicitly by creating a number of surfaces and attaching them by using the application's <b>AddAttachedSurface</b> method, or implicitly by the application's <b>CreateSurface</b> method. If this capability is set, DDSCAPS_TEXTURE must also be set.

</td>
</tr>
<tr>
<td>
DDSCAPS_MODEX

</td>
<td>
This surface is a 320x200 or 320x240 Mode X surface.

</td>
</tr>
<tr>
<td>
DDSCAPS_NONLOCALVIDMEM

</td>
<td>
This surface exists in nonlocal display memory rather than true, local display memory. If this flag is specified, then DDSCAPS_VIDEOMEMORY flag must be specified as well. This cannot be used with the DDSCAPS_LOCALVIDMEM flag.

</td>
</tr>
<tr>
<td>
DDSCAPS_OFFSCREENPLAIN

</td>
<td>
This surface is any offscreen surface that is not an overlay, texture, z-buffer, front-buffer, back-buffer, or alpha surface. It is used to identify plain surfaces.

</td>
</tr>
<tr>
<td>
DDSCAPS_OPTIMIZED

</td>
<td>
Not currently implemented.

</td>
</tr>
<tr>
<td>
DDSCAPS_OVERLAY

</td>
<td>
This surface is an overlay. It may or may not be directly visible depending on whether it is currently being overlaid onto the primary surface. DDSCAPS_VISIBLE can be used to determine if it is being overlaid at the moment.

</td>
</tr>
<tr>
<td>
DDSCAPS_OWNDC

</td>
<td>
This surface will have a device context (DC) association for a long period.

</td>
</tr>
<tr>
<td>
DDSCAPS_PALETTE

</td>
<td>
This device driver allows unique DirectDrawPalette objects to be created and attached to this surface.

</td>
</tr>
<tr>
<td>
DDSCAPS_PRIMARYSURFACE

</td>
<td>
The surface is the primary surface. It represents what is visible to the user at the moment.

</td>
</tr>
<tr>
<td>
DDSCAPS_PRIMARYSURFACELEFT

</td>
<td>
This surface is the primary surface for the left eye. It represents what is visible to the user's left eye at the moment. When this surface is created, the surface with the DDSCAPS_PRIMARYSURFACE capability represents what is seen by the user's right eye.

</td>
</tr>
<tr>
<td>
DDSCAPS_STANDARDVGAMODE

</td>
<td>
This surface is a standard VGA mode surface, and not a ModeX surface. This flag cannot be used in combination with the DDSCAPS_MODEX flag.

</td>
</tr>
<tr>
<td>
DDSCAPS_SYSTEMMEMORY 

</td>
<td>
This surface memory was allocated in system memory.

</td>
</tr>
<tr>
<td>
DDSCAPS_TEXTURE

</td>
<td>
This surface can be used as a 3D texture. It does not indicate whether the surface is being used for that purpose.

</td>
</tr>
<tr>
<td>
DDSCAPS_VIDEOMEMORY

</td>
<td>
This surface exists in display memory.

</td>
</tr>
<tr>
<td>
DDSCAPS_VIDEOPORT

</td>
<td>
This surface can receive data from a hardware video port.

</td>
</tr>
<tr>
<td>
DDSCAPS_VISIBLE

</td>
<td>
Changes made to this surface are immediately visible. It is always set for the primary surface, as well as for overlays while they are being overlaid and texture maps while they are being textured.

</td>
</tr>
<tr>
<td>
DDSCAPS_WRITEONLY

</td>
<td>
Only write access is permitted to the surface. Read access from the surface may generate a general protection fault (GPF), but the read results from this surface are not meaningful.

</td>
</tr>
<tr>
<td>
DDSCAPS_ZBUFFER

</td>
<td>
This surface is the z-buffer. The z-buffer contains information that cannot be displayed. Instead, it contains bit-depth information that is used to determine which pixels are visible and which are obscured.

</td>
</tr>
</table>

### -field dwFormatFlags

Specifies a set of optional control flags. This member can be set to a combination of the following flags:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDPF_ALPHA

</td>
<td>
The pixel format describes an alpha-only surface.

</td>
</tr>
<tr>
<td>
DDPF_ALPHAPIXELS

</td>
<td>
The surface has alpha channel information in the pixel format.

</td>
</tr>
<tr>
<td>
DDPF_ALPHAPREMULT

</td>
<td>
Reserved for system use.

</td>
</tr>
<tr>
<td>
DDPF_BUMPDUDV

</td>
<td>
Bump map dUdV data in the pixel format is valid.

</td>
</tr>
<tr>
<td>
DDPF_BUMPLUMINANCE

</td>
<td>
Luminance data in pixel format is valid. This flag is used when hanging luminance off bumpmap surfaces; the bitmask for the luminance portion of the pixel is then indicated by the <b>dwBumpLuminanceBitCount</b> member of the <a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-_ddpixelformat">DDPIXELFORMAT</a> structure.

</td>
</tr>
<tr>
<td>
DDPF_COMPRESSED

</td>
<td>
The surface accepts pixel data in the specified format and compresses it during the write operation.

</td>
</tr>
<tr>
<td>
DDPF_FOURCC

</td>
<td>
The <a href="/windows-hardware/drivers/">FOURCC</a> code is valid.

</td>
</tr>
<tr>
<td>
DDPF_LUMINANCE

</td>
<td>
Luminance data in the pixel format is valid. This flag is used for luminance only or luminance plus alpha surfaces; the bit depth is then indicated by the <b>dwLuminanceBitCount</b> member of the DDPIXELFORMAT structure.

</td>
</tr>
<tr>
<td>
DDPF_PALETTEINDEXED1

</td>
<td>
The surface is 1-bit color indexed.

</td>
</tr>
<tr>
<td>
DDPF_PALETTEINDEXED2

</td>
<td>
The surface is 2-bit color indexed.

</td>
</tr>
<tr>
<td>
DDPF_PALETTEINDEXED4

</td>
<td>
The surface is 4-bit color indexed.

</td>
</tr>
<tr>
<td>
DDPF_PALETTEINDEXED8

</td>
<td>
The surface is 8-bit color indexed.

</td>
</tr>
<tr>
<td>
DDPF_PALETTEINDEXEDTO8

</td>
<td>
The surface is 1-, 2-, or 4-bit color indexed to an 8-bit palette.

</td>
</tr>
<tr>
<td>
DDPF_RGB

</td>
<td>
The RGB data in the pixel format structure is valid.

</td>
</tr>
<tr>
<td>
DDPF_RGBTOYUV

</td>
<td>
The surface accepts RGB data and translates it during the write operation to YUV data. The format of the data to be written is contained in the pixel format structure. The DDPF_RGB flag is set.

</td>
</tr>
<tr>
<td>
DDPF_STENCILBUFFER

</td>
<td>
The surface contains stencil information along with the Z information.

</td>
</tr>
<tr>
<td>
DDPF_YUV

</td>
<td>
The YUV data in the pixel format structure is valid.

</td>
</tr>
<tr>
<td>
DDPF_ZBUFFER

</td>
<td>
The pixel format describes a z-buffer-only surface.

</td>
</tr>
<tr>
<td>
DDPF_ZPIXELS

</td>
<td>
The surface is in RGBZ format.

</td>
</tr>
</table>

### -field dwFormatFourCC

Specifies the <a href="/windows-hardware/drivers/">FOURCC</a> code. For more information about FOURCC codes, see the DirectX SDK documentation.

### -field dwFormatBitCount

Specifies the number of bits per pixel (4, 8, 16, 24, or 32) of the RGB or YUV data.

### -field dwRBitMask

Specifies the mask for red bits.

### -field dwYBitMask

Specifies the mask for Y bits.

### -field dwGBitMask

Specifies the mask for green bits.

### -field dwUBitMask

Specifies the mask for U bits.

### -field dwBBitMask

Specifies the mask for blue bits.

### -field dwVBitMask

Specifies the mask for V bits.

## -see-also

<a href="/previous-versions/windows/hardware/drivers/ff550695(v=vs.85)">DD_DXAPI_LOCK</a>



<a href="/previous-versions/windows/drivers/display/nf-dxapi-dxapi">DxApi</a>