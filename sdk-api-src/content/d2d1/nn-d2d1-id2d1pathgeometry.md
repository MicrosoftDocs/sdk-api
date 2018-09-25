---
UID: NN:d2d1.ID2D1PathGeometry
title: ID2D1PathGeometry
author: windows-sdk-content
description: Represents a complex shape that may be composed of arcs, curves, and lines.
old-location: direct2d\ID2D1PathGeometry.htm
tech.root: direct2d
ms.assetid: d200563c-d78e-4fa0-a8f2-242b24480e99
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: ID2D1PathGeometry, ID2D1PathGeometry interface [Direct2D], ID2D1PathGeometry interface [Direct2D],described, d2d1/ID2D1PathGeometry, direct2d.ID2D1PathGeometry
ms.prod: windows
ms.technology: windows-sdk
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
 - ID2D1PathGeometry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1PathGeometry interface


## -description


Represents a complex shape that may be composed of arcs, curves, and lines. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1PathGeometry</b> interface inherits from <a href="https://msdn.microsoft.com/be4ab801-64f6-48f9-8f62-d0492cc438b1">ID2D1Geometry</a>. <b>ID2D1PathGeometry</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/f46d28f6-5f46-45eb-85c9-6d3b21fa2cff">GetFigureCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of figures in the path geometry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/53a80fec-5851-4b62-aa9b-fb7f8b15b0e7">GetSegmentCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of segments in the path geometry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/08ff9ffb-1f1e-440c-a22c-dc58865b678a">Open</a>
</td>
<td align="left" width="63%">
Retrieves the geometry sink that is used to populate the path geometry with figures and segments. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e128b4e7-8fde-44f1-a7a3-928aace0fe7f">Stream</a>
</td>
<td align="left" width="63%">
Copies the contents of the path geometry to the specified <a href="https://msdn.microsoft.com/6d2c1959-1309-45d8-8204-19ffea03375b">ID2D1GeometrySink</a>.

</td>
</tr>
</table> 


## -remarks



An <b>ID2D1PathGeometry</b> object enables you to describe a geometric path. To describe an <b>ID2D1PathGeometry</b>  object's path, use the object's  <a href="https://msdn.microsoft.com/08ff9ffb-1f1e-440c-a22c-dc58865b678a">Open</a> method to retrieve an <a href="https://msdn.microsoft.com/6d2c1959-1309-45d8-8204-19ffea03375b">ID2D1GeometrySink</a>. Use the sink to populate the path geometry with figures and segments. 

<h3><a id="Creating_ID2D1PathGeometry_Objects"></a><a id="creating_id2d1pathgeometry_objects"></a><a id="CREATING_ID2D1PATHGEOMETRY_OBJECTS"></a>Creating ID2D1PathGeometry Objects</h3>
To create a path geometry, use the <a href="https://msdn.microsoft.com/35c46055-3df2-44d5-b11d-520ab2fa4a0e">ID2D1Factory::CreatePathGeometry</a>  method.   

<b>ID2D1PathGeometry</b> objects are device-independent resources created by <a href="https://msdn.microsoft.com/cef6115c-98e8-49e6-b419-271b43ce2938">ID2D1Factory</a>.  In general, you should create geometries once and retain them for the life of the application, or until they need to be modified. For more information about device-independent and device-dependent resources, see  the <a href="https://msdn.microsoft.com/afd308a7-9524-4436-9a0e-8575383d96fa">Resources Overview</a>. 


#### Examples

The following example creates an <b>ID2D1PathGeometry</b>, retrieves a sink, and uses it to define an hourglass shape. For the complete example, see <a href="https://msdn.microsoft.com/d7aad487-04e0-448d-bedf-b8dfadc7bbe9">How to Draw and Fill a Complex Shape</a>.

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




<a href="https://msdn.microsoft.com/371a6662-f68f-418a-a81d-239de56877f1">Geometries How-to Topics</a>



<a href="https://msdn.microsoft.com/f5870d4b-dd30-4034-884e-1c398a6865c6">Geometries Overview</a>



<a href="https://msdn.microsoft.com/35c46055-3df2-44d5-b11d-520ab2fa4a0e">ID2D1Factory::CreatePathGeometry</a>



<a href="https://msdn.microsoft.com/be4ab801-64f6-48f9-8f62-d0492cc438b1">ID2D1Geometry</a>



<a href="https://msdn.microsoft.com/38a290be-b915-4317-b9b1-0e49e40dc8ec">Path Geometries Overview</a>
 

 

