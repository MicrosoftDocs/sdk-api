---
UID: NF:d2d1.ID2D1PathGeometry.Open
title: ID2D1PathGeometry::Open
author: windows-sdk-content
description: Retrieves the geometry sink that is used to populate the path geometry with figures and segments.
old-location: direct2d\ID2D1PathGeometry_Open.htm
tech.root: direct2d
ms.assetid: 08ff9ffb-1f1e-440c-a22c-dc58865b678a
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: ID2D1PathGeometry interface [Direct2D],Open method, ID2D1PathGeometry.Open, ID2D1PathGeometry::Open, Open, Open method [Direct2D], Open method [Direct2D],ID2D1PathGeometry interface, d2d1/ID2D1PathGeometry::Open, direct2d.ID2D1PathGeometry_Open
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
 - ID2D1PathGeometry.Open
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1PathGeometry::Open


## -description


Retrieves the geometry sink that is used to populate the path geometry with figures and segments. 


## -parameters




### -param geometrySink [out]

Type: <b><a href="https://msdn.microsoft.com/6d2c1959-1309-45d8-8204-19ffea03375b">ID2D1GeometrySink</a>**</b>

When this method returns, <i>geometrySink</i> contains the address of a pointer to the geometry sink that is used to populate the path geometry with figures and segments. This parameter is passed uninitialized.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Because path geometries are immutable and can only be populated once, it is an error to call <b>Open</b> on a path geometry more than once.

Note that the fill mode defaults to <a href="https://msdn.microsoft.com/f1a14447-39fa-4a48-9516-ff5b03abc3a6">D2D1_FILL_MODE_ALTERNATE</a>. To set the fill mode, call <a href="https://msdn.microsoft.com/f60f48bb-989e-46a5-b77f-65da0b91a599">SetFillMode</a> before the first call to <a href="https://msdn.microsoft.com/87a932d4-1f90-4bdb-b131-0664566b0318">BeginFigure</a>. Failure to do so will put the geometry sink in an error state. 


#### Examples

The following example creates an <a href="https://msdn.microsoft.com/d200563c-d78e-4fa0-a8f2-242b24480e99">ID2D1PathGeometry</a>, retrieves a sink, and uses the sink  to define an hourglass shape. For the complete example, see <a href="https://msdn.microsoft.com/d7aad487-04e0-448d-bedf-b8dfadc7bbe9">How to Draw and Fill a Complex Shape</a>.

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




<a href="https://msdn.microsoft.com/d200563c-d78e-4fa0-a8f2-242b24480e99">ID2D1PathGeometry</a>
 

 

