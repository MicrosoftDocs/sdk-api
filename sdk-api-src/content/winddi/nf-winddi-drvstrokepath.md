---
UID: NF:winddi.DrvStrokePath
title: DrvStrokePath function (winddi.h)
description: The DrvStrokePath function strokes (outlines) a path.
helpviewer_keywords: ["DrvStrokePath","DrvStrokePath function [Display Devices]","ddifncs_73cbbe62-5351-4297-82fc-b0098f21fee2.xml","display.drvstrokepath","winddi/DrvStrokePath"]
old-location: display\drvstrokepath.htm
tech.root: display
ms.assetid: c931a39d-c0ae-4f40-b70f-f51d5621c228
ms.date: 12/05/2018
ms.keywords: DrvStrokePath, DrvStrokePath function [Display Devices], ddifncs_73cbbe62-5351-4297-82fc-b0098f21fee2.xml, display.drvstrokepath, winddi/DrvStrokePath
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
 - DrvStrokePath
 - winddi/DrvStrokePath
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
 - DrvStrokePath
---

# DrvStrokePath function


## -description

The <b>DrvStrokePath</b> function strokes (outlines) a path.

## -parameters

### -param pso [in, out]

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure that identifies the surface on which to draw.

### -param ppo [in]

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-pathobj">PATHOBJ</a> structure. GDI PATHOBJ_<i>Xxx</i> service routines are provided to enumerate the lines, Bezier curves, and other data that make up the path. This indicates what is to be drawn.

### -param pco [in]

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a> structure. GDI CLIPOBJ_<i>Xxx</i> service routines are provided to enumerate the <a href="/windows-hardware/drivers/">clip region</a> as a set of rectangles. Optionally, all the lines in the path may be enumerated preclipped in a CLIPOBJ structure. This means that drivers can have GDI perform all line clipping calculations.

### -param pxo [in, optional]

Pointer to a <a href="/previous-versions/windows/hardware/drivers/ff570618(v=vs.85)">XFORMOBJ</a> structure. This is needed only when a geometric wide line is to be drawn. It specifies the transform that maps world coordinates to device coordinates. This is needed because the path is provided in device coordinates but a geometric wide line is actually widened in world coordinates.

The XFORMOBJ structure can be queried to find the transform.

### -param pbo [in]

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-brushobj">BRUSHOBJ</a> structure that specifies the brush to be used when drawing the path.

### -param pptlBrushOrg [in]

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-pointl">POINTL</a> structure that specifies the brush origin used to align the brush pattern on the device.

### -param plineattrs [in]

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-lineattrs">LINEATTRS</a> structure. Note that the <b>elStyleState</b> member of this structure must be updated as part of this function if the line is styled. Also note that the <b>ptlLastPel</b> member must be updated if a single pixel width cosmetic line is being drawn.

### -param mix [in]

The mix mode that defines the foreground and background raster operations to use for the brush. For more information about mix mode, see Remarks.

## -returns

The return value is <b>TRUE</b> if the driver is able to stroke the path. If GDI should instead stroke the path, the return value is <b>FALSE</b>, but no error code is logged. If the driver encounters an error, the return value is DDI_ERROR, and an error code is reported.

## -remarks

If the driver has hooked the function, and if the appropriate GCAPS are set, GDI calls <b>DrvStrokePath</b> when GDI draws a line or curve with any set of attributes.

If a driver supports this entry point, it should also support the drawing of cosmetic wide lines with arbitrary clipping. Using the provided GDI functions, the call can be broken down into a set of single-pixel-width lines with precomputed clipping.

This function is required if any drawing is to be done on a <a href="/windows-hardware/drivers/">device-managed surface</a>.

Drivers for advanced devices can optionally receive this call to draw paths containing Bezier curves and geometric wide lines. GDI will test the GCAPS_BEZIERS and GCAPS_GEOMETRICWIDE flags of the <b>flGraphicsCaps</b> member of the <a href="/windows/desktop/api/winddi/ns-winddi-devinfo">DEVINFO</a> structure to decide whether it should call this function. (The four combinations of the bits determine the four levels of functionality for this call.) If the driver gets an advanced call containing Bezier curves or geometric wide lines, it can decide not to handle the call, returning <b>FALSE</b>. This might happen if the path or clipping is too complex for the device to process. If the call does return <b>FALSE</b>, GDI breaks the call down into simpler calls that can be handled more easily.

For device-managed surfaces, the function must minimally support single-pixel-wide solid and styled cosmetic lines using a solid-colored brush.

The mix mode defines how the incoming pattern should be mixed with the data that is already on the device surface. The MIX data type consists of two binary raster operation (ROP2) values packed into a single ULONG. The lowest-order byte defines the foreground raster operation; the next byte defines the background raster operation. For more information about raster operation codes, see the Microsoft Windows SDK documentation.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a>



<a href="/windows/desktop/api/winddi/ns-winddi-devinfo">DEVINFO</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvfillpath">DrvFillPath</a>



<a href="/windows/desktop/api/winddi/ns-winddi-lineattrs">LINEATTRS</a>



<a href="/windows/desktop/api/winddi/ns-winddi-pathobj">PATHOBJ</a>



<a href="/previous-versions/windows/hardware/drivers/ff570618(v=vs.85)">XFORMOBJ</a>