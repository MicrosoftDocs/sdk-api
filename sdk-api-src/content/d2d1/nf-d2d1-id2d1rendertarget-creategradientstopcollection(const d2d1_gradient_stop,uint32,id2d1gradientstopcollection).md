---
UID: NF:d2d1.ID2D1RenderTarget.CreateGradientStopCollection(const D2D1_GRADIENT_STOP,UINT32,ID2D1GradientStopCollection)
title: ID2D1RenderTarget::CreateGradientStopCollection(const D2D1_GRADIENT_STOP,UINT32,ID2D1GradientStopCollection)
author: windows-sdk-content
description: Creates an ID2D1GradientStopCollection from the specified array of D2D1_GRADIENT_STOP structures.
old-location: direct2d\id2d1rendertarget_creategradientstopcollection.htm
tech.root: Direct2D
ms.assetid: 674ffba5-18c5-46bf-8813-d8d13e5ba903
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: CreateGradientStopCollection, CreateGradientStopCollection methods [Direct2D], ID2D1RenderTarget.CreateGradientStopCollection, ID2D1RenderTarget.CreateGradientStopCollection(const D2D1_GRADIENT_STOP,UINT32,ID2D1GradientStopCollection), ID2D1RenderTarget::CreateGradientStopCollection, ID2D1RenderTarget::CreateGradientStopCollection(const D2D1_GRADIENT_STOP,UINT32,ID2D1GradientStopCollection), d2d1_1/CreateGradientStopCollection, direct2d.id2d1rendertarget_creategradientstopcollection
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1.h
req.include-header: D2d1.h
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
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - ID2D1RenderTarget::CreateGradientStopCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget::CreateGradientStopCollection(const D2D1_GRADIENT_STOP,UINT32,ID2D1GradientStopCollection)


## -description


<span>     Creates an <a href="https://msdn.microsoft.com/982abf9c-4778-4871-a494-5843f0c0addc">ID2D1GradientStopCollection</a> from the specified array of <a href="https://msdn.microsoft.com/f6798542-382a-4074-bbe1-707bc00b3575">D2D1_GRADIENT_STOP</a> structures. 
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c5f3facf-f1fe-4a47-b283-c0c859d8bc03">CreateGradientStopCollection(D2D1_GRADIENT_STOP*,D2D1_GAMMA,D2D1_EXTEND_MODE,ID2D1GradientStopCollection**)</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/982abf9c-4778-4871-a494-5843f0c0addc">ID2D1GradientStopCollection</a> from the specified gradient stops, color interpolation gamma, and extend mode.  

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0351e843-18cc-402b-8e4d-3f834de9501a">CreateGradientStopCollection(D2D1_GRADIENT_STOP*,ID2D1GradientStopCollection**)</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/982abf9c-4778-4871-a494-5843f0c0addc">ID2D1GradientStopCollection</a> from the specified gradient stops that uses the <a href="https://msdn.microsoft.com/c84c66c6-5f4a-41de-938c-76a409145971">D2D1_GAMMA_2_2</a> color interpolation gamma and the clamp extend mode.

</td>
</tr>
</table>

## -parameters


## -see-also




<a href="https://msdn.microsoft.com/7a31d9e7-0521-40ee-b2c1-592dfaf5301e">Brushes Overview</a>



<a href="https://msdn.microsoft.com/f6798542-382a-4074-bbe1-707bc00b3575">D2D1_GRADIENT_STOP</a>



<a href="https://msdn.microsoft.com/3cf5acc6-2f17-49d4-aca5-a84a846d1749">How to Create a Linear Gradient Brush</a>



<a href="https://msdn.microsoft.com/663743c9-16e9-4e3a-90b2-883ef0b8d5cf">How to Create a Radial Gradient Brush</a>



<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

