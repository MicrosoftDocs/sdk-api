---
UID: NS:winddi._CLIPOBJ
title: CLIPOBJ (winddi.h)
description: The CLIPOBJ structure describes the clip region used when drawing.
helpviewer_keywords: ["CLIPOBJ","CLIPOBJ structure [Display Devices]","display.clipobj","grstrcts_028034f6-2370-4e77-be77-7bc8e9ee8504.xml","winddi/CLIPOBJ"]
old-location: display\clipobj.htm
tech.root: display
ms.assetid: c3f632ed-f8d1-44bb-b2fb-6f7f2c71fd63
ms.date: 12/05/2018
ms.keywords: CLIPOBJ, CLIPOBJ structure [Display Devices], display.clipobj, grstrcts_028034f6-2370-4e77-be77-7bc8e9ee8504.xml, winddi/CLIPOBJ
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
req.typenames: CLIPOBJ
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLIPOBJ
 - winddi/_CLIPOBJ
 - CLIPOBJ
 - winddi/CLIPOBJ
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
 - CLIPOBJ
---

# CLIPOBJ structure


## -description

The CLIPOBJ structure describes the clip region used when drawing.

## -struct-fields

### -field iUniq

Specifies a value that uniquely identifies the clip region. If <b>iUniq</b> is nonzero, the driver uses it as a cache identifier. This allows the driver to recognize a region after downloading and caching it. If the value is zero, the driver should not cache the region because the region will not be used again.

### -field rclBounds

Specifies a <a href="/windows/desktop/api/windef/ns-windef-rectl">RECTL</a> structure that bounds the part of the region that intersects the drawing. If <b>iDComplexity</b> is DC_RECT, then this is the clipping rectangle to be considered.

### -field iDComplexity

Specifies the complexity of the part of the region that intersects with the drawing. This member must be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DC_COMPLEX

</td>
<td>
The clip region must be enumerated.

</td>
</tr>
<tr>
<td>
DC_RECT

</td>
<td>
Clip to a single rectangle.

</td>
</tr>
<tr>
<td>
DC_TRIVIAL

</td>
<td>
Clipping need not be considered; draw the whole figure.

</td>
</tr>
</table>

### -field iFComplexity

Specifies the complexity of the whole region. This value is used by the driver in deciding whether to cache the region. <a href="/windows/desktop/api/winddi/nf-winddi-clipobj_cenumstart">CLIPOBJ_cEnumStart</a> can be called to determine the exact number of rectangles in the region. This member can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
FC_COMPLEX

</td>
<td>
The region consists of more than four rectangles.

</td>
</tr>
<tr>
<td>
FC_RECT

</td>
<td>
The region is a single rectangle.

</td>
</tr>
<tr>
<td>
FC_RECT4

</td>
<td>
The region consists of, at most, four rectangles.

</td>
</tr>
</table>

### -field iMode

Specifies how the region is stored by GDI. This can help the driver determine how to enumerate the region. This member can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
TC_PATHOBJ

</td>
<td>
The region is stored as a path.

</td>
</tr>
<tr>
<td>
TC_RECTANGLES

</td>
<td>
The region is stored as rectangles.

</td>
</tr>
</table>

### -field fjOptions

Specifies clipping options. This member can be the following value:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
OC_BANK_CLIP

</td>
<td>
<b>Obsolete</b>. Indicates an engine callback for a banked device.

</td>
</tr>
</table>

## -remarks

The region, described by CLIPOBJ, can be enumerated as a series of rectangles.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-clipobj_benum">CLIPOBJ_bEnum</a>



<a href="/windows/desktop/api/winddi/nf-winddi-clipobj_cenumstart">CLIPOBJ_cEnumStart</a>



<a href="/windows/desktop/api/windef/ns-windef-rectl">RECTL</a>