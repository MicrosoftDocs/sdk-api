---
UID: NF:d2d1.CreateRadialGradientBrush
title: CreateRadialGradientBrush function
author: windows-driver-content
description: Creates an ID2D1RadialGradientBrush object that can be used to paint areas with a radial gradient.
old-location: direct2d\id2d1rendertarget_createradialgradientbrush.htm
old-project: Direct2D
ms.assetid: 985a4c1b-d29b-46ed-bc55-6dcd313718a8
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: CreateRadialGradientBrush, CreateRadialGradientBrush methods [Direct2D], ID2D1RenderTarget::CreateRadialGradientBrush, d2d1/CreateRadialGradientBrush, direct2d.id2d1rendertarget_createradialgradientbrush
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: d2d1.h
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
req.typenames: D2D1_WINDOW_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	D2d1.dll
api_name:
-	ID2D1RenderTarget::CreateRadialGradientBrush
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# CreateRadialGradientBrush function


## -description


<span>Creates an <a href="https://msdn.microsoft.com/21ed2286-e4df-4b77-ba31-e5d5927e16f5">ID2D1RadialGradientBrush</a> object that can be used to paint areas with a radial gradient.
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/177d0b8c-82ae-4d2a-ae43-246352b92166">CreateRadialGradientBrush(D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES&,ID2D1GradientStopCollection*,ID2D1RadialGradientBrush**)</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/21ed2286-e4df-4b77-ba31-e5d5927e16f5">ID2D1RadialGradientBrush</a> that contains the specified gradient stops, has no transform, and has a base opacity of 1.0.
    
    

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df87e288-392d-439e-8d03-e4866fde892f">CreateRadialGradientBrush(D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES&,D2D1_BRUSH_PROPERTIES&,ID2D1GradientStopCollection*,ID2D1RadialGradientBrush**)</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/21ed2286-e4df-4b77-ba31-e5d5927e16f5">ID2D1RadialGradientBrush</a> that contains the specified gradient stops and has the specified transform and base opacity.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6d4f4ba0-1d1d-477f-a721-898a259df022">CreateRadialGradientBrush(D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES*,D2D1_BRUSH_PROPERTIES*,ID2D1GradientStopCollection*,ID2D1RadialGradientBrush**)</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/21ed2286-e4df-4b77-ba31-e5d5927e16f5">ID2D1RadialGradientBrush</a> that contains the specified gradient stops and has the specified transform and base opacity.
    

</td>
</tr>
</table>

## -parameters


## -see-also




<a href="https://msdn.microsoft.com/7a31d9e7-0521-40ee-b2c1-592dfaf5301e">Brushes Overview</a>



<a href="https://msdn.microsoft.com/663743c9-16e9-4e3a-90b2-883ef0b8d5cf">How to Create a Radial Gradient Brush</a>



<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

