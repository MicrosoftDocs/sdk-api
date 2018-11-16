---
UID: NN:d2d1.ID2D1GeometrySink
title: ID2D1GeometrySink
author: windows-sdk-content
description: Describes a geometric path that can contain lines, arcs, cubic Bezier curves, and quadratic Bezier curves.
old-location: direct2d\ID2D1GeometrySink.htm
tech.root: Direct2D
ms.assetid: 6d2c1959-1309-45d8-8204-19ffea03375b
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ID2D1GeometrySink, ID2D1GeometrySink interface [Direct2D], ID2D1GeometrySink interface [Direct2D],described, d2d1/ID2D1GeometrySink, direct2d.ID2D1GeometrySink
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
 - ID2D1GeometrySink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1GeometrySink interface


## -description


Describes a geometric path that can contain lines, arcs, cubic Bezier curves, and quadratic Bezier curves.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1GeometrySink</b> interface inherits from <a href="https://msdn.microsoft.com/cf877a25-7b9f-4db0-ac53-b4a350795a86">ID2D1SimplifiedGeometrySink</a>. <b>ID2D1GeometrySink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1GeometrySink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/845fed36-8425-45fd-a12e-7537e5ba3c4f">AddArc</a>
</td>
<td align="left" width="63%">Overloaded. Creates a single arc and adds it to the path geometry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d1e228eb-dac6-485d-b3c9-69b2bd45e531">AddBezier</a>
</td>
<td align="left" width="63%">Overloaded. Creates  a cubic Bezier curve between the current point and the specified end point and adds it to the geometry sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ab11c38-784b-4834-bced-cd560a5273f6">AddLine</a>
</td>
<td align="left" width="63%">
Creates a line segment between the current point and the specified end point and adds it to the geometry sink. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/142f0823-0d8d-4216-8f40-9dec7f48032e">AddQuadraticBezier</a>
</td>
<td align="left" width="63%">Overloaded. Creates  a quadratic Bezier curve between the current point and the specified end point and adds it to the geometry sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3eb0921e-1d9c-48a0-a709-3ac7feed22c5">AddQuadraticBeziers</a>
</td>
<td align="left" width="63%">
Adds a sequence of quadratic Bezier segments as an array in a single call.

</td>
</tr>
</table> 


## -remarks



The <b>ID2D1GeometrySink</b> interface extends the <a href="https://msdn.microsoft.com/cf877a25-7b9f-4db0-ac53-b4a350795a86">ID2D1SimplifiedGeometrySink</a> interface to add support for arcs and quadratic beziers, as well as functions for adding single lines and cubic beziers.

A geometry sink consists of one or more figures. Each figure is made up of one or more line, curve, or arc segments. To create a figure, call the <a href="https://msdn.microsoft.com/87a932d4-1f90-4bdb-b131-0664566b0318">BeginFigure</a> method, specify the figure's start point, and then use its Add methods (such as AddLine and AddBezier) to add segments. When you are finished adding segments, call the <a href="https://msdn.microsoft.com/31f6aeba-2e81-4b8d-b734-0c501eae331f">EndFigure</a> method. You can repeat this sequence to create additional figures. When you are finished creating figures, call the <a href="https://msdn.microsoft.com/9dbbe5c6-d21c-4408-9208-53c7c051b22a">Close</a> method.


#### Examples

The following example creates an <a href="https://msdn.microsoft.com/d200563c-d78e-4fa0-a8f2-242b24480e99">ID2D1PathGeometry</a>, retrieves a sink, and uses it to define an hourglass shape. For the complete example, see <a href="https://msdn.microsoft.com/d7aad487-04e0-448d-bedf-b8dfadc7bbe9">How to Draw and Fill a Complex Shape</a>. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>ID2D1GeometrySink *pSink = NULL;

</pre>
</td>
</tr>
</table></span><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Create a path geometry.
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory-&gt;CreatePathGeometry(&amp;m_pPathGeometry);

    if (SUCCEEDED(hr))
    {
        // Write to the path geometry using the geometry sink.
        hr = m_pPathGeometry-&gt;Open(&amp;pSink);

        if (SUCCEEDED(hr))
        {
            pSink-&gt;BeginFigure(
                D2D1::Point2F(0, 0),
                D2D1_FIGURE_BEGIN_FILLED
                );

            pSink-&gt;AddLine(D2D1::Point2F(200, 0));

            pSink-&gt;AddBezier(
                D2D1::BezierSegment(
                    D2D1::Point2F(150, 50),
                    D2D1::Point2F(150, 150),
                    D2D1::Point2F(200, 200))
                );

            pSink-&gt;AddLine(D2D1::Point2F(0, 200));

            pSink-&gt;AddBezier(
                D2D1::BezierSegment(
                    D2D1::Point2F(50, 150),
                    D2D1::Point2F(50, 50),
                    D2D1::Point2F(0, 0))
                );

            pSink-&gt;EndFigure(D2D1_FIGURE_END_CLOSED);

            hr = pSink-&gt;Close();
        }
        SafeRelease(&amp;pSink);
    }
}
</pre>
</td>
</tr>
</table></span></div>
<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/f5870d4b-dd30-4034-884e-1c398a6865c6">Geometries Overview</a>



<a href="https://msdn.microsoft.com/d7aad487-04e0-448d-bedf-b8dfadc7bbe9">How to Draw and Fill a Complex Shape</a>



<a href="https://msdn.microsoft.com/cf877a25-7b9f-4db0-ac53-b4a350795a86">ID2D1SimplifiedGeometrySink</a>
 

 

