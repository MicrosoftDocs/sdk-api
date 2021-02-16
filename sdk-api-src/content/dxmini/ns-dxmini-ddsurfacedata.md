---
UID: NS:dxmini._DDSURFACEDATA
title: DDSURFACEDATA (dxmini.h)
description: The DDSURFACEDATA structure is used by DirectDraw to represent a surface to the kernel-mode miniport driver.
helpviewer_keywords: ["*LPDDSURFACEDATA","DDSURFACEDATA","DDSURFACEDATA structure [Display Devices]","LPDDSURFACEDATA","LPDDSURFACEDATA structure pointer [Display Devices]","Video_Structs_0138ef0b-62f2-4d2d-a76e-48d153080ca7.xml","display.ddsurfacedata","dxmini/DDSURFACEDATA","dxmini/LPDDSURFACEDATA"]
old-location: display\ddsurfacedata.htm
tech.root: display
ms.assetid: 4057cfcf-675e-439f-8b51-23adede1d35a
ms.date: 12/05/2018
ms.keywords: '*LPDDSURFACEDATA, DDSURFACEDATA, DDSURFACEDATA structure [Display Devices], LPDDSURFACEDATA, LPDDSURFACEDATA structure pointer [Display Devices], Video_Structs_0138ef0b-62f2-4d2d-a76e-48d153080ca7.xml, display.ddsurfacedata, dxmini/DDSURFACEDATA, dxmini/LPDDSURFACEDATA'
req.header: dxmini.h
req.include-header: Dxmini.h
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
req.typenames: DDSURFACEDATA, *LPDDSURFACEDATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDSURFACEDATA
 - dxmini/_DDSURFACEDATA
 - LPDDSURFACEDATA
 - dxmini/LPDDSURFACEDATA
 - DDSURFACEDATA
 - dxmini/DDSURFACEDATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxmini.h
api_name:
 - DDSURFACEDATA
---

# DDSURFACEDATA structure


## -description

The DDSURFACEDATA structure is used by DirectDraw to represent a surface to the kernel-mode miniport driver.

## -struct-fields

### -field ddsCaps

Points to a <a href="/previous-versions/windows/hardware/drivers/ff550286(v=vs.85)">DDSCAPS</a> structure that contains the creation capabilities used to describe the surface.

### -field dwSurfaceOffset

Specifies the byte offset from the beginning of the frame buffer to the start of the surface. This field is used only by the miniport driver.

### -field fpLockPtr

Points to the start of the surface.

### -field dwWidth

Specifies the surface width, in pixels.

### -field dwHeight

Specifies the surface height, in pixels.

### -field lPitch

Specifies the surface pitch, in bytes.

### -field dwOverlayFlags

Indicates a set of flags that specify the current user-mode DDOVER_<i>Xxx</i> flags set by <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_updateoverlay">DdUpdateOverlay</a>. This member is a bitwise OR of any of the following values:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDOVER_ADDDIRTYRECT

</td>
<td>
Add a dirty rectangle to an emulated overlaid surface.

</td>
</tr>
<tr>
<td>
DDOVER_ALPHADEST

</td>
<td>
Use either the alpha information in pixel format or the alpha channel surface attached to the destination surface as the alpha channel for this overlay.

</td>
</tr>
<tr>
<td>
DDOVER_ALPHADESTCONSTOVERRIDE

</td>
<td>
Use the <b>dwAlphaDestConst</b> member of the DDOVERLAYFX structure as the destination alpha channel for this overlay. The DDOVERLAYFX structure is defined in <i>ddraw.h</i>.

</td>
</tr>
<tr>
<td>
DDOVER_ALPHADESTNEG

</td>
<td>
The destination surface becomes more transparent as the alpha value increases (0 is opaque).

</td>
</tr>
<tr>
<td>
DDOVER_ALPHADESTSURFACEOVERRIDE

</td>
<td>
Use the <b>lpDDSAlphaDest</b> member of the DDOVERLAYFX structure (defined in the DirectDraw SDK documentation) as the alpha channel destination for this overlay.

</td>
</tr>
<tr>
<td>
DDOVER_ALPHAEDGEBLEND

</td>
<td>
Use the <b>dwAlphaEdgeBlend</b> member of the DDOVERLAYFX structure (defined in the DirectDraw SDK documentation) as the alpha channel for the edges of the image that border the color key colors.

</td>
</tr>
<tr>
<td>
DDOVER_ALPHASRC

</td>
<td>
Use either the alpha information in pixel format or the alpha channel surface attached to the source surface as the source alpha channel for this overlay.

</td>
</tr>
<tr>
<td>
DDOVER_ALPHASRCCONSTOVERRIDE

</td>
<td>
Use the <b>dwAlphaSrcConst</b> member of the DDOVERLAYFX structure (defined in the DirectDraw SDK documentation) as the source alpha channel for this overlay.

</td>
</tr>
<tr>
<td>
DDOVER_ALPHASRCNEG

</td>
<td>
The source surface becomes more transparent as the alpha value increases (0 is opaque).

</td>
</tr>
<tr>
<td>
DDOVER_ALPHASRCSURFACEOVERRIDE

</td>
<td>
Use the <b>lpDDSAlphaSrc</b> member of the DDOVERLAYFX structure (defined in the DirectDraw SDK documentation) as the alpha channel source for this overlay.

</td>
</tr>
<tr>
<td>
DDOVER_AUTOFLIP

</td>
<td>
Automatically flip to the next surface in the flip chain each time a hardware video port VSYNC occurs.

</td>
</tr>
<tr>
<td>
DDOVER_BOB

</td>
<td>
Display each field of the interlaced video stream individually without causing any artifacts.

</td>
</tr>
<tr>
<td>
DDOVER_BOBHARDWARE

</td>
<td>
Bob is performed using hardware rather than software or being emulated.

</td>
</tr>
<tr>
<td>
DDOVER_DDFX

</td>
<td>
Use the overlay FX flags to define special overlay effects.

</td>
</tr>
<tr>
<td>
DDOVER_HIDE

</td>
<td>
Turn this overlay off.

</td>
</tr>
<tr>
<td>
DDOVER_INTERLEAVED

</td>
<td>
The surface memory is composed of interleaved fields.

</td>
</tr>
<tr>
<td>
DDOVER_KEYDEST

</td>
<td>
Use the color key associated with the destination surface.

</td>
</tr>
<tr>
<td>
DDOVER_KEYDESTOVERRIDE

</td>
<td>
Use the <b>dckDestColorkey</b> member of the DDOVERLAYFX structure (defined in the DirectDraw SDK documentation) as the color key for the destination surface.

</td>
</tr>
<tr>
<td>
DDOVER_KEYSRC

</td>
<td>
Use the color key associated with the source surface.

</td>
</tr>
<tr>
<td>
DDOVER_KEYSRCOVERRIDE

</td>
<td>
Use the <b>dckSrcColorkey</b> member of the DDOVERLAYFX structure (defined in the DirectDraw SDK documentation) as the color key for the source surface.

</td>
</tr>
<tr>
<td>
DDOVER_OVERRIDEBOBWEAVE

</td>
<td>
Bob and weave decisions should not be overridden by other interfaces. If this flag is set, DirectDraw does not allow a kernel-mode driver to use the kernel-mode video transport functionality to switch the hardware between bob and weave mode.

</td>
</tr>
<tr>
<td>
DDOVER_REFRESHALL

</td>
<td>
Redraw the entire surface on an emulated overlaid surface.

</td>
</tr>
<tr>
<td>
DDOVER_REFRESHDIRTYRECTS

</td>
<td>
Redraw all dirty rectangles on an emulated overlaid surface.

</td>
</tr>
<tr>
<td>
DDOVER_SHOW

</td>
<td>
Turn this overlay on.

</td>
</tr>
</table>

### -field dwOverlayOffset

Specifies the byte offset from the beginning of the frame buffer to the start of the overlay. This field is used only by the miniport driver.

### -field dwOverlaySrcWidth

Specifies the overlay source width, in pixels. This field is used only by the miniport driver.

### -field dwOverlaySrcHeight

Specifies the overlay source height, in pixels. This field is used only by the miniport driver.

### -field dwOverlayDestWidth

Specifies the overlay destination width, in pixels. This field is used only by the miniport driver.

### -field dwOverlayDestHeight

Specifies the overlay destination height, in pixels. This field is used only by the miniport driver.

### -field dwVideoPortId

If this surface is being fed by a <a href="/windows-hardware/drivers/">video port extensions (VPE)</a> object, this field indicates the ID of the VPE object, an integer in the range (0 - (maximum number of hardware video ports -1 )); otherwise, this field is -1.

### -field dwFormatFlags

Specifies a set of pixel-format control flags. This member is a bitwise OR of any of the following values:

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
The color components in the pixel are premultiplied by the alpha value in the pixel. If this flag is set, the DDPF_ALPHAPIXELS flag must also be set. If this flag is not set but the DDPF_ALPHAPIXELS flag is set, the color components in the pixel format are not premultiplied by alpha. In this case, the color components must be multiplied by the alpha value at the time that an alpha-blending operation is performed.

</td>
</tr>
<tr>
<td>
DDPF_BUMPDUDV

</td>
<td>
The bump map dUdV data in the pixel format is valid.

</td>
</tr>
<tr>
<td>
DDPF_BUMPLUMINANCE

</td>
<td>
The luminance data in pixel format is valid. This flag is used when hanging luminance off bumpmap surfaces. The bitmask for the luminance portion of the pixel is then indicated by the <b>dwBumpLuminanceBitCount</b> member of the <a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-_ddpixelformat">DDPIXELFORMAT</a> structure.

</td>
</tr>
<tr>
<td>
DDPF_COMPRESSED

</td>
<td>
The surface will accept pixel data in the specified format and compress it during the write operation.

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
The luminance data in the pixel format is valid. This flag is used for luminance only or luminance plus alpha surfaces; the bit depth is then indicated by the <b>dwLuminanceBitCount</b> member of the <a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-_ddpixelformat">DDPIXELFORMAT</a> structure.

</td>
</tr>
<tr>
<td>
DDPF_PALETTEINDEXED1

</td>
<td>
The surface is 1--bit color indexed.

</td>
</tr>
<tr>
<td>
DDPF_PALETTEINDEXED2

</td>
<td>
The surface is 2--bit color indexed.

</td>
</tr>
<tr>
<td>
DDPF_PALETTEINDEXED4

</td>
<td>
The surface is 4--bit color indexed.

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
The surface will accept RGB data and translate it during the write operation to YUV data. The format of the data to be written will be contained in the pixel format structure. The DDPF_RGB flag will be set.

</td>
</tr>
<tr>
<td>
DDPF_STENCILBUFFER

</td>
<td>
The surface contains stencil information along with Z information.

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

Specifies the <a href="/windows-hardware/drivers/">FOURCC</a> code.

### -field dwFormatBitCount

Specifies the number of bits per pixel (4, 8, 16, 24, or 32).

### -field dwRBitMask

Specifies the red bitmask.

### -field dwGBitMask

Specifies the green bitmask.

### -field dwBBitMask

Specifies the blue bitmask.

### -field dwDriverReserved1

Reserved for the HAL/Miniport

### -field dwDriverReserved2

Reserved for the HAL/Miniport

### -field dwDriverReserved3

Reserved for the HAL/Miniport

### -field dwDriverReserved4

Are reserved for use by the miniport driver.

## -see-also

<a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-_ddpixelformat">DDPIXELFORMAT</a>



<a href="/previous-versions/windows/hardware/drivers/ff550286(v=vs.85)">DDSCAPS</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_updateoverlay">DdUpdateOverlay</a>