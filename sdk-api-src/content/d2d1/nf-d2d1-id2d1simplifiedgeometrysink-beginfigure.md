---
UID: NF:d2d1.ID2D1SimplifiedGeometrySink.BeginFigure
title: ID2D1SimplifiedGeometrySink::BeginFigure
author: windows-sdk-content
description: Starts a new figure at the specified point.
old-location: direct2d\ID2D1SimplifiedGeometrySink_BeginFigure.htm
tech.root: direct2d
ms.assetid: 87a932d4-1f90-4bdb-b131-0664566b0318
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: BeginFigure, BeginFigure method [Direct2D], BeginFigure method [Direct2D],ID2D1SimplifiedGeometrySink interface, ID2D1SimplifiedGeometrySink interface [Direct2D],BeginFigure method, ID2D1SimplifiedGeometrySink.BeginFigure, ID2D1SimplifiedGeometrySink::BeginFigure, d2d1/ID2D1SimplifiedGeometrySink::BeginFigure, direct2d.ID2D1SimplifiedGeometrySink_BeginFigure
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ID2D1SimplifiedGeometrySink.BeginFigure
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d2d1.h
: 
- ID2D1SimplifiedGeometrySink.BeginFigure
: 
---

# ID2D1SimplifiedGeometrySink::BeginFigure


## -description


Starts a new figure at the specified point.


## -parameters




### -param startPoint

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The point at which to begin the new figure.


### -param figureBegin

Type: <b><a href="https://msdn.microsoft.com/c29aa79e-b978-4318-a8e1-5a321cd66327">D2D1_FIGURE_BEGIN</a></b>

Whether the new figure should be hollow or filled.


## -returns



This method does not return a value.




## -remarks



If this method is called while a figure is currently in progress, the interface is invalidated and all future methods will fail.


#### Examples

The following example creates an <a href="https://msdn.microsoft.com/d200563c-d78e-4fa0-a8f2-242b24480e99">ID2D1PathGeometry</a>, retrieves a sink, and uses it to define an hourglass shape. 

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



## -see-also




<a href="https://msdn.microsoft.com/cf877a25-7b9f-4db0-ac53-b4a350795a86">ID2D1SimplifiedGeometrySink</a>



<a href="https://msdn.microsoft.com/38a290be-b915-4317-b9b1-0e49e40dc8ec">Path Geometries Overview</a>
 

 

