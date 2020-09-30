---
UID: NF:winddi.DrvTextOut
title: DrvTextOut function (winddi.h)
description: The DrvTextOut function is the entry point from GDI that calls for the driver to render a set of glyphs at specified positions.
helpviewer_keywords: ["DrvTextOut","DrvTextOut function [Display Devices]","ddifncs_e78c3647-65af-427c-8153-0046e031e345.xml","display.drvtextout","winddi/DrvTextOut"]
old-location: display\drvtextout.htm
tech.root: display
ms.assetid: f2f61687-d833-4d09-8cd5-99e81436c1c1
ms.date: 12/05/2018
ms.keywords: DrvTextOut, DrvTextOut function [Display Devices], ddifncs_e78c3647-65af-427c-8153-0046e031e345.xml, display.drvtextout, winddi/DrvTextOut
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Desktop
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrvTextOut
 - winddi/DrvTextOut
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
 - DrvTextOut
---

# DrvTextOut function


## -description

The <b>DrvTextOut</b> function is the entry point from GDI that calls for the driver to render a set of glyphs at specified positions.

## -parameters

### -param pso

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure that describes the surface on which to write.

### -param pstro

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-strobj">STROBJ</a> structure that defines the glyphs to be rendered and the positions in which to place them.

### -param pfo

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-fontobj">FONTOBJ</a> structure from which to retrieve information about the font and its glyphs.

### -param pco

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a> structure that defines the clip region through which all rendering must be done. The driver cannot affect any pixels outside the clip region.

### -param prclExtra

Pointer to a RECTL structure. GDI always sets this parameter to <b>NULL</b> in calls to this function. It should be ignored by the driver.

### -param prclOpaque

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rectl">RECTL</a> structure that represents a single opaque rectangle. This rectangle is lower-right exclusive. Pixels within this rectangle (those that are not foreground and not clipped) are to be rendered with the opaque brush. This rectangle always bounds the text to be drawn. If this parameter is <b>NULL</b>, no opaque pixels are to be rendered.

### -param pboFore

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-brushobj">BRUSHOBJ</a> structure that represents the brush object to be used for the foreground pixels. This brush will always be a solid color brush.

### -param pboOpaque

Pointer to a BRUSHOBJ structure that represents the opaque pixels. Both the foreground and background mix modes for this brush are assumed to be R2_COPYPEN. Unless the driver sets the GCAPS_ARBRUSHOPAQUE capabilities bit in the <b>flGraphicsCaps</b> member of the <a href="/windows/desktop/api/winddi/ns-winddi-devinfo">DEVINFO</a> structure, it will always be called with a solid color brush.

### -param pptlOrg

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-pointl">POINTL</a> structure that defines the brush origin for both brushes.

### -param mix

The mix mode that defines the foreground and background raster operations to use for the brush that <i>pboFore</i> points to. For more information about mix mode, see Remarks.

## -returns

The return value is <b>TRUE</b> if the function is successful; otherwise, it is <b>FALSE</b>.

## -remarks

The input parameters to <b>DrvTextOut</b> define two sets of pixels: foreground and opaque. The driver must render the surface so that the result is identical to a process where the opaque pixels are rendered first with the opaque brush, and then the foreground pixels are rendered with the foreground brush. Each of these operations is limited by clipping.

The foreground and opaque pixels are regarded as a screen through which color is brushed onto the surface. The glyphs of the font do not have color in themselves.

The input parameters to <b>DrvTextOut</b> define the set of glyph pixels, the set of extra rectangles, the opaque rectangle, and the clip region. It is the driver's responsibility to calculate and then render the set of foreground and opaque pixels.

GDI guarantees that <b>DrvTextOut</b> and <a href="/windows/desktop/api/winddi/nf-winddi-drvdestroyfont">DrvDestroyFont</a> never overlap; consequently, the driver can rely on cached information while processing a <b>DrvTextOut</b> call.

The mix mode defines how the incoming pattern should be mixed with the data that is already on the device surface. The MIX data type consists of two binary raster operation (ROP2) values packed into a single ULONG. The lowest-order byte defines the foreground raster operation; the next byte defines the background raster operation. For more information about raster operation codes, see the Microsoft Windows SDK documentation.

This is a conditionally required function.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a>



<a href="/windows/desktop/api/winddi/ns-winddi-devinfo">DEVINFO</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvdestroyfont">DrvDestroyFont</a>



<a href="/windows/desktop/api/winddi/ns-winddi-fontobj">FONTOBJ</a>



<a href="/windows/desktop/api/winddi/ns-winddi-strobj">STROBJ</a>



<a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a>