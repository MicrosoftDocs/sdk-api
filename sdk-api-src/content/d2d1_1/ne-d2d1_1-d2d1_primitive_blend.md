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

# D2D1_PRIMITIVE_BLEND enumeration


## -description



        Used to specify the geometric blend mode for all Direct2D primitives.
      


## -enum-fields




### -field D2D1_PRIMITIVE_BLEND_SOURCE_OVER

The standard source-over-destination blend mode.


### -field D2D1_PRIMITIVE_BLEND_COPY

The source is copied to the destination; the destination pixels are ignored.


### -field D2D1_PRIMITIVE_BLEND_MIN


              The resulting pixel values use the minimum of the source and destination pixel values. Available in Windows 8 and later.
            


### -field D2D1_PRIMITIVE_BLEND_ADD


              The resulting pixel values are the sum of the source and destination pixel values. Available in Windows 8 and later.
            


### -field D2D1_PRIMITIVE_BLEND_MAX

The resulting pixel values use the maximum of the source and destination pixel values. 
          Available in Windows 10 and later (set using <a href="https://msdn.microsoft.com/20934CEA-2B89-45F5-8E61-CD47C4A9B78F">ID21CommandSink4::SetPrimitiveBlend2</a>).


### -field D2D1_PRIMITIVE_BLEND_FORCE_DWORD




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
<td>
                The resulting pixel values use the minimum of the source and destination pixel values. Available in Windows 8.1 and later.
              </td>
</tr>
<tr>
<td>D2D1_PRIMITIVE_BLEND_ADD</td>
<td>O = (S + D) * C + D * (1 – C)</td>
<td>O = S * C + D</td>
<td>
                The resulting pixel values are the sum of the source and destination pixel values. Available in Windows 8.1 and later.
              </td>
</tr>
</table>
 

<img alt="An illustration of Direct2D primitive blend modes with varying opacity and backgrounds." src="images/PrimBlendDemo.png"/>
An illustration of the primitive blend modes with varying opacity and backgrounds.




## -see-also




<a href="https://msdn.microsoft.com/c3d6cfae-5776-4d1d-933b-b94271c431b6">ID2D1DeviceContext::GetPrimitiveBlend</a>



<a href="https://msdn.microsoft.com/be04c9f7-397f-468e-91c0-3b11c68b489f">ID2D1DeviceContext::SetPrimitiveBlend</a>
 

 

