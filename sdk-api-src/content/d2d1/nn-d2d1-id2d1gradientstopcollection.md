---
UID: NN:d2d1.ID2D1GradientStopCollection
title: ID2D1GradientStopCollection (d2d1.h)
description: Represents a collection of D2D1_GRADIENT_STOP objects for linear and radial gradient brushes.
helpviewer_keywords: ["ID2D1GradientStopCollection","ID2D1GradientStopCollection interface [Direct2D]","ID2D1GradientStopCollection interface [Direct2D]","described","d2d1/ID2D1GradientStopCollection","direct2d.ID2D1GradientStopCollection"]
old-location: direct2d\ID2D1GradientStopCollection.htm
tech.root: Direct2D
ms.assetid: 982abf9c-4778-4871-a494-5843f0c0addc
ms.date: 12/05/2018
ms.keywords: ID2D1GradientStopCollection, ID2D1GradientStopCollection interface [Direct2D], ID2D1GradientStopCollection interface [Direct2D],described, d2d1/ID2D1GradientStopCollection, direct2d.ID2D1GradientStopCollection
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
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1GradientStopCollection
 - d2d1/ID2D1GradientStopCollection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1GradientStopCollection
---

# ID2D1GradientStopCollection interface


## -description

Represents a collection of <a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop">D2D1_GRADIENT_STOP</a> objects for linear and radial gradient brushes.

## -inheritance

The <b>ID2D1GradientStopCollection</b> interface inherits from <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1resource">ID2D1Resource</a>. <b>ID2D1GradientStopCollection</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

<h3><a id="Creating_ID2D1GradientStopCollection_Objects"></a><a id="creating_id2d1gradientstopcollection_objects"></a><a id="CREATING_ID2D1GRADIENTSTOPCOLLECTION_OBJECTS"></a>Creating ID2D1GradientStopCollection Objects</h3>
To create an <b>ID2D1GradientStopCollection</b>, use the  <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)">ID2D1RenderTarget::CreateGradientStopCollection</a> method.  

A gradient stop collection is a device-dependent resource: your application should create gradient stop collections after it initializes the render target with which the gradient stop collection will be used, and recreate the gradient stop collection whenever the render target needs recreated. (For more information about resources, see <a href="/windows/win32/Direct2D/resources-and-resource-domains">Resources Overview</a>.)


## Examples

The following example creates an array of gradient stops, then uses them to create an <b>ID2D1GradientStopCollection</b>.


```cpp
// Create an array of gradient stops to put in the gradient stop
// collection that will be used in the gradient brush.
ID2D1GradientStopCollection *pGradientStops = NULL;

D2D1_GRADIENT_STOP gradientStops[2];
gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
gradientStops[0].position = 0.0f;
gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
gradientStops[1].position = 1.0f;
// Create the ID2D1GradientStopCollection from a previously
// declared array of D2D1_GRADIENT_STOP structs.
hr = m_pRenderTarget->CreateGradientStopCollection(
    gradientStops,
    2,
    D2D1_GAMMA_2_2,
    D2D1_EXTEND_MODE_CLAMP,
    &pGradientStops
    );

```


The next code example uses the <b>ID2D1GradientStopCollection</b> to create an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush">ID2D1LinearGradientBrush</a>.


```cpp
// The line that determines the direction of the gradient starts at
// the upper-left corner of the square and ends at the lower-right corner.

if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateLinearGradientBrush(
        D2D1::LinearGradientBrushProperties(
            D2D1::Point2F(0, 0),
            D2D1::Point2F(150, 150)),
        pGradientStops,
        &m_pLinearGradientBrush
        );
}

```

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1resource">ID2D1Resource</a>

