---
UID: NE:medparam._MP_CURVE_TYPE
title: MP_CURVE_TYPE (medparam.h)
description: The MP_CURVE_TYPE enumeration defines the curve that a media parameter follows within an envelope segment.
helpviewer_keywords: ["MP_CURVE_INVSQUARE","MP_CURVE_JUMP","MP_CURVE_LINEAR","MP_CURVE_SINE","MP_CURVE_SQUARE","MP_CURVE_TYPE","MP_CURVE_TYPE","MP_CURVE_TYPE enumeration [DirectShow]","MP_CURVE_TYPEEnumeration","dshow.mp_curve_type","medparam/MP_CURVE_INVSQUARE","medparam/MP_CURVE_JUMP","medparam/MP_CURVE_LINEAR","medparam/MP_CURVE_SINE","medparam/MP_CURVE_SQUARE","medparam/MP_CURVE_TYPE"]
old-location: dshow\mp_curve_type.htm
tech.root: dshow
ms.assetid: 0665796e-5589-4e6c-b101-e19eddec7e0d
ms.date: 12/05/2018
ms.keywords: MP_CURVE_INVSQUARE, MP_CURVE_JUMP, MP_CURVE_LINEAR, MP_CURVE_SINE, MP_CURVE_SQUARE, MP_CURVE_TYPE, MP_CURVE_TYPE , MP_CURVE_TYPE enumeration [DirectShow], MP_CURVE_TYPEEnumeration, dshow.mp_curve_type, medparam/MP_CURVE_INVSQUARE, medparam/MP_CURVE_JUMP, medparam/MP_CURVE_LINEAR, medparam/MP_CURVE_SINE, medparam/MP_CURVE_SQUARE, medparam/MP_CURVE_TYPE
req.header: medparam.h
req.include-header: 
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
req.typenames: MP_CURVE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MP_CURVE_TYPE
 - medparam/_MP_CURVE_TYPE
 - MP_CURVE_TYPE
 - medparam/MP_CURVE_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Medparam.h
api_name:
 - MP_CURVE_TYPE
---

# MP_CURVE_TYPE enumeration


## -description

The <code>MP_CURVE_TYPE</code> enumeration defines the curve that a media parameter follows within an envelope segment.

## -enum-fields

### -field MP_CURVE_JUMP:0x1

No interpolation. Jump to the next point.

### -field MP_CURVE_LINEAR:0x2

Linear interpolation.

### -field MP_CURVE_SQUARE:0x4

Parabolic curve.

### -field MP_CURVE_INVSQUARE:0x8

Inverse square curve.

### -field MP_CURVE_SINE:0x10

Sine curve.

## -remarks

The following table lists the defined curves and their mathematical equivalents.

<table>
<tr>
<th>Value
            </th>
<th>Curve to Fit
            </th>
<th>Range
            </th>
</tr>
<tr>
<td>MP_CURVE_LINEAR</td>
<td><i>y</i> = <i>x</i></td>
<td>0.0 – 1.0</td>
</tr>
<tr>
<td>MP_CURVE_SQUARE</td>
<td><i>y</i> = <i>x</i>^2</td>
<td>0.0 – 1.0</td>
</tr>
<tr>
<td>MP_CURVE_INVSQUARE</td>
<td><i>y</i> = 1 –<i>x</i>^2</td>
<td>0.0 – 1.0</td>
</tr>
<tr>
<td>MP_CURVE_SINE</td>
<td><i>y</i> = sin(<i>x</i>)</td>
<td>–π/2 – π/2</td>
</tr>
</table>
 

For Boolean and enumeration parameters, only MP_CURVE_JUMP is valid.

## -see-also

<a href="/windows/desktop/DirectShow/dmo-enumerated-types">DMO Enumerated Types</a>



<a href="/previous-versions/windows/desktop/api/medparam/ns-medparam-mp_envelope_segment">MP_ENVELOPE_SEGMENT</a>
