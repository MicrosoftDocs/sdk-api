---
UID: NS:winddi._PATHOBJ
title: PATHOBJ (winddi.h)
description: The PATHOBJ structure is used to describe a set of lines and Bezier curves that are to be stroked or filled.
helpviewer_keywords: ["PATHOBJ","PATHOBJ structure [Display Devices]","display.pathobj","grstrcts_e8c946a6-f07c-4cc2-8440-d4f3af979612.xml","winddi/PATHOBJ"]
old-location: display\pathobj.htm
tech.root: display
ms.assetid: ceccca92-3312-49b4-b0f6-a3d0cd4bbef5
ms.date: 12/05/2018
ms.keywords: PATHOBJ, PATHOBJ structure [Display Devices], display.pathobj, grstrcts_e8c946a6-f07c-4cc2-8440-d4f3af979612.xml, winddi/PATHOBJ
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
req.typenames: PATHOBJ
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PATHOBJ
 - winddi/_PATHOBJ
 - PATHOBJ
 - winddi/PATHOBJ
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
 - PATHOBJ
---

# PATHOBJ structure


## -description

The PATHOBJ structure is used to describe a set of lines and Bezier curves that are to be stroked or filled.

## -struct-fields

### -field fl

A set of hint flags that describe the path. This member is a bitwise OR (with certain restrictions) of the following values:

<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td>
PO_ALL_INTEGERS

</td>
<td>
The vertices of the path have integer coordinates with no fractional parts. This flag is intended primarily as an accelerator so that drivers can use a simpler all-integer fast-path.

In addition, when GDI sets this flag, the driver is permitted to deviate slightly from the standard NT-based operating system GDI Grid Intersection Quantization (GIQ) convention that dictates the rasterization rules for lines. Specifically, when PO_ALL_INTEGERS is set the driver can choose its own rules for which pixel should be lit in the tie-breaker case where a line logically falls exactly between two pixels. Typically, this flag allows drivers to use hardware point-to-point line drawing capabilities even when the hardware has a different tie-breaker rule from that of GIQ.

GDI sets this flag only for solid lines that are one pixel wide. Also, GDI sets this flag only if the graphics mode of the device context is set to GM_COMPATIBLE. For more information about setting the graphics mode, see <b>SetGraphicsMode</b> in the Microsoft Window SDK documentation.

</td>
</tr>
<tr>
<td>
PO_BEZIERS

</td>
<td>
The path contains Bezier curves. GDI sets only one of PO_BEZIERS or PO_ELLIPSE in the <b>fl</b> member.

</td>
</tr>
<tr>
<td>
PO_ELLIPSE

</td>
<td>
The path consists of a single ellipse inscribed in the path's bounding rectangle. GDI sets only one of PO_BEZIERS or PO_ELLIPSE in the <b>fl</b> member.

</td>
</tr>
<tr>
<td>
PO_ENUM_AS_INTEGERS

</td>
<td>
The driver can request that the vertices returned from <a href="/windows/desktop/api/winddi/nf-winddi-pathobj_benum">PATHOBJ_bEnum</a> be expressed in a 32-bit integer format rather than the standard 28.4 format. The driver makes this request by ORing PO_ENUM_AS_INTEGERS into the <b>fl</b> member of the given PATHOBJ before calling <b>PATHOBJ_bEnum</b>.

The driver can set PO_ENUM_AS_INTEGERS only when GDI has set the PO_ALL_INTEGERS flag. That is, the path must be known to contain only integer coordinates. Note that PO_ENUM_AS_INTEGERS is the only flag that the driver is permitted to modify.

When this flag is set, the driver is permitted to deviate slightly from the standard GIQ convention that dictates the rasterization rules for lines. Specifically, when PO_ENUM_ALL_INTEGERS is set the driver can choose its own rules for which pixel should be lit in the tie-breaker case where a line logically falls exactly between two pixels. Typically, this flag allows drivers to use hardware point-to-point line drawing capabilities even when the hardware has a different tie-breaker rule from that of GIQ.

</td>
</tr>
</table>

### -field cCurves

The number of lines and Bezier curves that make up the path.

## -remarks

Functions associated with this structure allow the lines and curves to be enumerated for the driver.

The following GDI service routines are provided for PATHOBJ objects:


<dl>
<dt>
<a href="/windows/desktop/api/winddi/nf-winddi-pathobj_bclosefigure">PATHOBJ_bCloseFigure</a>
</dt>
<dt>
<a href="/windows/desktop/api/winddi/nf-winddi-pathobj_benum">PATHOBJ_bEnum</a>
</dt>
<dt>
<a href="/windows/desktop/api/winddi/nf-winddi-pathobj_benumcliplines">PATHOBJ_bEnumClipLines</a>
</dt>
<dt>
<a href="/windows/desktop/api/winddi/nf-winddi-pathobj_bmoveto">PATHOBJ_bMoveTo</a>
</dt>
<dt>
<a href="/windows/desktop/api/winddi/nf-winddi-pathobj_bpolybezierto">PATHOBJ_bPolyBezierTo</a>
</dt>
<dt>
<a href="/windows/desktop/api/winddi/nf-winddi-pathobj_bpolylineto">PATHOBJ_bPolyLineTo</a>
</dt>
<dt>
<a href="/windows/desktop/api/winddi/nf-winddi-pathobj_venumstart">PATHOBJ_vEnumStart</a>
</dt>
<dt>
<a href="/windows/desktop/api/winddi/nf-winddi-pathobj_venumstartcliplines">PATHOBJ_vEnumStartClipLines</a>
</dt>
<dt>
<a href="/windows/desktop/api/winddi/nf-winddi-pathobj_vgetbounds">PATHOBJ_vGetBounds</a>
</dt>
</dl>

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvfillpath">DrvFillPath</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvstrokeandfillpath">DrvStrokeAndFillPath</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvstrokepath">DrvStrokePath</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engcreatepath">EngCreatePath</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engdeletepath">EngDeletePath</a>