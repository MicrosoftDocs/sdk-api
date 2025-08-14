---
UID: NF:winddi.PATHOBJ_bPolyBezierTo
title: PATHOBJ_bPolyBezierTo function (winddi.h)
description: The PATHOBJ_bPolyBezierTo function draws Bezier curves on a path.
helpviewer_keywords: ["PATHOBJ_bPolyBezierTo","PATHOBJ_bPolyBezierTo function [Display Devices]","display.pathobj_bpolybezierto","gdifncs_787796de-11ca-457d-8084-8eb0af187eef.xml","winddi/PATHOBJ_bPolyBezierTo"]
old-location: display\pathobj_bpolybezierto.htm
tech.root: display
ms.assetid: 0937c816-b205-4c5d-b4b6-74c3e7fdb0ce
ms.date: 12/05/2018
ms.keywords: PATHOBJ_bPolyBezierTo, PATHOBJ_bPolyBezierTo function [Display Devices], display.pathobj_bpolybezierto, gdifncs_787796de-11ca-457d-8084-8eb0af187eef.xml, winddi/PATHOBJ_bPolyBezierTo
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
 - PATHOBJ_bPolyBezierTo
 - winddi/PATHOBJ_bPolyBezierTo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-base-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - PATHOBJ_bPolyBezierTo
---

# PATHOBJ_bPolyBezierTo function


## -description

The <b>PATHOBJ_bPolyBezierTo</b> function draws Bezier curves on a path.

## -parameters

### -param ppo

Pointer to the <a href="/windows/desktop/api/winddi/ns-winddi-pathobj">PATHOBJ</a> structure created by the driver.

### -param pptfx

Pointer to the array of POINTFIX structures that define control points. Each set of three control points, along with the preceding control point, or current position, determines a Bezier curve. For a description of this data type, see <a href="/windows-hardware/drivers/display/gdi-data-types">GDI Data Types</a>.

### -param cptfx

Specifies the count of points in <i>pptfx</i>. Must be a multiple of three.

## -returns

The return value is <b>TRUE</b> if the function is successful. Otherwise, it is <b>FALSE</b>, and an error code is logged.

## -remarks

<b>PATHOBJ_bPolyBezierTo</b> must be called only with a PATHOBJ structure created by <a href="/windows/desktop/api/winddi/nf-winddi-engcreatepath">EngCreatePath</a>.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engcreatepath">EngCreatePath</a>



<a href="/windows/desktop/api/winddi/ns-winddi-pathobj">PATHOBJ</a>



<a href="/windows/desktop/api/winddi/nf-winddi-pathobj_bpolylineto">PATHOBJ_bPolyLineTo</a>