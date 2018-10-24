---
UID: NS:d2d1.D2D1_GRADIENT_STOP
title: D2D1_GRADIENT_STOP
author: windows-sdk-content
description: Contains the position and color of a gradient stop.
old-location: direct2d\D2D1_GRADIENT_STOP.htm
tech.root: Direct2D
ms.assetid: f6798542-382a-4074-bbe1-707bc00b3575
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: D2D1_GRADIENT_STOP, D2D1_GRADIENT_STOP structure [Direct2D], d2d1/D2D1_GRADIENT_STOP, direct2d.D2D1_GRADIENT_STOP
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_GRADIENT_STOP
product: Windows
targetos: Windows
req.typenames: D2D1_GRADIENT_STOP
req.redist: 
---

# D2D1_GRADIENT_STOP structure


## -description


Contains the position and color of a gradient stop. 


## -struct-fields




### -field position

Type: <b>FLOAT</b>

A value that indicates the relative position of the gradient stop in the brush. This value must be in the [0.0f, 1.0f] range if the gradient stop is to be seen explicitly. 


### -field color

Type: <b><a href="https://msdn.microsoft.com/564d4f41-2da7-49ed-b85a-d1070d662b40">D2D1_COLOR_F</a></b>

The color of the gradient stop.


## -remarks



Gradient stops can be specified in any order if they are at different positions. Two stops may share a position. In this case, the first stop specified is treated as the "low" stop (nearer 0.0f) and subsequent stops are treated as "higher" (nearer 1.0f). This behavior is useful if a caller wants an instant transition in the middle of a stop.

Typically, there are at least two points in a collection, although creation with only one stop is permitted. For example, one point is at position 0.0f, another point is at position 1.0f, and additional points are distributed in the [0, 1] range. Where the gradient progression is beyond the range of [0, 1], the stops are stored, but may affect the gradient. 

When drawn, the [0, 1] range of positions is mapped to the brush, in a brush-dependent way. For details, see <a href="https://msdn.microsoft.com/bbb5e36a-d13d-448e-8686-d14ee99b1ccb">ID2D1LinearGradientBrush</a> and <a href="https://msdn.microsoft.com/21ed2286-e4df-4b77-ba31-e5d5927e16f5">ID2D1RadialGradientBrush</a>. 

Gradient stops with a position outside the [0, 1] range cannot be seen explicitly, but they can still affect the colors produced in the [0, 1] range. For example, a two-stop gradient {{0.0f, Black}, {2.0f, White}} is indistinguishable visually from {{0.0f, Black}, {1.0f, Mid-level gray}}. Also, the colors are clamped before interpolation.


#### Examples

The following example creates an array of gradient stops, then uses them to create 
        an <a href="https://msdn.microsoft.com/982abf9c-4778-4871-a494-5843f0c0addc">ID2D1GradientStopCollection</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Create an array of gradient stops to put in the gradient stop
// collection that will be used in the gradient brush.
ID2D1GradientStopCollection *pGradientStops = NULL;

D2D1_GRADIENT_STOP gradientStops[2];
gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
gradientStops[0].position = 0.0f;
gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
gradientStops[1].position = 1.0f;
// Create the ID2D1GradientStopCollection from a previously
// declared array of D2D1_GRADIENT_STOP structs.
hr = m_pRenderTarget-&gt;CreateGradientStopCollection(
    gradientStops,
    2,
    D2D1_GAMMA_2_2,
    D2D1_EXTEND_MODE_CLAMP,
    &amp;pGradientStops
    );
</pre>
</td>
</tr>
</table></span></div>
The next code example uses the <a href="https://msdn.microsoft.com/982abf9c-4778-4871-a494-5843f0c0addc">ID2D1GradientStopCollection</a> to 
        create an <a href="https://msdn.microsoft.com/bbb5e36a-d13d-448e-8686-d14ee99b1ccb">ID2D1LinearGradientBrush</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// The line that determines the direction of the gradient starts at
// the upper-left corner of the square and ends at the lower-right corner.

if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget-&gt;CreateLinearGradientBrush(
        D2D1::LinearGradientBrushProperties(
            D2D1::Point2F(0, 0),
            D2D1::Point2F(150, 150)),
        pGradientStops,
        &amp;m_pLinearGradientBrush
        );
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7a31d9e7-0521-40ee-b2c1-592dfaf5301e">Brushes Overview</a>



<a href="https://msdn.microsoft.com/674ffba5-18c5-46bf-8813-d8d13e5ba903">CreateGradientStopCollection</a>



<a href="https://msdn.microsoft.com/3cf5acc6-2f17-49d4-aca5-a84a846d1749">How to Create a Linear Gradient Brush</a>



<a href="https://msdn.microsoft.com/663743c9-16e9-4e3a-90b2-883ef0b8d5cf">How to Create a Radial Gradient Brush</a>



<a href="https://msdn.microsoft.com/982abf9c-4778-4871-a494-5843f0c0addc">ID2D1GradientStopCollection</a>



<a href="https://msdn.microsoft.com/bbb5e36a-d13d-448e-8686-d14ee99b1ccb">ID2D1LinearGradientBrush</a>



<a href="https://msdn.microsoft.com/21ed2286-e4df-4b77-ba31-e5d5927e16f5">ID2D1RadialGradientBrush</a>
 

 

