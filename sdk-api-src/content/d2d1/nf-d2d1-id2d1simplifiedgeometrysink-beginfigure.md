---
UID: NF:d2d1.ID2D1SimplifiedGeometrySink.BeginFigure
title: ID2D1SimplifiedGeometrySink::BeginFigure (d2d1.h)
description: Starts a new figure at the specified point.
helpviewer_keywords: ["BeginFigure","BeginFigure method [Direct2D]","BeginFigure method [Direct2D]","ID2D1SimplifiedGeometrySink interface","ID2D1SimplifiedGeometrySink interface [Direct2D]","BeginFigure method","ID2D1SimplifiedGeometrySink.BeginFigure","ID2D1SimplifiedGeometrySink::BeginFigure","d2d1/ID2D1SimplifiedGeometrySink::BeginFigure","direct2d.ID2D1SimplifiedGeometrySink_BeginFigure"]
old-location: direct2d\ID2D1SimplifiedGeometrySink_BeginFigure.htm
tech.root: Direct2D
ms.assetid: 87a932d4-1f90-4bdb-b131-0664566b0318
ms.date: 12/05/2018
ms.keywords: BeginFigure, BeginFigure method [Direct2D], BeginFigure method [Direct2D],ID2D1SimplifiedGeometrySink interface, ID2D1SimplifiedGeometrySink interface [Direct2D],BeginFigure method, ID2D1SimplifiedGeometrySink.BeginFigure, ID2D1SimplifiedGeometrySink::BeginFigure, d2d1/ID2D1SimplifiedGeometrySink::BeginFigure, direct2d.ID2D1SimplifiedGeometrySink_BeginFigure
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
 - ID2D1SimplifiedGeometrySink::BeginFigure
 - d2d1/ID2D1SimplifiedGeometrySink::BeginFigure
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
 - ID2D1SimplifiedGeometrySink.BeginFigure
---

# ID2D1SimplifiedGeometrySink::BeginFigure


## -description

Starts a new figure at the specified point.

## -parameters

### -param startPoint

Type: <b><a href="/windows/win32/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

The point at which to begin the new figure.

### -param figureBegin

Type: <b><a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_figure_begin">D2D1_FIGURE_BEGIN</a></b>

Whether the new figure should be hollow or filled.

## -remarks

If this method is called while a figure is currently in progress, the interface is invalidated and all future methods will fail.


## Examples

The following example creates an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry">ID2D1PathGeometry</a>, retrieves a sink, and uses it to define an hourglass shape. 


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

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink">ID2D1SimplifiedGeometrySink</a>



<a href="/windows/win32/Direct2D/path-geometries-overview">Path Geometries Overview</a>

