---
UID: NS:winddi._PATHOBJ
title: "_PATHOBJ"
author: windows-driver-content
description: The PATHOBJ structure is used to describe a set of lines and Bezier curves that are to be stroked or filled.
old-location: display\pathobj.htm
old-project: display
ms.assetid: ceccca92-3312-49b4-b0f6-a3d0cd4bbef5
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: PATHOBJ, PATHOBJ structure [Display Devices], _PATHOBJ, display.pathobj, grstrcts_e8c946a6-f07c-4cc2-8440-d4f3af979612.xml, winddi/PATHOBJ
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: PATHOBJ
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	winddi.h
api_name:
-	PATHOBJ
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _PATHOBJ structure


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
The driver can request that the vertices returned from <a href="https://msdn.microsoft.com/library/windows/hardware/ff568851">PATHOBJ_bEnum</a> be expressed in a 32-bit integer format rather than the standard 28.4 format. The driver makes this request by ORing PO_ENUM_AS_INTEGERS into the <b>fl</b> member of the given PATHOBJ before calling <b>PATHOBJ_bEnum</b>.

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
<a href="https://msdn.microsoft.com/library/windows/hardware/ff568850">PATHOBJ_bCloseFigure</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff568851">PATHOBJ_bEnum</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff568852">PATHOBJ_bEnumClipLines</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff568853">PATHOBJ_bMoveTo</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff568854">PATHOBJ_bPolyBezierTo</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff568855">PATHOBJ_bPolyLineTo</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff568856">PATHOBJ_vEnumStart</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff568857">PATHOBJ_vEnumStartClipLines</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff568858">PATHOBJ_vGetBounds</a>
</dt>
</dl>





## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556220">DrvFillPath</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556311">DrvStrokeAndFillPath</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556316">DrvStrokePath</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564755">EngCreatePath</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564811">EngDeletePath</a>
 

 

