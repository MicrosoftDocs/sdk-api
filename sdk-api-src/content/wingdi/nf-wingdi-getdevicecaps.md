---
UID: NF:wingdi.GetDeviceCaps
title: GetDeviceCaps function (wingdi.h)
description: The GetDeviceCaps function retrieves device-specific information for the specified device.
helpviewer_keywords: ["ASPECTX","ASPECTXY","ASPECTY","BITSPIXEL","BLTALIGNMENT","CLIPCAPS","COLORMGMTCAPS","COLORRES","CURVECAPS","DRIVERVERSION","GetDeviceCaps","GetDeviceCaps function [Windows GDI]","HORZRES","HORZSIZE","LINECAPS","LOGPIXELSX","LOGPIXELSY","NUMBRUSHES","NUMCOLORS","NUMFONTS","NUMPENS","NUMRESERVED","PDEVICESIZE","PHYSICALHEIGHT","PHYSICALOFFSETX","PHYSICALOFFSETY","PHYSICALWIDTH","PLANES","POLYGONALCAPS","RASTERCAPS","SCALINGFACTORX","SCALINGFACTORY","SHADEBLENDCAPS","SIZEPALETTE","TECHNOLOGY","TEXTCAPS","VERTRES","VERTSIZE","VREFRESH","_win32_GetDeviceCaps","gdi.getdevicecaps","wingdi/GetDeviceCaps"]
old-location: gdi\getdevicecaps.htm
tech.root: gdi
ms.assetid: d524c4c7-22af-495d-aecc-b9921e53ca7b
ms.date: 12/05/2018
ms.keywords: ASPECTX, ASPECTXY, ASPECTY, BITSPIXEL, BLTALIGNMENT, CLIPCAPS, COLORMGMTCAPS, COLORRES, CURVECAPS, DRIVERVERSION, GetDeviceCaps, GetDeviceCaps function [Windows GDI], HORZRES, HORZSIZE, LINECAPS, LOGPIXELSX, LOGPIXELSY, NUMBRUSHES, NUMCOLORS, NUMFONTS, NUMPENS, NUMRESERVED, PDEVICESIZE, PHYSICALHEIGHT, PHYSICALOFFSETX, PHYSICALOFFSETY, PHYSICALWIDTH, PLANES, POLYGONALCAPS, RASTERCAPS, SCALINGFACTORX, SCALINGFACTORY, SHADEBLENDCAPS, SIZEPALETTE, TECHNOLOGY, TEXTCAPS, VERTRES, VERTSIZE, VREFRESH, _win32_GetDeviceCaps, gdi.getdevicecaps, wingdi/GetDeviceCaps
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetDeviceCaps
 - wingdi/GetDeviceCaps
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-devcaps-l1-1-0.dll
 - Ext-MS-Win-RTCore-GDI-devcaps-l1-1-0.dll
 - Ext-MS-Win-RTCore-GDI-DevCaps-L1-1-1.dll
 - GDI32Full.dll
api_name:
 - GetDeviceCaps
---

# GetDeviceCaps function


## -description

The <b>GetDeviceCaps</b> function retrieves device-specific information for the specified device.

## -parameters

### -param hdc [in]

A handle to the DC.

### -param index [in]

The item to be returned. This parameter can be one of the following values.

<table>
<tr>
<th>Index</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DRIVERVERSION"></a><a id="driverversion"></a><dl>
<dt><b>DRIVERVERSION</b></dt>
</dl>
</td>
<td width="60%">
The device driver version.

</td>
</tr>
<tr>
<td width="40%"><a id="TECHNOLOGY"></a><a id="technology"></a><dl>
<dt><b>TECHNOLOGY</b></dt>
</dl>
</td>
<td width="60%">
Device technology. It can be any one of the following values.

<table>
<tr>
<td>DT_PLOTTER</td>
<td>Vector plotter</td>
</tr>
<tr>
<td>DT_RASDISPLAY</td>
<td>Raster display</td>
</tr>
<tr>
<td>DT_RASPRINTER</td>
<td>Raster printer</td>
</tr>
<tr>
<td>DT_RASCAMERA</td>
<td>Raster camera</td>
</tr>
<tr>
<td>DT_CHARSTREAM</td>
<td>Character stream</td>
</tr>
<tr>
<td>DT_METAFILE</td>
<td>Metafile</td>
</tr>
<tr>
<td>DT_DISPFILE</td>
<td>Display file</td>
</tr>
</table>
 

If the <i>hdc</i> parameter is a handle to the DC of an enhanced metafile, the device technology is that of the referenced device as specified to the <a href="/windows/desktop/api/wingdi/nf-wingdi-createenhmetafilea">CreateEnhMetaFile</a> function. To determine whether it is an enhanced metafile DC, use the <a href="/windows/desktop/api/wingdi/nf-wingdi-getobjecttype">GetObjectType</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="HORZSIZE"></a><a id="horzsize"></a><dl>
<dt><b>HORZSIZE</b></dt>
</dl>
</td>
<td width="60%">
Width, in millimeters, of the physical screen.

</td>
</tr>
<tr>
<td width="40%"><a id="VERTSIZE"></a><a id="vertsize"></a><dl>
<dt><b>VERTSIZE</b></dt>
</dl>
</td>
<td width="60%">
Height, in millimeters, of the physical screen.

</td>
</tr>
<tr>
<td width="40%"><a id="HORZRES"></a><a id="horzres"></a><dl>
<dt><b>HORZRES</b></dt>
</dl>
</td>
<td width="60%">
Width, in pixels, of the screen; or for printers, the width, in pixels, of the printable area of the page.

</td>
</tr>
<tr>
<td width="40%"><a id="VERTRES"></a><a id="vertres"></a><dl>
<dt><b>VERTRES</b></dt>
</dl>
</td>
<td width="60%">
Height, in raster lines, of the screen; or for printers, the height, in pixels, of the printable area of the page.

</td>
</tr>
<tr>
<td width="40%"><a id="LOGPIXELSX"></a><a id="logpixelsx"></a><dl>
<dt><b>LOGPIXELSX</b></dt>
</dl>
</td>
<td width="60%">
Number of pixels per logical inch along the screen width. In a system with multiple display monitors, this value is the same for all monitors.

</td>
</tr>
<tr>
<td width="40%"><a id="LOGPIXELSY"></a><a id="logpixelsy"></a><dl>
<dt><b>LOGPIXELSY</b></dt>
</dl>
</td>
<td width="60%">
Number of pixels per logical inch along the screen height. In a system with multiple display monitors, this value is the same for all monitors.

</td>
</tr>
<tr>
<td width="40%"><a id="BITSPIXEL"></a><a id="bitspixel"></a><dl>
<dt><b>BITSPIXEL</b></dt>
</dl>
</td>
<td width="60%">
Number of adjacent color bits for each pixel.

</td>
</tr>
<tr>
<td width="40%"><a id="PLANES"></a><a id="planes"></a><dl>
<dt><b>PLANES</b></dt>
</dl>
</td>
<td width="60%">
Number of color planes.

</td>
</tr>
<tr>
<td width="40%"><a id="NUMBRUSHES"></a><a id="numbrushes"></a><dl>
<dt><b>NUMBRUSHES</b></dt>
</dl>
</td>
<td width="60%">
Number of device-specific brushes.

</td>
</tr>
<tr>
<td width="40%"><a id="NUMPENS"></a><a id="numpens"></a><dl>
<dt><b>NUMPENS</b></dt>
</dl>
</td>
<td width="60%">
Number of device-specific pens.

</td>
</tr>
<tr>
<td width="40%"><a id="NUMFONTS"></a><a id="numfonts"></a><dl>
<dt><b>NUMFONTS</b></dt>
</dl>
</td>
<td width="60%">
Number of device-specific fonts.

</td>
</tr>
<tr>
<td width="40%"><a id="NUMCOLORS"></a><a id="numcolors"></a><dl>
<dt><b>NUMCOLORS</b></dt>
</dl>
</td>
<td width="60%">
Number of entries in the device's color table, if the device has a color depth of no more than 8 bits per pixel. For devices with greater color depths, -1 is returned.

</td>
</tr>
<tr>
<td width="40%"><a id="ASPECTX"></a><a id="aspectx"></a><dl>
<dt><b>ASPECTX</b></dt>
</dl>
</td>
<td width="60%">
Relative width of a device pixel used for line drawing.

</td>
</tr>
<tr>
<td width="40%"><a id="ASPECTY"></a><a id="aspecty"></a><dl>
<dt><b>ASPECTY</b></dt>
</dl>
</td>
<td width="60%">
Relative height of a device pixel used for line drawing.

</td>
</tr>
<tr>
<td width="40%"><a id="ASPECTXY"></a><a id="aspectxy"></a><dl>
<dt><b>ASPECTXY</b></dt>
</dl>
</td>
<td width="60%">
Diagonal width of the device pixel used for line drawing.

</td>
</tr>
<tr>
<td width="40%"><a id="PDEVICESIZE"></a><a id="pdevicesize"></a><dl>
<dt><b>PDEVICESIZE</b></dt>
</dl>
</td>
<td width="60%">
Reserved.

</td>
</tr>
<tr>
<td width="40%"><a id="CLIPCAPS"></a><a id="clipcaps"></a><dl>
<dt><b>CLIPCAPS</b></dt>
</dl>
</td>
<td width="60%">
Flag that indicates the clipping capabilities of the device. If the device can clip to a rectangle, it is 1. Otherwise, it is 0.

</td>
</tr>
<tr>
<td width="40%"><a id="SIZEPALETTE"></a><a id="sizepalette"></a><dl>
<dt><b>SIZEPALETTE</b></dt>
</dl>
</td>
<td width="60%">
Number of entries in the system palette. This index is valid only if the device driver sets the RC_PALETTE bit in the RASTERCAPS index and is available only if the driver is compatible with 16-bit Windows.

</td>
</tr>
<tr>
<td width="40%"><a id="NUMRESERVED"></a><a id="numreserved"></a><dl>
<dt><b>NUMRESERVED</b></dt>
</dl>
</td>
<td width="60%">
Number of reserved entries in the system palette. This index is valid only if the device driver sets the RC_PALETTE bit in the RASTERCAPS index and is available only if the driver is compatible with 16-bit Windows.

</td>
</tr>
<tr>
<td width="40%"><a id="COLORRES"></a><a id="colorres"></a><dl>
<dt><b>COLORRES</b></dt>
</dl>
</td>
<td width="60%">
Actual color resolution of the device, in bits per pixel. This index is valid only if the device driver sets the RC_PALETTE bit in the RASTERCAPS index and is available only if the driver is compatible with 16-bit Windows.

</td>
</tr>
<tr>
<td width="40%"><a id="PHYSICALWIDTH"></a><a id="physicalwidth"></a><dl>
<dt><b>PHYSICALWIDTH</b></dt>
</dl>
</td>
<td width="60%">
For printing devices: the width of the physical page, in device units. For example, a printer set to print at 600 dpi on 8.5-x11-inch paper has a physical width value of 5100 device units. Note that the physical page is almost always greater than the printable area of the page, and never smaller.

</td>
</tr>
<tr>
<td width="40%"><a id="PHYSICALHEIGHT"></a><a id="physicalheight"></a><dl>
<dt><b>PHYSICALHEIGHT</b></dt>
</dl>
</td>
<td width="60%">
For printing devices: the height of the physical page, in device units. For example, a printer set to print at 600 dpi on 8.5-by-11-inch paper has a physical height value of 6600 device units. Note that the physical page is almost always greater than the printable area of the page, and never smaller.

</td>
</tr>
<tr>
<td width="40%"><a id="PHYSICALOFFSETX"></a><a id="physicaloffsetx"></a><dl>
<dt><b>PHYSICALOFFSETX</b></dt>
</dl>
</td>
<td width="60%">
For printing devices: the distance from the left edge of the physical page to the left edge of the printable area, in device units. For example, a printer set to print at 600 dpi on 8.5-by-11-inch paper, that cannot print on the leftmost 0.25-inch of paper, has a horizontal physical offset of 150 device units.

</td>
</tr>
<tr>
<td width="40%"><a id="PHYSICALOFFSETY"></a><a id="physicaloffsety"></a><dl>
<dt><b>PHYSICALOFFSETY</b></dt>
</dl>
</td>
<td width="60%">
For printing devices: the distance from the top edge of the physical page to the top edge of the printable area, in device units. For example, a printer set to print at 600 dpi on 8.5-by-11-inch paper, that cannot print on the topmost 0.5-inch of paper, has a vertical physical offset of 300 device units.

</td>
</tr>
<tr>
<td width="40%"><a id="VREFRESH"></a><a id="vrefresh"></a><dl>
<dt><b>VREFRESH</b></dt>
</dl>
</td>
<td width="60%">
For display devices: the current vertical refresh rate of the device, in cycles per second (Hz).

A vertical refresh rate value of 0 or 1 represents the display hardware's default refresh rate. This default rate is typically set by switches on a display card or computer motherboard, or by a configuration program that does not use display functions such as <a href="/windows/desktop/api/winuser/nf-winuser-changedisplaysettingsa">ChangeDisplaySettings</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SCALINGFACTORX"></a><a id="scalingfactorx"></a><dl>
<dt><b>SCALINGFACTORX</b></dt>
</dl>
</td>
<td width="60%">
Scaling factor for the x-axis of the printer.

</td>
</tr>
<tr>
<td width="40%"><a id="SCALINGFACTORY"></a><a id="scalingfactory"></a><dl>
<dt><b>SCALINGFACTORY</b></dt>
</dl>
</td>
<td width="60%">
Scaling factor for the y-axis of the printer.

</td>
</tr>
<tr>
<td width="40%"><a id="BLTALIGNMENT"></a><a id="bltalignment"></a><dl>
<dt><b>BLTALIGNMENT</b></dt>
</dl>
</td>
<td width="60%">
Preferred horizontal drawing alignment, expressed as a multiple of pixels. For best drawing performance, windows should be horizontally aligned to a multiple of this value. A value of zero indicates that the device is accelerated, and any alignment may be used.

</td>
</tr>
<tr>
<td width="40%"><a id="SHADEBLENDCAPS"></a><a id="shadeblendcaps"></a><dl>
<dt><b>SHADEBLENDCAPS</b></dt>
</dl>
</td>
<td width="60%">
Value that indicates the shading and blending capabilities of the device. See Remarks for further comments.

<table>
<tr>
<td>SB_CONST_ALPHA</td>
<td>Handles the <b>SourceConstantAlpha</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-blendfunction">BLENDFUNCTION</a> structure, which is referenced by the blendFunction parameter of the <a href="/windows/desktop/api/wingdi/nf-wingdi-alphablend">AlphaBlend</a> function.</td>
</tr>
<tr>
<td>SB_GRAD_RECT</td>
<td>Capable of doing <a href="/windows/desktop/api/wingdi/nf-wingdi-gradientfill">GradientFill</a> rectangles.</td>
</tr>
<tr>
<td>SB_GRAD_TRI</td>
<td>Capable of doing <a href="/windows/desktop/api/wingdi/nf-wingdi-gradientfill">GradientFill</a> triangles.</td>
</tr>
<tr>
<td>SB_NONE</td>
<td>Device does not support any of these capabilities.</td>
</tr>
<tr>
<td>SB_PIXEL_ALPHA</td>
<td>Capable of handling per-pixel alpha in <a href="/windows/desktop/api/wingdi/nf-wingdi-alphablend">AlphaBlend</a>.</td>
</tr>
<tr>
<td>SB_PREMULT_ALPHA</td>
<td>Capable of handling premultiplied alpha in <a href="/windows/desktop/api/wingdi/nf-wingdi-alphablend">AlphaBlend</a>.</td>
</tr>
</table>
 

</td>
</tr>
<tr>
<td width="40%"><a id="RASTERCAPS"></a><a id="rastercaps"></a><dl>
<dt><b>RASTERCAPS</b></dt>
</dl>
</td>
<td width="60%">
Value that indicates the raster capabilities of the device, as shown in the following table.

<table>
<tr>
<td>RC_BANDING</td>
<td>Requires banding support.</td>
</tr>
<tr>
<td>RC_BITBLT</td>
<td>Capable of transferring bitmaps.</td>
</tr>
<tr>
<td>RC_BITMAP64</td>
<td>Capable of supporting bitmaps larger than 64 KB.</td>
</tr>
<tr>
<td>RC_DI_BITMAP</td>
<td>Capable of supporting the <a href="/windows/desktop/api/wingdi/nf-wingdi-setdibits">SetDIBits</a> and <a href="/windows/desktop/api/wingdi/nf-wingdi-getdibits">GetDIBits</a> functions.</td>
</tr>
<tr>
<td>RC_DIBTODEV</td>
<td>Capable of supporting the <a href="/windows/desktop/api/wingdi/nf-wingdi-setdibitstodevice">SetDIBitsToDevice</a> function.</td>
</tr>
<tr>
<td>RC_FLOODFILL</td>
<td>Capable of performing flood fills.</td>
</tr>
<tr>
<td>RC_PALETTE</td>
<td>Specifies a palette-based device.</td>
</tr>
<tr>
<td>RC_SCALING</td>
<td>Capable of scaling.</td>
</tr>
<tr>
<td>RC_STRETCHBLT</td>
<td>Capable of performing the <a href="/windows/desktop/api/wingdi/nf-wingdi-stretchblt">StretchBlt</a> function.</td>
</tr>
<tr>
<td>RC_STRETCHDIB</td>
<td>Capable of performing the <a href="/windows/desktop/api/wingdi/nf-wingdi-stretchdibits">StretchDIBits</a> function.</td>
</tr>
</table>
 

</td>
</tr>
<tr>
<td width="40%"><a id="CURVECAPS"></a><a id="curvecaps"></a><dl>
<dt><b>CURVECAPS</b></dt>
</dl>
</td>
<td width="60%">
Value that indicates the curve capabilities of the device, as shown in the following table.

<table>
<tr>
<td>CC_NONE</td>
<td>Device does not support curves.</td>
</tr>
<tr>
<td>CC_CHORD</td>
<td>Device can draw chord arcs.</td>
</tr>
<tr>
<td>CC_CIRCLES</td>
<td>Device can draw circles.</td>
</tr>
<tr>
<td>CC_ELLIPSES</td>
<td>Device can draw ellipses.</td>
</tr>
<tr>
<td>CC_INTERIORS</td>
<td>Device can draw interiors.</td>
</tr>
<tr>
<td>CC_PIE</td>
<td>Device can draw pie wedges.</td>
</tr>
<tr>
<td>CC_ROUNDRECT</td>
<td>Device can draw rounded rectangles.</td>
</tr>
<tr>
<td>CC_STYLED</td>
<td>Device can draw styled borders.</td>
</tr>
<tr>
<td>CC_WIDE</td>
<td>Device can draw wide borders.</td>
</tr>
<tr>
<td>CC_WIDESTYLED</td>
<td>Device can draw borders that are wide and styled.</td>
</tr>
</table>
 

</td>
</tr>
<tr>
<td width="40%"><a id="LINECAPS"></a><a id="linecaps"></a><dl>
<dt><b>LINECAPS</b></dt>
</dl>
</td>
<td width="60%">
Value that indicates the line capabilities of the device, as shown in the following table:

<table>
<tr>
<td>LC_NONE</td>
<td>Device does not support lines.</td>
</tr>
<tr>
<td>LC_INTERIORS</td>
<td>Device can draw interiors.</td>
</tr>
<tr>
<td>LC_MARKER</td>
<td>Device can draw a marker.</td>
</tr>
<tr>
<td>LC_POLYLINE</td>
<td>Device can draw a polyline.</td>
</tr>
<tr>
<td>LC_POLYMARKER</td>
<td>Device can draw multiple markers.</td>
</tr>
<tr>
<td>LC_STYLED</td>
<td>Device can draw styled lines.</td>
</tr>
<tr>
<td>LC_WIDE</td>
<td>Device can draw wide lines.</td>
</tr>
<tr>
<td>LC_WIDESTYLED</td>
<td>Device can draw lines that are wide and styled.</td>
</tr>
</table>
 

</td>
</tr>
<tr>
<td width="40%"><a id="POLYGONALCAPS"></a><a id="polygonalcaps"></a><dl>
<dt><b>POLYGONALCAPS</b></dt>
</dl>
</td>
<td width="60%">
Value that indicates the polygon capabilities of the device, as shown in the following table.

<table>
<tr>
<td>PC_NONE</td>
<td>Device does not support polygons.</td>
</tr>
<tr>
<td>PC_INTERIORS</td>
<td>Device can draw interiors.</td>
</tr>
<tr>
<td>PC_POLYGON</td>
<td>Device can draw alternate-fill polygons.</td>
</tr>
<tr>
<td>PC_RECTANGLE</td>
<td>Device can draw rectangles.</td>
</tr>
<tr>
<td>PC_SCANLINE</td>
<td>Device can draw a single scanline.</td>
</tr>
<tr>
<td>PC_STYLED</td>
<td>Device can draw styled borders.</td>
</tr>
<tr>
<td>PC_WIDE</td>
<td>Device can draw wide borders.</td>
</tr>
<tr>
<td>PC_WIDESTYLED</td>
<td>Device can draw borders that are wide and styled.</td>
</tr>
<tr>
<td>PC_WINDPOLYGON</td>
<td>Device can draw winding-fill polygons.</td>
</tr>
</table>
 

</td>
</tr>
<tr>
<td width="40%"><a id="TEXTCAPS"></a><a id="textcaps"></a><dl>
<dt><b>TEXTCAPS</b></dt>
</dl>
</td>
<td width="60%">
Value that indicates the text capabilities of the device, as shown in the following table.

<table>
<tr>
<td>TC_OP_CHARACTER</td>
<td>Device is capable of character output precision.</td>
</tr>
<tr>
<td>TC_OP_STROKE</td>
<td>Device is capable of stroke output precision.</td>
</tr>
<tr>
<td>TC_CP_STROKE</td>
<td>Device is capable of stroke clip precision.</td>
</tr>
<tr>
<td>TC_CR_90</td>
<td>Device is capable of 90-degree character rotation.</td>
</tr>
<tr>
<td>TC_CR_ANY</td>
<td>Device is capable of any character rotation.</td>
</tr>
<tr>
<td>TC_SF_X_YINDEP</td>
<td>Device can scale independently in the x- and y-directions.</td>
</tr>
<tr>
<td>TC_SA_DOUBLE</td>
<td>Device is capable of doubled character for scaling.</td>
</tr>
<tr>
<td>TC_SA_INTEGER</td>
<td>Device uses integer multiples only for character scaling.</td>
</tr>
<tr>
<td>TC_SA_CONTIN</td>
<td>Device uses any multiples for exact character scaling.</td>
</tr>
<tr>
<td>TC_EA_DOUBLE</td>
<td>Device can draw double-weight characters.</td>
</tr>
<tr>
<td>TC_IA_ABLE</td>
<td>Device can italicize.</td>
</tr>
<tr>
<td>TC_UA_ABLE</td>
<td>Device can underline.</td>
</tr>
<tr>
<td>TC_SO_ABLE</td>
<td>Device can draw strikeouts.</td>
</tr>
<tr>
<td>TC_RA_ABLE</td>
<td>Device can draw raster fonts.</td>
</tr>
<tr>
<td>TC_VA_ABLE</td>
<td>Device can draw vector fonts.</td>
</tr>
<tr>
<td>TC_RESERVED</td>
<td>Reserved; must be zero.</td>
</tr>
<tr>
<td>TC_SCROLLBLT</td>
<td>Device cannot scroll using a bit-block transfer. Note that this meaning may be the opposite of what you expect.</td>
</tr>
</table>
 

</td>
</tr>
<tr>
<td width="40%"><a id="COLORMGMTCAPS"></a><a id="colormgmtcaps"></a><dl>
<dt><b>COLORMGMTCAPS</b></dt>
</dl>
</td>
<td width="60%">
Value that indicates the color management capabilities of the device.

<table>
<tr>
<td>CM_CMYK_COLOR</td>
<td>Device can accept CMYK color space ICC color profile.</td>
</tr>
<tr>
<td>CM_DEVICE_ICM</td>
<td>Device can perform ICM on either the device driver or the device itself.</td>
</tr>
<tr>
<td>CM_GAMMA_RAMP</td>
<td>Device supports <a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicegammaramp">GetDeviceGammaRamp</a> and <a href="/windows/desktop/api/wingdi/nf-wingdi-setdevicegammaramp">SetDeviceGammaRamp</a>
</td>
</tr>
<tr>
<td>CM_NONE</td>
<td>Device does not support ICM.</td>
</tr>
</table>
 

</td>
</tr>
</table>

## -returns

The return value specifies the value of the desired item.

When <i>nIndex</i> is BITSPIXEL and the device has 15bpp or 16bpp, the return value is 16.

## -remarks

When <i>nIndex</i> is SHADEBLENDCAPS:

<ul>
<li>For a printer, <b>GetDeviceCaps</b> returns whatever the printer reports.</li>
<li>For a display device, all blending operations are available; besides SB_NONE, the only return values are SB_CONST_ALPHA and SB_PIXEL_ALPHA, which indicate whether these operations are accelerated.</li>
</ul>
On a multiple monitor system, if <i>hdc</i> is the desktop, <b>GetDeviceCaps</b> returns the capabilities of the primary monitor. If you want info for other monitors, you must use the <a href="/windows/desktop/gdi/multiple-display-monitors-reference">multi-monitor APIs</a> or <a href="/windows/desktop/api/wingdi/nf-wingdi-createdca">CreateDC</a> to get a HDC for the device context (DC) of a specific monitor.  

<div class="alert"><b>Note</b>  Display1 is typically the primary monitor, but not always.</div>
<div> </div>
<b>GetDeviceCaps</b> provides the following six indexes in place of printer escapes.

<table>
<tr>
<th>Index</th>
<th>Printer escape replaced</th>
</tr>
<tr>
<td>PHYSICALWIDTH</td>
<td>GETPHYSPAGESIZE</td>
</tr>
<tr>
<td>PHYSICALHEIGHT</td>
<td>GETPHYSPAGESIZE</td>
</tr>
<tr>
<td>PHYSICALOFFSETX</td>
<td>GETPRINTINGOFFSET</td>
</tr>
<tr>
<td>PHYSICALOFFSETY</td>
<td>GETPHYSICALOFFSET</td>
</tr>
<tr>
<td>SCALINGFACTORX</td>
<td>GETSCALINGFACTOR</td>
</tr>
<tr>
<td>SCALINGFACTORY</td>
<td>GETSCALINGFACTOR</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  <b>GetDeviceCaps</b> reports info that the display driver provides. If the display driver declines to report any info, <b>GetDeviceCaps</b> calculates the info based on fixed calculations. If the display driver reports invalid info, <b>GetDeviceCaps</b> returns the invalid info. Also, if the display driver declines to report info, <b>GetDeviceCaps</b> might calculate incorrect info because it assumes either fixed DPI (96 DPI) or a fixed size (depending on the info that the display driver did and didn’t provide). Unfortunately, a display driver that is implemented to the Windows Display Driver Model (WDDM) (introduced in Windows Vista) causes GDI to not get the info, so <b>GetDeviceCaps</b> must always calculate the info.</div>
<div> </div>

#### Examples

For an example, see <a href="/windows/desktop/printdocs/preparing-to-print">Preparing to Print</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-createenhmetafilea">CreateEnhMetaFile</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createica">CreateIC</a>



<a href="/windows/desktop/gdi/device-context-functions">Device Context Functions</a>



<a href="/windows/desktop/gdi/device-contexts">Device Contexts Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-devicecapabilitiesa">DeviceCapabilities</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdibits">GetDIBits</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getobjecttype">GetObjectType</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setdibits">SetDIBits</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setdibitstodevice">SetDIBitsToDevice</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-stretchblt">StretchBlt</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-stretchdibits">StretchDIBits</a>
