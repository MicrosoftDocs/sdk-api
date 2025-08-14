---
UID: NF:winddi.EngStrokePath
title: EngStrokePath function (winddi.h)
description: The EngStrokePath function requests that GDI stroke a specified path.
helpviewer_keywords: ["EngStrokePath","EngStrokePath function [Display Devices]","display.engstrokepath","gdifncs_d6a5ca42-fa75-4cba-8eff-d8c0801d058b.xml","winddi/EngStrokePath"]
old-location: display\engstrokepath.htm
tech.root: display
ms.assetid: e592297d-69ff-443e-bc76-9849b61a6915
ms.date: 12/05/2018
ms.keywords: EngStrokePath, EngStrokePath function [Display Devices], display.engstrokepath, gdifncs_d6a5ca42-fa75-4cba-8eff-d8c0801d058b.xml, winddi/EngStrokePath
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
 - EngStrokePath
 - winddi/EngStrokePath
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
 - EngStrokePath
---

# EngStrokePath function


## -description

The <b>EngStrokePath</b> function requests that GDI stroke a specified path.

## -parameters

### -param pso

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure that describes the surface on which to draw.

### -param ppo

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-pathobj">PATHOBJ</a> structure. The <b>PATHOBJ_</b><i>Xxx</i> service routines are provided to enumerate the lines, Bezier curves, and other data that make up the path. This indicates what is to be drawn.

### -param pco

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a> structure. The <b>CLIPOBJ_</b><i>Xxx</i> service routines are provided to enumerate the <a href="/windows-hardware/drivers/">clip region</a> as a set of rectangles. Optionally, all the lines in the path can be enumerated preclipped by this CLIPOBJ. This means that drivers can have all their line clipping calculations done for them.

### -param pxo

Pointer to a <a href="/previous-versions/windows/hardware/drivers/ff570618(v=vs.85)">XFORMOBJ</a> structure. This is needed only when a geometric wide line is to be drawn. It specifies the transform that converts world coordinates to device coordinates. This is needed because the path is provided in device coordinates but a geometric wide line is actually widened in world coordinates.

The driver can use the <b>XFORMOBJ_</b><i>Xxx</i> service routines to determine the transform.

### -param pbo

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-brushobj">BRUSHOBJ</a> structure that specifies the brush to be used when drawing the path.

### -param pptlBrushOrg

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-pointl">POINTL</a> structure that contains the brush origin used to align the brush pattern on the device.

### -param plineattrs [in]

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-lineattrs">LINEATTRS</a> structure. Note that the <b>elStyleState</b> member of this structure must be updated as part of this function if the line is styled. Also note the <b>ptlLastPel</b> member of the same structure must be updated if a single-pixel-width cosmetic line is being drawn.

### -param mix [in]

Specifies how to combine the brush with the destination.

## -returns

The return value is <b>TRUE</b> if GDI strokes the path. If the driver should stroke the path, the return value is <b>FALSE</b>, and no error is logged. If GDI encounters an error, the return value is DDI_ERROR, and an error code is logged.

## -remarks

The mix mode defines how the incoming pattern should be mixed with the data already on the device surface. The MIX data type consists of two ROP2 values packed into a single ULONG. The low-order byte defines the foreground raster operation; the next byte defines the background raster operation. For more information about raster operation codes, see the Microsoft Windows SDK documentation.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvstrokepath">DrvStrokePath</a>



<a href="/windows/desktop/api/winddi/ns-winddi-lineattrs">LINEATTRS</a>



<a href="/windows/desktop/api/winddi/ns-winddi-pathobj">PATHOBJ</a>



<a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a>



<a href="/previous-versions/windows/hardware/drivers/ff570618(v=vs.85)">XFORMOBJ</a>