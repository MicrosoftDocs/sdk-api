---
UID: NF:winddi.EngPaint
title: EngPaint function (winddi.h)
description: The EngPaint function causes GDI to paint a specified region.
helpviewer_keywords: ["EngPaint","EngPaint function [Display Devices]","display.engpaint","gdifncs_fdbafee3-278d-4d69-bd16-535e92436a1d.xml","winddi/EngPaint"]
old-location: display\engpaint.htm
tech.root: display
ms.assetid: 9bfa2e7b-06c7-427a-9283-54b9c6cdac30
ms.date: 12/05/2018
ms.keywords: EngPaint, EngPaint function [Display Devices], display.engpaint, gdifncs_fdbafee3-278d-4d69-bd16-535e92436a1d.xml, winddi/EngPaint
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
 - EngPaint
 - winddi/EngPaint
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-full-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - EngPaint
---

# EngPaint function


## -description

The <b>EngPaint</b> function causes GDI to paint a specified region.

## -parameters

### -param pso

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure that describes the surface on which to draw.

### -param pco

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a> structure that defines the area to be painted. The <b>CLIPOBJ_</b><i>Xxx</i> service routines are provided to enumerate the <a href="/windows-hardware/drivers/">clip region</a> as a set of rectangles.

### -param pbo

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-brushobj">BRUSHOBJ</a> structure that defines the pattern and colors with which to fill.

### -param pptlBrushOrg

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-pointl">POINTL</a> structure that defines the brush origin used to align the brush pattern on the device.

### -param mix [in]

Defines the foreground and background raster operations to use for the brush.

## -returns

The return value is <b>TRUE</b> if the function is successful. Otherwise, it is <b>FALSE</b>, and an error code is logged.

## -remarks

Vector device drivers can implement this function with the help of <a href="/windows/desktop/api/winddi/nf-winddi-engcreatepath">EngCreatePath</a> and <b>PATHOBJ_</b><i>Xxx</i> service routines.

The mix mode defines how the incoming pattern should be mixed with the data already on the device surface. The MIX data type consists of two ROP2 values packed into a single ULONG. The low-order byte defines the foreground raster operation; the next byte defines the background raster operation. For more information about raster operation codes, see the Microsoft Windows SDK documentation.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-brushobj">BRUSHOBJ</a>



<a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engcreatepath">EngCreatePath</a>



<a href="/windows/desktop/api/winddi/ns-winddi-pathobj">PATHOBJ</a>



<a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a>