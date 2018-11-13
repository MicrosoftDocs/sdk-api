---
UID: NF:d2d1.ID2D1SimplifiedGeometrySink.EndFigure
title: ID2D1SimplifiedGeometrySink::EndFigure
author: windows-sdk-content
description: Ends the current figure; optionally, closes it.
old-location: direct2d\ID2D1SimplifiedGeometrySink_EndFigure.htm
tech.root: direct2d
ms.assetid: 31f6aeba-2e81-4b8d-b734-0c501eae331f
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: EndFigure, EndFigure method [Direct2D], EndFigure method [Direct2D],ID2D1SimplifiedGeometrySink interface, ID2D1SimplifiedGeometrySink interface [Direct2D],EndFigure method, ID2D1SimplifiedGeometrySink.EndFigure, ID2D1SimplifiedGeometrySink::EndFigure, d2d1/ID2D1SimplifiedGeometrySink::EndFigure, direct2d.ID2D1SimplifiedGeometrySink_EndFigure
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
 - ID2D1SimplifiedGeometrySink.EndFigure
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1SimplifiedGeometrySink::EndFigure


## -description


Ends the current figure; optionally, closes it.


## -parameters




### -param figureEnd

Type: <b><a href="https://msdn.microsoft.com/44821eef-7ecf-44c1-bbfb-df259c0489dd">D2D1_FIGURE_END</a></b>

A value that indicates whether the current figure is closed. If the figure is closed, a line is drawn between the current point and the start point specified by <a href="https://msdn.microsoft.com/87a932d4-1f90-4bdb-b131-0664566b0318">BeginFigure</a>.


## -returns



This method does not return a value.




## -remarks



Calling this method without a matching call to <a href="https://msdn.microsoft.com/87a932d4-1f90-4bdb-b131-0664566b0318">BeginFigure</a>  places the geometry sink in an error state; subsequent calls are ignored, and the overall failure will be returned when the <a href="https://msdn.microsoft.com/9dbbe5c6-d21c-4408-9208-53c7c051b22a">Close</a> method is called.


#### Examples

The following example creates an <a href="https://msdn.microsoft.com/d200563c-d78e-4fa0-a8f2-242b24480e99">ID2D1PathGeometry</a>, retrieves a sink, uses it to define an hourglass shape, and then calls <b>EndFigure</b> with the D2D1_FIGURE_END_CLOSED value to end the creation of the hourglass. For the complete example, see <a href="https://msdn.microsoft.com/d7aad487-04e0-448d-bedf-b8dfadc7bbe9">How to Draw and Fill a Complex Shape</a>.

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




<a href="https://msdn.microsoft.com/cf877a25-7b9f-4db0-ac53-b4a350795a86">ID2D1SimplifiedGeometrySink</a>
 

 

