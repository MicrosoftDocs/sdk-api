---
UID: NF:winddi.DrvStrokeAndFillPath
title: DrvStrokeAndFillPath function (winddi.h)
description: The DrvStrokeAndFillPath function strokes (outlines) and fills a path concurrently.
helpviewer_keywords: ["DrvStrokeAndFillPath","DrvStrokeAndFillPath function [Display Devices]","ddifncs_ca3b1895-31d0-4c1b-b47c-df61ccef2afa.xml","display.drvstrokeandfillpath","winddi/DrvStrokeAndFillPath"]
old-location: display\drvstrokeandfillpath.htm
tech.root: display
ms.assetid: 92a04fe5-146d-4839-a854-1ac50705b447
ms.date: 12/05/2018
ms.keywords: DrvStrokeAndFillPath, DrvStrokeAndFillPath function [Display Devices], ddifncs_ca3b1895-31d0-4c1b-b47c-df61ccef2afa.xml, display.drvstrokeandfillpath, winddi/DrvStrokeAndFillPath
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
 - DrvStrokeAndFillPath
 - winddi/DrvStrokeAndFillPath
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
 - DrvStrokeAndFillPath
---

# DrvStrokeAndFillPath function


## -description

The <b>DrvStrokeAndFillPath</b> function strokes (outlines) and fills a path concurrently.

## -parameters

### -param pso [in, out]

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure that describes the surface on which to draw.

### -param ppo [in, out]

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-pathobj">PATHOBJ</a> structure that describes the path to be filled. The PATHOBJ_<i>Xxx</i> service routines are provided to enumerate the lines, Bezier curves, and other data that make up the path.

### -param pco [in]

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a> structure. The CLIPOBJ_<i>Xxx</i> service routines are provided to enumerate the <a href="/windows-hardware/drivers/">clip region</a> as a set of rectangles.

### -param pxo [in, optional]

Pointer to a <a href="/previous-versions/windows/hardware/drivers/ff570618(v=vs.85)">XFORMOBJ</a> structure that is required when a geometric wide line is drawn. It specifies the transform that takes world coordinates to device coordinates. This is needed because the path is provided in device coordinates but a geometric wide line is actually widened in world coordinates. The XFORMOBJ can be queried to find out what the transform is.

### -param pboStroke [in]

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-brushobj">BRUSHOBJ</a> structure that specifies the brush to use when stroking the path.

### -param plineattrs [in]

Pointer to the <a href="/windows/desktop/api/winddi/ns-winddi-lineattrs">LINEATTRS</a> structure that describes the attributes of the line to be drawn.

### -param pboFill [in]

Pointer to a BRUSHOBJ structure that specifies the brush to use when filling the path.

### -param pptlBrushOrg [in]

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-pointl">POINTL</a> structure that specifies the brush origin for both brushes.

### -param mixFill [in]

The mix mode that defines the foreground and background raster operations to use for the brush. For more information about mix mode, see Remarks.

### -param flOptions [in]

Specifies either FP_WINDINGMODE, meaning that a winding mode fill should be performed, or FP_ALTERNATEMODE, meaning that an alternating mode fill should be performed. All other flags should be ignored. For more information about these modes, see <a href="/windows-hardware/drivers/display/path-fill-modes">Path Fill Modes</a>.

## -returns

The return value is <b>TRUE</b> if the driver is able to fill the path. Otherwise, if GDI should instead fill the path, the return value is <b>FALSE</b>. If an error occurs, the return value is DDI_ERROR, and an error code is logged.

## -remarks

If a wide line is used for stroking, the filled area must be reduced to compensate.

The driver can return <b>FALSE</b> if the path or the clipping is too complex for the device to handle; in that case, GDI converts to a simpler call. For example, if the device driver has set the GCAPS_BEZIERS flag in the <b>flGraphicsCaps</b> member of the <a href="/windows/desktop/api/winddi/ns-winddi-devinfo">DEVINFO</a> structure and then receives a path with Bezier curves, it can return <b>FALSE</b>; GDI will then convert the Bezier curves to lines and call <b>DrvStrokeAndFillPath</b> again. If the device driver returns <b>FALSE</b> again, GDI will further simplify the call, making calls to <a href="/windows/desktop/api/winddi/nf-winddi-drvstrokepath">DrvStrokePath</a> and <a href="/windows/desktop/api/winddi/nf-winddi-drvfillpath">DrvFillPath</a>, or to <a href="/windows/desktop/api/winddi/nf-winddi-drvbitblt">DrvBitBlt</a>, depending on the mix and width of the lines making up the path.

The mix mode defines how the incoming pattern should be mixed with the data that is already on the device surface. The MIX data type consists of two binary raster operation (ROP2) values packed into a single ULONG. The lowest-order byte defines the foreground raster operation; the next byte defines the background raster operation. For more information about raster operation codes, see the Microsoft Windows SDK documentation.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvbitblt">DrvBitBlt</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvfillpath">DrvFillPath</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvstrokepath">DrvStrokePath</a>



<a href="/windows/desktop/api/winddi/ns-winddi-lineattrs">LINEATTRS</a>



<a href="/windows/desktop/api/winddi/ns-winddi-pathobj">PATHOBJ</a>



<a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a>



<a href="/previous-versions/windows/hardware/drivers/ff570618(v=vs.85)">XFORMOBJ</a>