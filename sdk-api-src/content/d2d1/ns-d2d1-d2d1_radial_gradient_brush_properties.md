---
UID: NS:d2d1.D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES
title: D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES
author: windows-sdk-content
description: Contains the gradient origin offset and the size and position of the gradient ellipse for an ID2D1RadialGradientBrush.
old-location: direct2d\D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES.htm
old-project: Direct2D
ms.assetid: 194f7624-ac3b-4054-8d6f-5b4c99ef6546
ms.author: windowssdkdev
ms.date: 04/20/2018
ms.keywords: D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES, D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES structure [Direct2D], d2d1/D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES, direct2d.D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES structure


## -description



    Contains the gradient origin offset and the size and position of the gradient ellipse for an <a href="https://msdn.microsoft.com/21ed2286-e4df-4b77-ba31-e5d5927e16f5">ID2D1RadialGradientBrush</a>. 


## -struct-fields




### -field center

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

In the brush's coordinate space, the center of the gradient ellipse.


### -field gradientOriginOffset

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

In the brush's coordinate space, the offset of the gradient origin relative to the gradient ellipse's center.


### -field radiusX

Type: <b>FLOAT</b>

In the brush's coordinate space, the x-radius  of the gradient ellipse.


### -field radiusY

Type: <b>FLOAT</b>

In the brush's coordinate space, the y-radius  of the gradient ellipse.


## -remarks



Different values for <i>center</i>,  <i>gradientOriginOffset</i>,  <i>radiusX</i> and/or <i>radiusY</i> produce different gradients.   The following illustration shows several radial gradients that have different gradient origin offsets, creating the appearance of the light illuminating the circles from different angles.

<img alt="Illustration of four circles with radial gradients that have different origin offsets" src="./images/RadialGradient.png"/>

For convenience, Direct2D provides the <a href="https://msdn.microsoft.com/d65ee26c-28d4-4b58-9089-1aab959246cc">D2D1::RadialGradientBrushProperties</a> function for creating new <b>D2D1_RADIAL_GRADIENT_BRUSH</b> structures.


#### Examples

The following example calls <a href="https://msdn.microsoft.com/985a4c1b-d29b-46ed-bc55-6dcd313718a8">CreateRadialGradientBrush</a> to create an <a href="https://msdn.microsoft.com/21ed2286-e4df-4b77-ba31-e5d5927e16f5">ID2D1RadialGradientBrush</a>. It uses the <a href="https://msdn.microsoft.com/d65ee26c-28d4-4b58-9089-1aab959246cc">D2D1::RadialGradientBrushProperties</a> helper function to create a <b>D2D1_RADIAL_GRADIENT_BRUSH</b> structure that has a <i>center</i> value of (75, 5), a <i>gradientOriginOffset</i> of (0, 0), and a <i>radiusX</i> and <i>radiusY</i> of to 75 and passes the structure to the <b>CreateRadialGradientBrush</b> method.   When the gradient brush is used to fill a rectangle, it produces output as shown in the following illustration.

<img alt="Illustration of a circle with a radial gradient brush" src="./images/brushes_ovw_radials.png"/>

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// The center of the gradient is in the center of the box.
// The gradient origin offset was set to zero(0, 0) or center in this case.
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget-&gt;CreateRadialGradientBrush(
        D2D1::RadialGradientBrushProperties(
            D2D1::Point2F(75, 75),
            D2D1::Point2F(0, 0),
            75,
            75),
        pGradientStops,
        &amp;m_pRadialGradientBrush
        );
}
</pre>
</td>
</tr>
</table></span></div>
For more information about radial gradient brushes, see the <a href="https://msdn.microsoft.com/663743c9-16e9-4e3a-90b2-883ef0b8d5cf">How to Create a Radial Gradient Brush</a> topic and the <a href="https://msdn.microsoft.com/7a31d9e7-0521-40ee-b2c1-592dfaf5301e">Brushes Overview</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/7a31d9e7-0521-40ee-b2c1-592dfaf5301e">Brushes Overview</a>



<a href="https://msdn.microsoft.com/d65ee26c-28d4-4b58-9089-1aab959246cc">D2D1::RadialGradientBrushProperties</a>



<a href="https://msdn.microsoft.com/663743c9-16e9-4e3a-90b2-883ef0b8d5cf">How to Create a Radial Gradient Brush</a>



<a href="https://msdn.microsoft.com/21ed2286-e4df-4b77-ba31-e5d5927e16f5">ID2D1RadialGradientBrush</a>
 

 

