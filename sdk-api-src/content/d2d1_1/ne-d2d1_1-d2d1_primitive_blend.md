---
UID: NE:d2d1_1.D2D1_PRIMITIVE_BLEND
title: D2D1_PRIMITIVE_BLEND (d2d1_1.h)
description: Used to specify the geometric blend mode for all Direct2D primitives.
helpviewer_keywords: ["D2D1_PRIMITIVE_BLEND","D2D1_PRIMITIVE_BLEND enumeration [Direct2D]","D2D1_PRIMITIVE_BLEND_ADD","D2D1_PRIMITIVE_BLEND_COPY","D2D1_PRIMITIVE_BLEND_MAX","D2D1_PRIMITIVE_BLEND_MIN","D2D1_PRIMITIVE_BLEND_SOURCE_OVER","d2d1_1/D2D1_PRIMITIVE_BLEND","d2d1_1/D2D1_PRIMITIVE_BLEND_ADD","d2d1_1/D2D1_PRIMITIVE_BLEND_COPY","d2d1_1/D2D1_PRIMITIVE_BLEND_MAX","d2d1_1/D2D1_PRIMITIVE_BLEND_MIN","d2d1_1/D2D1_PRIMITIVE_BLEND_SOURCE_OVER","direct2d.__d2d1_primitive_blend"]
old-location: direct2d\__d2d1_primitive_blend.htm
tech.root: Direct2D
ms.assetid: 411a42c9-f8d7-46f3-a6e6-51afc83375ad
ms.date: 12/05/2018
ms.keywords: D2D1_PRIMITIVE_BLEND, D2D1_PRIMITIVE_BLEND enumeration [Direct2D], D2D1_PRIMITIVE_BLEND_ADD, D2D1_PRIMITIVE_BLEND_COPY, D2D1_PRIMITIVE_BLEND_MAX, D2D1_PRIMITIVE_BLEND_MIN, D2D1_PRIMITIVE_BLEND_SOURCE_OVER, d2d1_1/D2D1_PRIMITIVE_BLEND, d2d1_1/D2D1_PRIMITIVE_BLEND_ADD, d2d1_1/D2D1_PRIMITIVE_BLEND_COPY, d2d1_1/D2D1_PRIMITIVE_BLEND_MAX, d2d1_1/D2D1_PRIMITIVE_BLEND_MIN, d2d1_1/D2D1_PRIMITIVE_BLEND_SOURCE_OVER, direct2d.__d2d1_primitive_blend
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: D2D1_PRIMITIVE_BLEND
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_PRIMITIVE_BLEND
 - d2d1_1/D2D1_PRIMITIVE_BLEND
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D2d1_1.h
api_name:
 - D2D1_PRIMITIVE_BLEND
---

# D2D1_PRIMITIVE_BLEND enumeration


## -description

Used to specify the geometric blend mode for all Direct2D primitives.

## -enum-fields

### -field D2D1_PRIMITIVE_BLEND_SOURCE_OVER:0

The standard source-over-destination blend mode.

### -field D2D1_PRIMITIVE_BLEND_COPY:1

The source is copied to the destination; the destination pixels are ignored.

### -field D2D1_PRIMITIVE_BLEND_MIN:2

The resulting pixel values use the minimum of the source and destination pixel values. Available in Windows 8 and later.

### -field D2D1_PRIMITIVE_BLEND_ADD:3

The resulting pixel values are the sum of the source and destination pixel values. Available in Windows 8 and later.

### -field D2D1_PRIMITIVE_BLEND_MAX:4

The resulting pixel values use the maximum of the source and destination pixel values. 
          Available in Windows 10 and later (set using <a href="/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1commandsink4-setprimitiveblend2">ID21CommandSink4::SetPrimitiveBlend2</a>).

### -field D2D1_PRIMITIVE_BLEND_FORCE_DWORD:0xffffffff

## -remarks

<h3><a id="Blend_modes"></a><a id="blend_modes"></a><a id="BLEND_MODES"></a>Blend modes</h3>
For aliased rendering (except for MIN mode), the output value O is computed by linearly interpolating the value <i>blend(S, D)</i> with the destination pixel value, based on the amount that the primitive covers the destination pixel.
          



The table here shows the primitive blend modes for both aliased and antialiased blending. The equations listed in the table  use these elements:
            <ul>
<li>O = Output</li>
<li>S = Source</li>
<li>SA = Source Alpha</li>
<li>D = Destination</li>
<li>DA = Destination Alpha</li>
<li>C = Pixel coverage</li>
</ul>


<table>
<tr>
<th>Primitive blend mode</th>
<th>Aliased blending</th>
<th>Antialiased blending</th>
<th>Description</th>
</tr>
<tr>
<td>D2D1_PRIMITIVE_BLEND_SOURCE_OVER</td>
<td>O = (S + (1 – SA) * D) * C + D * (1 – C)</td>
<td>O = S * C + D *(1 – SA *C)</td>
<td>The standard source-over-destination blend mode.</td>
</tr>
<tr>
<td>D2D1_PRIMITIVE_BLEND_COPY</td>
<td>O = S * C + D * (1 – C)</td>
<td>O = S * C + D * (1 – C)</td>
<td>The source is copied to the destination; the destination pixels are ignored.</td>
</tr>
<tr>
<td>D2D1_PRIMITIVE_BLEND_MIN</td>
<td>O = Min(S + 1-SA, D) </td>
<td>O = Min(S * C + 1 – SA *C, D)</td>
<td>The resulting pixel values use the minimum of the source and destination pixel values. Available in Windows 8.1 and later.
              </td>
</tr>
<tr>
<td>D2D1_PRIMITIVE_BLEND_ADD</td>
<td>O = (S + D) * C + D * (1 – C)</td>
<td>O = S * C + D</td>
<td>The resulting pixel values are the sum of the source and destination pixel values. Available in Windows 8.1 and later.
              </td>
</tr>
</table>
 

<img alt="An illustration of Direct2D primitive blend modes with varying opacity and backgrounds." src="./images/PrimBlendDemo.png"/>
An illustration of the primitive blend modes with varying opacity and backgrounds.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-getprimitiveblend">ID2D1DeviceContext::GetPrimitiveBlend</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setprimitiveblend">ID2D1DeviceContext::SetPrimitiveBlend</a>
