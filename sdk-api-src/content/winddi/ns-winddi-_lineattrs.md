---
UID: NS:winddi._LINEATTRS
title: "_LINEATTRS"
author: windows-sdk-content
description: The LINEATTRS structure is used by a driver's line-drawing functions to determine line attributes.
old-location: display\lineattrs.htm
tech.root: display
ms.assetid: 40fcd6e2-7ed4-433f-ab8b-cc75a305adb9
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: "*PLINEATTRS, LINEATTRS, LINEATTRS structure [Display Devices], PLINEATTRS, PLINEATTRS structure pointer [Display Devices], _LINEATTRS, display.lineattrs, grstrcts_2e75edb5-bba8-4f62-b7f4-e3af44794eb2.xml, winddi/LINEATTRS, winddi/PLINEATTRS"
ms.prod: windows
ms.technology: windows-sdk
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - LINEATTRS
product: Windows
targetos: Windows
req.typenames: LINEATTRS, *PLINEATTRS
req.redist: 
---

# _LINEATTRS structure


## -description


The LINEATTRS structure is used by a driver's line-drawing functions to determine line attributes.


## -struct-fields




### -field fl

Option flags. This member can be one of the following values:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
LA_ALTERNATE

</td>
<td>
A special cosmetic line style; every other pixel is on.

</td>
</tr>
<tr>
<td>
LA_GEOMETRIC

</td>
<td>
A geometric wide line.

</td>
</tr>
<tr>
<td>
LA_STARTGAP

</td>
<td>
The first entry in the style array specifies the length of the first gap.

</td>
</tr>
<tr>
<td>
LA_STYLED

</td>
<td>
The line is a styled line.

</td>
</tr>
</table>
 


### -field iJoin

Specifies join styles for geometric wide lines. This member can be one of the following values:

<table>
<tr>
<th>Join Style</th>
<th>Meaning</th>
</tr>
<tr>
<td>
JOIN_BEVEL

</td>
<td>
The joining edges of wide lines are beveled.

</td>
</tr>
<tr>
<td>
JOIN_MITER

</td>
<td>
The joining edges of wide lines are mitered.

</td>
</tr>
<tr>
<td>
JOIN_ROUND

</td>
<td>
The joining edges of wide lines are rounded.

</td>
</tr>
</table>
 


### -field iEndCap

Specifies the end cap style for a geometric wide line. This member can be one of the following values:

<table>
<tr>
<th>End Cap Style</th>
<th>Meaning</th>
</tr>
<tr>
<td>
ENDCAP_BUTT

</td>
<td>
The end cap is

</td>
</tr>
<tr>
<td>
ENDCAP_ROUND

</td>
<td>
The end cap is rounded.

</td>
</tr>
<tr>
<td>
ENDCAP_SQUARE

</td>
<td>
The end cap is square.

</td>
</tr>
</table>
 


### -field elWidth

Specifies a FLOAT_LONG that indicates the width of the line. This width is measured in FLOAT world coordinates for a geometric wide line, but in LONG device coordinates for a cosmetic wide line. For a description of the FLOAT_LONG data type, see <a href="https://msdn.microsoft.com/2054aa16-6d86-4db3-8b16-4570b0374e23">GDI Data Types</a>.


### -field eMiterLimit

Specifies a FLOATL that sets the limit as a multiple of the line width that a miter join is allowed to extend from its inside corner to its outer vertex. This prevents very long spikes from occurring when lines of a path meet at very small angles. If the miter limit is exceeded, a bevel join should be used instead. For a description of the FLOATL data type, see <a href="https://msdn.microsoft.com/2054aa16-6d86-4db3-8b16-4570b0374e23">GDI Data Types</a>.

This member is used only by geometric wide lines.


### -field cstyle

Specifies the number of entries in the style array pointed to by the <b>pstyle</b> member.


### -field pstyle

Pointer to an array of FLOAT_LONG elements: the style array. If this member is <b>NULL</b>, the line style is solid. For a description of the FLOAT_LONG data type, see <a href="https://msdn.microsoft.com/2054aa16-6d86-4db3-8b16-4570b0374e23">GDI Data Types</a>.


### -field elStyleState

Specifies a FLOAT_LONG that contains a pair of 16-bit values supplied by GDI whenever the driver calls <a href="https://msdn.microsoft.com/edc64b1e-dd3f-4b6a-858c-91c49a819b0a">PATHOBJ_bEnumClipLines</a>. These two values, packed into a FLOAT_LONG, specify where in the styling array (at which pixel) to start the first subpath. This value must be updated as part of the output routine if the line is not solid. This member applies to cosmetic lines only

. See also <a href="https://msdn.microsoft.com/07e72190-7c8e-471e-9851-ccc037312c5c">Styled Cosmetic Lines</a> for additional information.


## -see-also




<a href="https://msdn.microsoft.com/92a04fe5-146d-4839-a854-1ac50705b447">DrvStrokeAndFillPath</a>



<a href="https://msdn.microsoft.com/c931a39d-c0ae-4f40-b70f-f51d5621c228">DrvStrokePath</a>



<a href="https://msdn.microsoft.com/3db437aa-40d1-4703-ab1e-b3e154923d2d">PATHOBJ_vEnumStartClipLines</a>
 

 

