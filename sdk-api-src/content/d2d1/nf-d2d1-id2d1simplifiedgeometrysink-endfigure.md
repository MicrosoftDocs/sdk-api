---
UID: NF:d2d1.ID2D1SimplifiedGeometrySink.EndFigure
title: ID2D1SimplifiedGeometrySink::EndFigure (d2d1.h)
description: Ends the current figure; optionally, closes it.
helpviewer_keywords: ["EndFigure","EndFigure method [Direct2D]","EndFigure method [Direct2D]","ID2D1SimplifiedGeometrySink interface","ID2D1SimplifiedGeometrySink interface [Direct2D]","EndFigure method","ID2D1SimplifiedGeometrySink.EndFigure","ID2D1SimplifiedGeometrySink::EndFigure","d2d1/ID2D1SimplifiedGeometrySink::EndFigure","direct2d.ID2D1SimplifiedGeometrySink_EndFigure"]
old-location: direct2d\ID2D1SimplifiedGeometrySink_EndFigure.htm
tech.root: Direct2D
ms.assetid: 31f6aeba-2e81-4b8d-b734-0c501eae331f
ms.date: 12/05/2018
ms.keywords: EndFigure, EndFigure method [Direct2D], EndFigure method [Direct2D],ID2D1SimplifiedGeometrySink interface, ID2D1SimplifiedGeometrySink interface [Direct2D],EndFigure method, ID2D1SimplifiedGeometrySink.EndFigure, ID2D1SimplifiedGeometrySink::EndFigure, d2d1/ID2D1SimplifiedGeometrySink::EndFigure, direct2d.ID2D1SimplifiedGeometrySink_EndFigure
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
 - ID2D1SimplifiedGeometrySink::EndFigure
 - d2d1/ID2D1SimplifiedGeometrySink::EndFigure
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
 - ID2D1SimplifiedGeometrySink.EndFigure
---

# ID2D1SimplifiedGeometrySink::EndFigure


## -description

Ends the current figure; optionally, closes it.

## -parameters

### -param figureEnd

Type: <b><a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_figure_end">D2D1_FIGURE_END</a></b>

A value that indicates whether the current figure is closed. If the figure is closed, a line is drawn between the current point and the start point specified by <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure">BeginFigure</a>.

## -remarks

Calling this method without a matching call to <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure">BeginFigure</a>  places the geometry sink in an error state; subsequent calls are ignored, and the overall failure will be returned when the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close">Close</a> method is called.


## Examples

The following example creates an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry">ID2D1PathGeometry</a>, retrieves a sink, uses it to define an hourglass shape, and then calls <b>EndFigure</b> with the D2D1_FIGURE_END_CLOSED value to end the creation of the hourglass. For the complete example, see <a href="/windows/win32/Direct2D/how-to-draw-and-fill-a-complex-shape">How to Draw and Fill a Complex Shape</a>.


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

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink">ID2D1SimplifiedGeometrySink</a>

