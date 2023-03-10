---
UID: NF:d2d1.ID2D1RenderTarget.PopLayer
title: ID2D1RenderTarget::PopLayer (d2d1.h)
description: Stops redirecting drawing operations to the layer that is specified by the last PushLayer call.
helpviewer_keywords: ["ID2D1RenderTarget interface [Direct2D]","PopLayer method","ID2D1RenderTarget.PopLayer","ID2D1RenderTarget::PopLayer","PopLayer","PopLayer method [Direct2D]","PopLayer method [Direct2D]","ID2D1RenderTarget interface","d2d1/ID2D1RenderTarget::PopLayer","direct2d.ID2D1RenderTarget_PopLayer"]
old-location: direct2d\ID2D1RenderTarget_PopLayer.htm
tech.root: Direct2D
ms.assetid: 6ab05160-4f42-477f-a5bf-f16863b0635c
ms.date: 12/05/2018
ms.keywords: ID2D1RenderTarget interface [Direct2D],PopLayer method, ID2D1RenderTarget.PopLayer, ID2D1RenderTarget::PopLayer, PopLayer, PopLayer method [Direct2D], PopLayer method [Direct2D],ID2D1RenderTarget interface, d2d1/ID2D1RenderTarget::PopLayer, direct2d.ID2D1RenderTarget_PopLayer
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
 - ID2D1RenderTarget::PopLayer
 - d2d1/ID2D1RenderTarget::PopLayer
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
 - ID2D1RenderTarget.PopLayer
---

# ID2D1RenderTarget::PopLayer


## -description

Stops redirecting drawing operations to the layer that is specified by the last <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)">PushLayer</a> call.



## -remarks

A <b>PopLayer</b>  must match a previous <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)">PushLayer</a> call.

This method doesn't return an error code if it fails. To determine whether a drawing operation (such as <b>PopLayer</b>) failed, check the result returned by the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">ID2D1RenderTarget::EndDraw</a> or <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush">ID2D1RenderTarget::Flush</a> methods. 


## Examples

The following example uses a layer to clip a bitmap to a geometric mask. For the complete example, see <a href="/windows/win32/Direct2D/how-to-clip-with-layers">How to Clip to a Geometric Mask</a>.


```cpp
HRESULT DemoApp::RenderWithLayer(ID2D1RenderTarget *pRT)
{
    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(350, 50));

        // Push the layer with the geometric mask.
        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::InfiniteRect(), m_pPathGeometry),
            pLayer
            );
            
  
        pRT->DrawBitmap(m_pOrigBitmap, D2D1::RectF(0, 0, 200, 133));
        pRT->FillRectangle(D2D1::RectF(0.f, 0.f, 25.f, 25.f), m_pSolidColorBrush);  
        pRT->FillRectangle(D2D1::RectF(25.f, 25.f, 50.f, 50.f), m_pSolidColorBrush);
        pRT->FillRectangle(D2D1::RectF(50.f, 50.f, 75.f, 75.f), m_pSolidColorBrush); 
        pRT->FillRectangle(D2D1::RectF(75.f, 75.f, 100.f, 100.f), m_pSolidColorBrush);    
        pRT->FillRectangle(D2D1::RectF(100.f, 100.f, 125.f, 125.f), m_pSolidColorBrush); 
        pRT->FillRectangle(D2D1::RectF(125.f, 125.f, 150.f, 150.f), m_pSolidColorBrush);    
        

        pRT->PopLayer();
    }

    SafeRelease(&pLayer);

    return hr;
}

```

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>



<a href="/windows/win32/Direct2D/direct2d-layers-overview">Layers Overview</a>



<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)">PushLayer</a>

