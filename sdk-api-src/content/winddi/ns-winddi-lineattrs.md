---
UID: NS:winddi._LINEATTRS
title: LINEATTRS (winddi.h)
description: The LINEATTRS structure is used by a driver's line-drawing functions to determine line attributes.
helpviewer_keywords: ["*PLINEATTRS","LINEATTRS","LINEATTRS structure [Display Devices]","PLINEATTRS","PLINEATTRS structure pointer [Display Devices]","display.lineattrs","grstrcts_2e75edb5-bba8-4f62-b7f4-e3af44794eb2.xml","winddi/LINEATTRS","winddi/PLINEATTRS"]
old-location: display\lineattrs.htm
tech.root: display
ms.assetid: 40fcd6e2-7ed4-433f-ab8b-cc75a305adb9
ms.date: 12/05/2018
ms.keywords: '*PLINEATTRS, LINEATTRS, LINEATTRS structure [Display Devices], PLINEATTRS, PLINEATTRS structure pointer [Display Devices], display.lineattrs, grstrcts_2e75edb5-bba8-4f62-b7f4-e3af44794eb2.xml, winddi/LINEATTRS, winddi/PLINEATTRS'
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
req.typenames: LINEATTRS, *PLINEATTRS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _LINEATTRS
 - winddi/_LINEATTRS
 - PLINEATTRS
 - winddi/PLINEATTRS
 - LINEATTRS
 - winddi/LINEATTRS
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
 - LINEATTRS
---

# LINEATTRS structure


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

Specifies a FLOAT_LONG that indicates the width of the line. This width is measured in FLOAT world coordinates for a geometric wide line, but in LONG device coordinates for a cosmetic wide line. For a description of the FLOAT_LONG data type, see <a href="/windows-hardware/drivers/display/gdi-data-types">GDI Data Types</a>.

### -field eMiterLimit

Specifies a FLOATL that sets the limit as a multiple of the line width that a miter join is allowed to extend from its inside corner to its outer vertex. This prevents very long spikes from occurring when lines of a path meet at very small angles. If the miter limit is exceeded, a bevel join should be used instead. For a description of the FLOATL data type, see <a href="/windows-hardware/drivers/display/gdi-data-types">GDI Data Types</a>.

This member is used only by geometric wide lines.

### -field cstyle

Specifies the number of entries in the style array pointed to by the <b>pstyle</b> member.

### -field pstyle

Pointer to an array of FLOAT_LONG elements: the style array. If this member is <b>NULL</b>, the line style is solid. For a description of the FLOAT_LONG data type, see <a href="/windows-hardware/drivers/display/gdi-data-types">GDI Data Types</a>.

### -field elStyleState

Specifies a FLOAT_LONG that contains a pair of 16-bit values supplied by GDI whenever the driver calls <a href="/windows/desktop/api/winddi/nf-winddi-pathobj_benumcliplines">PATHOBJ_bEnumClipLines</a>. These two values, packed into a FLOAT_LONG, specify where in the styling array (at which pixel) to start the first subpath. This value must be updated as part of the output routine if the line is not solid. This member applies to cosmetic lines only

. See also <a href="/windows-hardware/drivers/display/styled-cosmetic-lines">Styled Cosmetic Lines</a> for additional information.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvstrokeandfillpath">DrvStrokeAndFillPath</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvstrokepath">DrvStrokePath</a>



<a href="/windows/desktop/api/winddi/nf-winddi-pathobj_venumstartcliplines">PATHOBJ_vEnumStartClipLines</a>