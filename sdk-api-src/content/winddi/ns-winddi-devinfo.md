---
UID: NS:winddi.tagDEVINFO
title: DEVINFO (winddi.h)
description: The DEVINFO structure provides information about the driver and its private PDEV to the graphics engine.
helpviewer_keywords: ["*PDEVINFO","DEVINFO","DEVINFO structure [Display Devices]","PDEVINFO","PDEVINFO structure pointer [Display Devices]","display.devinfo","grstrcts_a5bb2e1a-5348-4453-a5ef-674b4693dbed.xml","winddi/DEVINFO","winddi/PDEVINFO"]
old-location: display\devinfo.htm
tech.root: display
ms.assetid: 5ba3e521-2e70-4a5b-979d-30a061275d42
ms.date: 12/05/2018
ms.keywords: '*PDEVINFO, DEVINFO, DEVINFO structure [Display Devices], PDEVINFO, PDEVINFO structure pointer [Display Devices], display.devinfo, grstrcts_a5bb2e1a-5348-4453-a5ef-674b4693dbed.xml, winddi/DEVINFO, winddi/PDEVINFO'
req.header: winddi.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DEVINFO, *PDEVINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDEVINFO
 - winddi/tagDEVINFO
 - PDEVINFO
 - winddi/PDEVINFO
 - DEVINFO
 - winddi/DEVINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DEVINFO
---

# DEVINFO structure


## -description

The DEVINFO structure provides information about the driver and its private <a href="/windows-hardware/drivers/">PDEV</a> to the graphics engine.

## -struct-fields

### -field flGraphicsCaps

Is a set of flags that describe graphics capabilities of the graphics driver and/or its hardware. These flags are defined in the following table.

<table>
<tr>
<th>Flag</th>
<th>Definition</th>
</tr>
<tr>
<td>
GCAPS_ALTERNATEFILL

</td>
<td>
Handles alternating fills.

</td>
</tr>
<tr>
<td>
GCAPS_ARBRUSHOPAQUE

</td>
<td>
Supports an arbitrary brush for text opaque rectangle (background color).

</td>
</tr>
<tr>
<td>
GCAPS_ARBRUSHTEXT

</td>
<td>
Supports an arbitrary brush for the text foreground color.

</td>
</tr>
<tr>
<td>
GCAPS_ASYNCCHANGE

</td>
<td>
This flag is obsolete. In legacy drivers, this flag indicates that the driver can change the pointer shape in hardware while other drawing is occurring on the device.

</td>
</tr>
<tr>
<td>
GCAPS_ASYNCMOVE

</td>
<td>
The driver can move the pointer in hardware while other drawing is occurring on the device.

</td>
</tr>
<tr>
<td>
GCAPS_BEZIERS

</td>
<td>
Handles Bezier curves.

</td>
</tr>
<tr>
<td>
GCAPS_CMYKCOLOR

</td>
<td>
The driver supports the CYMK color space.

</td>
</tr>
<tr>
<td>
GCAPS_COLOR_DITHER

</td>
<td>
Handles color dithering to a PDEV-compatible surface.

</td>
</tr>
<tr>
<td>
GCAPS_DIRECTDRAW

</td>
<td>
This flag is obsolete.

</td>
</tr>
<tr>
<td>
GCAPS_DITHERONREALIZE

</td>
<td>
Specifies that GDI can call <a href="/windows/desktop/api/winddi/nf-winddi-drvrealizebrush">DrvRealizeBrush</a> with the RGB to be dithered directly.

</td>
</tr>
<tr>
<td>
GCAPS_DONTJOURNAL

</td>
<td>
Disallows metafile printing to this printer driver. This is valid only for printer DCs and will generally result in slower return-to-application time when printing.

</td>
</tr>
<tr>
<td>
GCAPS_FONT_RASTERIZER

</td>
<td>
Device hardware can rasterize TrueType fonts.

</td>
</tr>
<tr>
<td>
GCAPS_FORCEDITHER

</td>
<td>
Allows dithering on all geometric pens.

</td>
</tr>
<tr>
<td>
GCAPS_GEOMETRICWIDE

</td>
<td>
Handles geometric widening.

</td>
</tr>
<tr>
<td>
GCAPS_GRAY16

</td>
<td>
Handles antialiased text natively.

</td>
</tr>
<tr>
<td>
GCAPS_HALFTONE

</td>
<td>
Handles halftoning.

</td>
</tr>
<tr>
<td>
GCAPS_HIGHRESTEXT

</td>
<td>
This flag is obsolete. In legacy drivers, this flag indicates that the driver is requesting glyph positions as returned by the STROBJ in FIX point coordinates.

</td>
</tr>
<tr>
<td>
GCAPS_HORIZSTRIKE

</td>
<td>
This flag is obsolete. In legacy drivers, this flag indicates that the driver handles horizontal strikeouts in <a href="/windows/desktop/api/winddi/nf-winddi-drvtextout">DrvTextOut</a>.

</td>
</tr>
<tr>
<td>
GCAPS_ICM

</td>
<td>
Indicates that color management operations can be performed by the driver or printer hardware.

</td>
</tr>
<tr>
<td>
GCAPS_LAYERED

</td>
<td>
Indicates that this is a layer or <a href="/windows-hardware/drivers/">mirror driver</a> for remoting. Printer drivers cannot be layer drivers.

</td>
</tr>
<tr>
<td>
GCAPS_MONO_DITHER

</td>
<td>
Handles monochrome dithering.

</td>
</tr>
<tr>
<td>
GCAPS_NO64BITMEMACCESS

</td>
<td>
This flag is obsolete.

</td>
</tr>
<tr>
<td>
GCAPS_NUP

</td>
<td>
Indicates that "N-up" printing is supported.

</td>
</tr>
<tr>
<td>
GCAPS_OPAQUERECT

</td>
<td>
Handles opaque rectangles in <a href="/windows/desktop/api/winddi/nf-winddi-drvtextout">DrvTextOut</a>.

</td>
</tr>
<tr>
<td>
GCAPS_PALMANAGED

</td>
<td>
Supports palette management.

</td>
</tr>
<tr>
<td>
GCAPS_PANNING

</td>
<td>
When GDI is simulating the pointer, it should call <a href="/windows/desktop/api/winddi/nf-winddi-drvmovepointer">DrvMovePointer</a> to notify the driver of the current cursor position. This allows the driver to handle panning virtual displays.

</td>
</tr>
<tr>
<td>
GCAPS_SCREENPRECISION

</td>
<td>
The rasterizer (font engine) should choose a screen (soft) font over a device font when choosing a font for which there is no exact match.

</td>
</tr>
<tr>
<td>
GCAPS_VECTORFONT

</td>
<td>
Handles stroking of vector fonts in <a href="/windows/desktop/api/winddi/nf-winddi-drvtextout">DrvTextOut</a>.

</td>
</tr>
<tr>
<td>
GCAPS_VERTSTRIKE

</td>
<td>
This flag is obsolete. In legacy drivers, this flag indicated that the driver handled vertical strikeouts in <a href="/windows/desktop/api/winddi/nf-winddi-drvtextout">DrvTextOut</a>.

</td>
</tr>
<tr>
<td>
GCAPS_WINDINGFILL

</td>
<td>
Handles winding mode fills. See <a href="/windows-hardware/drivers/display/path-fill-modes">Path Fill Modes</a> for more information.

</td>
</tr>
<tr>
<td>
GCAPS2_REMOTEDRIVER

</td>
<td>
Indicates that the display driver is used to support a remote user session.

</td>
</tr>
</table>

### -field lfDefaultFont

Is an Extended Logical Font structure that specifies the default font for a device. For more information about this structure, see EXTLOGFONT in the Microsoft Windows SDK documentation.

### -field lfAnsiVarFont

Is an Extended Logical Font structure that specifies the default variable-pitch font for a device. For more information about this structure, see EXTLOGFONT in the Windows SDK documentation.

### -field lfAnsiFixFont

Is an Extended Logical Font structure that specifies the default fixed-pitch (monospaced) font for a device. For more information about this structure, see EXTLOGFONT in the Windows SDK documentation.

### -field cFonts

Specifies the number of device fonts. GDI assumes that the device can draw text with this number of fonts on its own surfaces and that the driver can provide metrics information about the fonts. If the driver sets <b>cFonts</b> to -1, GDI will wait until fonts are needed to query the driver for the actual number of fonts it supports in a call to <a href="/windows/desktop/api/winddi/nf-winddi-drvqueryfont">DrvQueryFont</a>.

### -field iDitherFormat

Specifies the format of the bitmap. This parameter indicates how many bits of color information per pixel are requested, and must be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
BMF_1BPP

</td>
<td>
Monochrome

</td>
</tr>
<tr>
<td>
BMF_4BPP

</td>
<td>
4 bits per pixel

</td>
</tr>
<tr>
<td>
BMF_8BPP

</td>
<td>
8 bits per pixel

</td>
</tr>
<tr>
<td>
BMF_16BPP

</td>
<td>
16 bits per pixel

</td>
</tr>
<tr>
<td>
BMF_24BPP

</td>
<td>
24 bits per pixel

</td>
</tr>
<tr>
<td>
BMF_32BPP

</td>
<td>
32 bits per pixel

</td>
</tr>
<tr>
<td>
BMF_4RLE

</td>
<td>
4 bits per pixel, run length encoded

</td>
</tr>
<tr>
<td>
BMF_8RLE

</td>
<td>
8 bits per pixel, run length encoded

</td>
</tr>
<tr>
<td>
BMF_JPEG

</td>
<td>
JPEG compressed image

</td>
</tr>
<tr>
<td>
BMF_PNG

</td>
<td>
PNG compressed image

</td>
</tr>
</table>

### -field cxDither

### -field cyDither

Specify the dimensions of a dithered brush. If these members are nonzero, then the device can create a dithered brush for a given RGB color.

### -field hpalDefault

Handle to the default palette for the device. The driver should create the palette by calling <a href="/windows/desktop/api/winddi/nf-winddi-engcreatepalette">EngCreatePalette</a>. The driver associates a palette with a device by returning this handle to GDI.

### -field flGraphicsCaps2

Is a set of flags that describe additional graphics capabilities of the device driver. These flags are defined in the following table.

<table>
<tr>
<th>Flag</th>
<th>Definition</th>
</tr>
<tr>
<td>
GCAPS2_ALPHACURSOR

</td>
<td>
Handles pointers with per-pixel alpha values.

</td>
</tr>
<tr>
<td>
GCAPS2_CHANGEGAMMARAMP

</td>
<td>
The display device has a loadable hardware <a href="/windows-hardware/drivers/">gamma ramp</a>.

</td>
</tr>
<tr>
<td>
GCAPS2_EXCLUDELAYERED

</td>
<td>
Indicates that this is an accessibility mirror driver. Mirror drivers that do not set this flag will still receive drawing primitives for layered HWNDs. See <a href="/windows-hardware/drivers/display/mirror-drivers">Mirror Drivers</a> for more information.

</td>
</tr>
<tr>
<td>
GCAPS2_ICD_MULTIMON

</td>
<td>
Informs GDI that the driver intends to handle <a href="/windows/desktop/api/winddi/nf-winddi-drvsetpixelformat">DrvSetPixelFormat</a>, <a href="/windows/desktop/api/winddi/nf-winddi-drvdescribepixelformat">DrvDescribePixelFormat</a>, and <a href="/windows/desktop/api/winddi/nf-winddi-drvswapbuffers">DrvSwapBuffers</a> calls in a multimon environment, even when the rectangle in the operation also intersects another device. Only one device is ever given the opportunity to handle those calls. If the capability is not specified and the region involved intersects more than one device, no driver is called.

</td>
</tr>
<tr>
<td>
GCAPS2_INCLUDEAPIBITMAPS

</td>
<td>
When drawing calls are made to a device-independent bitmap (DIB), an accessibility mirror driver will be called. See <a href="/windows-hardware/drivers/display/mirror-drivers">Mirror Drivers</a> for more information.

</td>
</tr>
<tr>
<td>
GCAPS2_JPEGSRC

</td>
<td>
Device can accept JPEG compressed images (that is, images for which BMF_JPEG is set in the <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure).

</td>
</tr>
<tr>
<td>
GCAPS2_MOUSETRAILS

</td>
<td>
Indicates that the driver supports mouse trails (a succession of cursor images showing the mouse's location during a short period of time). The driver is capable of handling the values GDI sends in the <i>fl</i> parameter of the <a href="/windows/desktop/api/winddi/nf-winddi-drvsetpointershape">DrvSetPointerShape</a> function. The driver should use the SPS_LENGTHMASK and SPS_FREQMASK masks to obtain values for the length and frequency of the mouse trails. See <b>DrvSetPointerShape</b> for more information about these masks.

</td>
</tr>
<tr>
<td>
GCAPS2_PNGSRC

</td>
<td>
Device can accept PNG compressed images (that is, images for which BMF_PNG is set in the <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure).

</td>
</tr>
<tr>
<td>
GCAPS2_SYNCFLUSH

</td>
<td>
The driver supports a programmatic-based flush mechanism for batched graphics DDI calls. <a href="/windows/desktop/api/winddi/nf-winddi-drvsynchronizesurface">DrvSynchronizeSurface</a> will be called whenever GDI must flush any drawing that is being batched by the driver.

</td>
</tr>
<tr>
<td>
GCAPS2_SYNCTIMER

</td>
<td>
The driver supports a timer-based flush mechanism for batched graphics DDI calls. <a href="/windows/desktop/api/winddi/nf-winddi-drvsynchronizesurface">DrvSynchronizeSurface</a> will be called periodically, based on a timer interval determined by GDI.

</td>
</tr>
</table>

## -remarks

The driver's <a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a> function fills in a DEVINFO structure; the driver should set only the members that are relevant to it. This structure is zero-initialized by GDI before <b>DrvEnablePDEV</b> is called. Applications do not have direct access to this structure.

If a driver sets GCAPS2_JPEGSRC or GCAPS2_PNGSRC in <b>flGraphicsCaps2</b>, the following rules apply:

<ul>
<li>
The driver must provide a <a href="/windows/desktop/api/winddi/nf-winddi-drvquerydevicesupport">DrvQueryDeviceSupport</a> function.

</li>
<li>
Every driver-defined graphics DDI function that receives a <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure as input must be able to either support the compressed format or return an error code. In the case of printer drivers, to support the compressed format, the driver must be able to perform either one of the following tasks:


<ul>
<li>If the print device can process the JPEG/PNG compressed format, the printer driver should pass the compressed format through to its page description language (PDL) output.</li>
<li>If the print device cannot process the JPEG/PNG compressed format, the printer driver must first convert the compressed JPEG/PNG format into another image format that the print device can process. The printer driver can then make the image information available in the driver's PDL output.
<div class="alert"><b>Note</b>  In the case of converting from JPEG/PNG to the bitmap format, the printer driver must not use GDI functions. For example, the driver can use the Windows Imaging Component (WIC)  APIs instead to do the conversion.</div>
<div> </div>


</li>
</ul>


</li>
<li>
The driver must be able to handle complex clip regions for images that use the compressed format.

</li>
<li>
For driver-defined graphics DDI functions that receive a ROP4 input argument, only 0xCCCC is used with JPEG and PNG formats.

</li>
</ul>

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvqueryfont">DrvQueryFont</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvrealizebrush">DrvRealizeBrush</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvtextout">DrvTextOut</a>