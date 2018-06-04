---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

