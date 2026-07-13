---
UID: NF:winddi.PATHOBJ_bPolyLineTo
title: PATHOBJ_bPolyLineTo function (winddi.h)
description: The PATHOBJ_bPolyLineTo function draws lines from the current position in a path through the specified points.
helpviewer_keywords: ["PATHOBJ_bPolyLineTo","PATHOBJ_bPolyLineTo function [Display Devices]","display.pathobj_bpolylineto","gdifncs_eaa54bcf-8b39-4661-a2cf-79198ffa1df6.xml","winddi/PATHOBJ_bPolyLineTo"]
old-location: display\pathobj_bpolylineto.htm
tech.root: display
ms.assetid: 468d20e3-a78b-47b3-9c56-ef355181eb63
ms.date: 12/05/2018
ms.keywords: PATHOBJ_bPolyLineTo, PATHOBJ_bPolyLineTo function [Display Devices], display.pathobj_bpolylineto, gdifncs_eaa54bcf-8b39-4661-a2cf-79198ffa1df6.xml, winddi/PATHOBJ_bPolyLineTo
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
 - PATHOBJ_bPolyLineTo
 - winddi/PATHOBJ_bPolyLineTo
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
 - PATHOBJ_bPolyLineTo
---

# PATHOBJ_bPolyLineTo function


## -description

The <b>PATHOBJ_bPolyLineTo</b> function draws lines from the current position in a path through the specified points.

## -parameters

### -param ppo

Pointer to the <a href="/windows/desktop/api/winddi/ns-winddi-pathobj">PATHOBJ</a> structure created by the driver.

### -param pptfx

Pointer to an array of POINTFIX structures that define control points. The first line is drawn from the current position to the first point in this array; lines are then drawn to each subsequent point in the array. For a description of this data type, see <a href="/windows-hardware/drivers/display/gdi-data-types">GDI Data Types</a>.

### -param cptfx

Specifies the count of points in <i>pptfx</i>. This is also the number of lines that will be added to the path.

## -returns

The return value is <b>TRUE</b> if the function is successful. Otherwise, it is <b>FALSE</b>, and an error code is logged.

## -remarks

<b>PATHOBJ_bPolyLineTo</b> should only be called with PATHOBJ structures created by <a href="/windows/desktop/api/winddi/nf-winddi-engcreatepath">EngCreatePath</a>.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engcreatepath">EngCreatePath</a>



<a href="/windows/desktop/api/winddi/ns-winddi-pathobj">PATHOBJ</a>



<a href="/windows/desktop/api/winddi/nf-winddi-pathobj_bpolybezierto">PATHOBJ_bPolyBezierTo</a>