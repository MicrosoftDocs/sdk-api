---
UID: NN:d2d1.ID2D1PathGeometry
title: ID2D1PathGeometry (d2d1.h)
description: Represents a complex shape that may be composed of arcs, curves, and lines.
old-location: direct2d\ID2D1PathGeometry.htm
tech.root: Direct2D
ms.assetid: d200563c-d78e-4fa0-a8f2-242b24480e99
ms.date: 12/05/2018
ms.keywords: ID2D1PathGeometry, ID2D1PathGeometry interface [Direct2D], ID2D1PathGeometry interface [Direct2D],described, d2d1/ID2D1PathGeometry, direct2d.ID2D1PathGeometry
ms.topic: interface
f1_keywords:
- d2d1/ID2D1PathGeometry
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D2d1.dll
api_name:
- ID2D1PathGeometry
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1PathGeometry interface


## -description


Represents a complex shape that may be composed of arcs, curves, and lines. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1PathGeometry</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1geometry">ID2D1Geometry</a>. <b>ID2D1PathGeometry</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1PathGeometry</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1pathgeometry-getfigurecount">GetFigureCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of figures in the path geometry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1pathgeometry-getsegmentcount">GetSegmentCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of segments in the path geometry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1pathgeometry-open">Open</a>
</td>
<td align="left" width="63%">
Retrieves the geometry sink that is used to populate the path geometry with figures and segments. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1pathgeometry-stream">Stream</a>
</td>
<td align="left" width="63%">
Copies the contents of the path geometry to the specified <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1geometrysink">ID2D1GeometrySink</a>.

</td>
</tr>
</table> 


## -remarks



An <b>ID2D1PathGeometry</b> object enables you to describe a geometric path. To describe an <b>ID2D1PathGeometry</b>  object's path, use the object's  <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1pathgeometry-open">Open</a> method to retrieve an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1geometrysink">ID2D1GeometrySink</a>. Use the sink to populate the path geometry with figures and segments. 

<h3><a id="Creating_ID2D1PathGeometry_Objects"></a><a id="creating_id2d1pathgeometry_objects"></a><a id="CREATING_ID2D1PATHGEOMETRY_OBJECTS"></a>Creating ID2D1PathGeometry Objects</h3>
To create a path geometry, use the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry">ID2D1Factory::CreatePathGeometry</a>  method.   

<b>ID2D1PathGeometry</b> objects are device-independent resources created by <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a>.  In general, you should create geometries once and retain them for the life of the application, or until they need to be modified. For more information about device-independent and device-dependent resources, see  the <a href="https://docs.microsoft.com/windows/desktop/Direct2D/resources-and-resource-domains">Resources Overview</a>. 


#### Examples

The following example creates an <b>ID2D1PathGeometry</b>, retrieves a sink, and uses it to define an hourglass shape. For the complete example, see <a href="https://docs.microsoft.com/windows/desktop/Direct2D/how-to-draw-and-fill-a-complex-shape">How to Draw and Fill a Complex Shape</a>.


```cpp
ID2D1GeometrySink *pSink = NULL;


```

```cpp
// Create a path geometry.
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometry);

    if (SUCCEEDED(hr))
    {
        // Write to the path geometry using the geometry sink.
        hr = m_pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            pSink->BeginFigure(
                D2D1::Point2F(0, 0),
                D2D1_FIGURE_BEGIN_FILLED
                );

            pSink->AddLine(D2D1::Point2F(200, 0));

            pSink->AddBezier(
                D2D1::BezierSegment(
                    D2D1::Point2F(150, 50),
                    D2D1::Point2F(150, 150),
                    D2D1::Point2F(200, 200))
                );

            pSink->AddLine(D2D1::Point2F(0, 200));

            pSink->AddBezier(
                D2D1::BezierSegment(
                    D2D1::Point2F(50, 150),
                    D2D1::Point2F(50, 50),
                    D2D1::Point2F(0, 0))
                );

            pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

            hr = pSink->Close();
        }
        SafeRelease(&pSink);
    }
}

```


<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Direct2D/geometries-how-to-topics">Geometries How-to Topics</a>



<a href="https://docs.microsoft.com/windows/desktop/Direct2D/direct2d-geometries-overview">Geometries Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry">ID2D1Factory::CreatePathGeometry</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1geometry">ID2D1Geometry</a>



<a href="https://docs.microsoft.com/windows/desktop/Direct2D/path-geometries-overview">Path Geometries Overview</a>
 

 

