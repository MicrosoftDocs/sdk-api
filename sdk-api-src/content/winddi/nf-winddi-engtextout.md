---
UID: NF:winddi.EngTextOut
title: EngTextOut function (winddi.h)
description: The EngTextOut function causes GDI to render a set of glyphs at specified positions.
helpviewer_keywords: ["EngTextOut","EngTextOut function [Display Devices]","display.engtextout","gdifncs_e383ce94-952d-48e3-a814-afd38822aad2.xml","winddi/EngTextOut"]
old-location: display\engtextout.htm
tech.root: display
ms.assetid: 7891692e-a4e1-401a-99e0-ed8135dc6f1d
ms.date: 12/05/2018
ms.keywords: EngTextOut, EngTextOut function [Display Devices], display.engtextout, gdifncs_e383ce94-952d-48e3-a814-afd38822aad2.xml, winddi/EngTextOut
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EngTextOut
 - winddi/EngTextOut
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-common-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - EngTextOut
---

# EngTextOut function


## -description

The <b>EngTextOut</b> function causes GDI to render a set of glyphs at specified positions.

## -parameters

### -param pso

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure that describes the surface on which to write.

### -param pstro

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-strobj">STROBJ</a> structure that defines the glyphs to be rendered and the positions where they are to be placed.

### -param pfo

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-fontobj">FONTOBJ</a> structure that is used to retrieve information about the font and its glyphs.

### -param pco

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a> structure that defines the clip region through which rendering must be done. No pixels can be affected outside this clip region.

### -param prclExtra

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rectl">RECTL</a> structure. This parameter should always be <b>NULL</b>.

### -param prclOpaque

Pointer to a RECTL structure that identifies a single opaque rectangle that is lower-right exclusive. Pixels within this rectangle (those that are not foreground and not clipped) are to be rendered with the opaque brush. This rectangle always bounds the text to be drawn. If this parameter is <b>NULL</b>, no opaque pixels are to be rendered.

### -param pboFore

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-brushobj">BRUSHOBJ</a> structure that represents the brush object to be used for the foreground pixels. This brush will always be a solid color brush.

### -param pboOpaque

Pointer to a BRUSHOBJ structure that represents the brush object for the opaque pixels. Both the foreground and background mix modes for this brush are assumed to be R2_COPYPEN. Unless the driver sets the GCAPS_ARBRUSHOPAQUE capabilities bit in the <b>flGraphicsCaps</b> member of the <a href="/windows/desktop/api/winddi/ns-winddi-devinfo">DEVINFO</a> structure, it will always be called with a solid color brush.

### -param pptlOrg

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-pointl">POINTL</a> structure that defines the brush origin for both brushes. If this parameter is set to 0 when <b>EngTextOut</b> is called, some printer drivers may print color images incorrectly. For more information, see <b>Remarks</b>.

### -param mix [in]

Specifies foreground and background raster operations (mix modes) for <i>pboFore</i>.

## -returns

The return value is <b>TRUE</b> if the function is successful. Otherwise, it is <b>FALSE</b>, and an error code is logged.

## -remarks

The driver should call <b>EngTextOut</b> when it has hooked <a href="/windows/desktop/api/winddi/nf-winddi-drvtextout">DrvTextOut</a> and cannot render the glyphs.

<div class="alert"><b>Note</b>    The driver cannot punt to <b>EngTextOut</b> if it has hooked <i>DrvTextOut</i> for a device managed surface.</div>
<div> </div>
The input parameters to <b>EngTextOut</b> define two sets of pixels: foreground and opaque. The driver must render the surface so the result is identical to a process where the opaque pixels are rendered first with the opaque brush, and then the foreground pixels are rendered with the foreground brush. Each of these operations is limited by clipping.

When the <i>pptlOrg</i> parameter of this function is set to 0, some printer drivers print color images incorrectly in Microsoft Windows Server 2003 (Japanese version). Setting <i>pptlOrg</i> to 0, a <b>NULL</b> pointer value, is interpreted to mean that no brush origin is defined. To prevent this problem, initialize <i>pptlOrg</i> with the address of a POINTL structure whose members are set to (0,0), prior to the call to <b>EngTextOut</b>.

The foreground and opaque pixels are regarded as a screen through which color is brushed onto the surface. The glyphs of the font do not have color in themselves.

The input parameters to <b>EngTextOut</b> define the set of glyph pixels, the set of extra rectangles, the opaque rectangle, and the clip region. The driver must calculate and then render the set of foreground and opaque pixels.

The mix mode defines how the incoming pattern should be mixed with the data already on the device surface. The MIX data type consists of two ROP2 values packed into a single ULONG. The low-order byte defines the foreground raster operation; the next byte defines the background raster operation. For more information about raster operation codes, see the Microsoft Windows SDK documentation.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a>



<a href="/windows/desktop/api/winddi/ns-winddi-devinfo">DEVINFO</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvtextout">DrvTextOut</a>



<a href="/windows/desktop/api/winddi/ns-winddi-fontobj">FONTOBJ</a>



<a href="/windows/desktop/api/winddi/ns-winddi-strobj">STROBJ</a>



<a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a>