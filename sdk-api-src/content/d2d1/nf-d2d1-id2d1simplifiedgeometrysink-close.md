---
UID: NF:d2d1.ID2D1SimplifiedGeometrySink.Close
title: ID2D1SimplifiedGeometrySink::Close (d2d1.h)
description: Closes the geometry sink, indicates whether it is in an error state, and resets the sink's error state.
helpviewer_keywords: ["Close","Close method [Direct2D]","Close method [Direct2D]","ID2D1SimplifiedGeometrySink interface","ID2D1SimplifiedGeometrySink interface [Direct2D]","Close method","ID2D1SimplifiedGeometrySink.Close","ID2D1SimplifiedGeometrySink::Close","d2d1/ID2D1SimplifiedGeometrySink::Close","direct2d.ID2D1SimplifiedGeometrySink_Close"]
old-location: direct2d\ID2D1SimplifiedGeometrySink_Close.htm
tech.root: Direct2D
ms.assetid: 9dbbe5c6-d21c-4408-9208-53c7c051b22a
ms.date: 12/05/2018
ms.keywords: Close, Close method [Direct2D], Close method [Direct2D],ID2D1SimplifiedGeometrySink interface, ID2D1SimplifiedGeometrySink interface [Direct2D],Close method, ID2D1SimplifiedGeometrySink.Close, ID2D1SimplifiedGeometrySink::Close, d2d1/ID2D1SimplifiedGeometrySink::Close, direct2d.ID2D1SimplifiedGeometrySink_Close
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
 - ID2D1SimplifiedGeometrySink::Close
 - d2d1/ID2D1SimplifiedGeometrySink::Close
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
 - ID2D1SimplifiedGeometrySink.Close
---

# ID2D1SimplifiedGeometrySink::Close


## -description

Closes the geometry sink, indicates whether it is in an error state, and resets the sink's error state.



## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -remarks

Do not close the geometry sink while a figure is still in progress; doing so puts the geometry sink in an error state. For the close operation to be successful, there must be one <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure">EndFigure</a> call for each call to <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure">BeginFigure</a>.

After calling this method, the geometry sink might not be usable. Direct2D implementations of this interface do not allow the geometry sink to be modified after it is closed, but other implementations might not impose this restriction.


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

