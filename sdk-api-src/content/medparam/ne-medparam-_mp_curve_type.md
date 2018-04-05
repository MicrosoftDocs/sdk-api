---
UID: NE:medparam._MP_CURVE_TYPE
title: "_MP_CURVE_TYPE"
author: windows-driver-content
description: The MP_CURVE_TYPE enumeration defines the curve that a media parameter follows within an envelope segment.
old-location: dshow\mp_curve_type.htm
old-project: DirectShow
ms.assetid: 0665796e-5589-4e6c-b101-e19eddec7e0d
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: MP_CURVE_INVSQUARE, MP_CURVE_JUMP, MP_CURVE_LINEAR, MP_CURVE_SINE, MP_CURVE_SQUARE, MP_CURVE_TYPE, MP_CURVE_TYPE enumeration [DirectShow], MP_CURVE_TYPEEnumeration, _MP_CURVE_TYPE, dshow.mp_curve_type, medparam/MP_CURVE_INVSQUARE, medparam/MP_CURVE_JUMP, medparam/MP_CURVE_LINEAR, medparam/MP_CURVE_SINE, medparam/MP_CURVE_SQUARE, medparam/MP_CURVE_TYPE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: MP_CURVE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Medparam.h
api_name:
-	MP_CURVE_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MP_CURVE_TYPE enumeration


## -description



The <code>MP_CURVE_TYPE</code> enumeration defines the curve that a media parameter follows within an envelope segment.




## -enum-fields




### -field MP_CURVE_JUMP

No interpolation. Jump to the next point.


### -field MP_CURVE_LINEAR

Linear interpolation.


### -field MP_CURVE_SQUARE

Parabolic curve.


### -field MP_CURVE_INVSQUARE

Inverse square curve.


### -field MP_CURVE_SINE

Sine curve.


## -remarks



The following table lists the defined curves and their mathematical equivalents.

<table>
<tr>
<th>
              Value
            </th>
<th>
              Curve to Fit
            </th>
<th>
              Range
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




<a href="https://msdn.microsoft.com/5d60c902-5fb0-419b-b54d-5e3b543c5df8">DMO Enumerated Types</a>



<a href="https://msdn.microsoft.com/b7386b63-c563-42dd-851c-780bf1043f65">MP_ENVELOPE_SEGMENT</a>
 

 

