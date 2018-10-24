---
UID: NF:d2d1_2.ID2D1CommandSink1.SetPrimitiveBlend1
title: ID2D1CommandSink1::SetPrimitiveBlend1
author: windows-sdk-content
description: Sets a new primitive blend mode.
old-location: direct2d\id2d1commandsink_setprimitiveblend1.htm
tech.root: Direct2D
ms.assetid: 3EA9EC07-1B2F-48A2-ABFB-2DA0E2EFFBF4
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: ID2D1CommandSink1 interface [Direct2D],SetPrimitiveBlend1 method, ID2D1CommandSink1.SetPrimitiveBlend1, ID2D1CommandSink1::SetPrimitiveBlend1, SetPrimitiveBlend1, SetPrimitiveBlend1 method [Direct2D], SetPrimitiveBlend1 method [Direct2D],ID2D1CommandSink1 interface, d2d1_2/ID2D1CommandSink1::SetPrimitiveBlend1, direct2d.id2d1commandsink_setprimitiveblend1
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - COM
api_location:
 - d2d1_2.h
api_name:
 - ID2D1CommandSink1.SetPrimitiveBlend1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1CommandSink1::SetPrimitiveBlend1


## -description


Sets a new primitive blend mode. 


## -parameters




### -param primitiveBlend

Type: <b><a href="https://msdn.microsoft.com/411a42c9-f8d7-46f3-a6e6-51afc83375ad">D2D1_PRIMITIVE_BLEND</a></b>

The primitive blend that will apply to subsequent primitives.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code. 





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
<td>The resulting pixel values use the minimum of the source and destination pixel values. Available in Windows 8 and later.</td>
</tr>
<tr>
<td>D2D1_PRIMITIVE_BLEND_ADD</td>
<td>O = (S + D) * C + D * (1 – C)</td>
<td>O = S * C + D</td>
<td>The resulting pixel values are the sum of the source and destination pixel values. Available in Windows 8 and later.</td>
</tr>
</table>
 

<img alt="An illustration of Direct2D primitive blend modes with varying opacity and backgrounds." src="images/PrimBlendDemo.png"/>
An illustration of the primitive blend modes with varying opacity and backgrounds.

The primitive blend will apply to all of the primitive drawn on the context, unless this is overridden with the <i>compositeMode</i> parameter on the <a href="https://msdn.microsoft.com/c41d8a79-280a-451e-b07b-f904d07da5c7">DrawImage</a> API.

The primitive blend applies to the interior of any primitives drawn on the context. In the case of <a href="https://msdn.microsoft.com/c41d8a79-280a-451e-b07b-f904d07da5c7">DrawImage</a>, this will be implied by the image rectangle, offset and world transform.

If the primitive blend is anything other than <b>D2D1_PRIMITIVE_BLEND_OVER</b> then ClearType rendering will be turned off. If the application explicitly forces ClearType rendering in these modes, the drawing context will be placed in an error state. D2DERR_WRONG_STATE will be returned from either <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">EndDraw</a> or <a href="https://msdn.microsoft.com/3ad9c966-85f5-4ddb-a8c1-aefcba533509">Flush</a>.





## -see-also




<a href="https://msdn.microsoft.com/126319DE-3E84-4070-A516-9291759593B7">ID2D1CommandSink1</a>
 

 

