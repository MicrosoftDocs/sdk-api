---
UID: NN:d2d1.ID2D1GradientStopCollection
title: ID2D1GradientStopCollection
author: windows-sdk-content
description: Represents an collection of D2D1_GRADIENT_STOP objects for linear and radial gradient brushes.
old-location: direct2d\ID2D1GradientStopCollection.htm
old-project: direct2d
ms.assetid: 982abf9c-4778-4871-a494-5843f0c0addc
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ID2D1GradientStopCollection, ID2D1GradientStopCollection interface [Direct2D], ID2D1GradientStopCollection interface [Direct2D],described, d2d1/ID2D1GradientStopCollection, direct2d.ID2D1GradientStopCollection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d2d1.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D2D1_WINDOW_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1GradientStopCollection
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# ID2D1GradientStopCollection interface


## -description


Represents an collection of <a href="https://msdn.microsoft.com/f6798542-382a-4074-bbe1-707bc00b3575">D2D1_GRADIENT_STOP</a> objects for linear and radial gradient brushes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1GradientStopCollection</b> interface inherits from <a href="https://msdn.microsoft.com/8f19e74a-f010-4082-a4da-d1dc3cfe3192">ID2D1Resource</a>. <b>ID2D1GradientStopCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1GradientStopCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d07f4dcc-7656-44ca-87cc-d59cb62eb36a">GetColorInterpolationGamma</a>
</td>
<td align="left" width="63%">
Indicates the gamma space in which the gradient stops are interpolated. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f20f5aed-db5d-4605-b5d4-58a0255822b1">GetExtendMode</a>
</td>
<td align="left" width="63%">
Indicates the behavior of the gradient outside the normalized gradient range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c3ef4b0-e781-4177-81a4-b39add8468a0">GetGradientStopCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of gradient stops in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5ae1b14-2694-4593-8eba-17d93b45bb9c">GetGradientStops</a>
</td>
<td align="left" width="63%">
Copies the gradient stops from the collection into an array of <a href="https://msdn.microsoft.com/f6798542-382a-4074-bbe1-707bc00b3575">D2D1_GRADIENT_STOP</a> structures.

</td>
</tr>
</table> 


## -remarks



<h3><a id="Creating_ID2D1GradientStopCollection_Objects"></a><a id="creating_id2d1gradientstopcollection_objects"></a><a id="CREATING_ID2D1GRADIENTSTOPCOLLECTION_OBJECTS"></a>Creating ID2D1GradientStopCollection Objects</h3>
To create an <b>ID2D1GradientStopCollection</b>, use the  <a href="https://msdn.microsoft.com/674ffba5-18c5-46bf-8813-d8d13e5ba903">ID2D1RenderTarget::CreateGradientStopCollection</a> method.  

A gradient stop collection is a device-dependent resource: your application should create gradient stop collections after it initializes the render target with which the gradient stop collection will be used, and recreate the gradient stop collection whenever the render target needs recreated. (For more information about resources, see <a href="https://msdn.microsoft.com/afd308a7-9524-4436-9a0e-8575383d96fa">Resources Overview</a>.)


#### Examples

The following example creates an array of gradient stops, then uses them to create an <b>ID2D1GradientStopCollection</b>.

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
The next code example uses the <b>ID2D1GradientStopCollection</b> to create an <a href="https://msdn.microsoft.com/bbb5e36a-d13d-448e-8686-d14ee99b1ccb">ID2D1LinearGradientBrush</a>.

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




<a href="https://msdn.microsoft.com/8f19e74a-f010-4082-a4da-d1dc3cfe3192">ID2D1Resource</a>
 

 

