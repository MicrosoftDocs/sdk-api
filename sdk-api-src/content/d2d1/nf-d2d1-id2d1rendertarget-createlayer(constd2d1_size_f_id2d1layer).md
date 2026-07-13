---
UID: NF:d2d1.ID2D1RenderTarget.CreateLayer(constD2D1_SIZE_F,ID2D1Layer)
title: ID2D1RenderTarget::CreateLayer (d2d1.h)
description: Creates a layer resource that can be used with this render target and its compatible render targets. (overload 2/2)
helpviewer_keywords: ["CreateLayer","CreateLayer methods [Direct2D]","ID2D1RenderTarget.CreateLayer","ID2D1RenderTarget::CreateLayer","d2d1/CreateLayer","direct2d.id2d1rendertarget_createlayer"]
old-location: direct2d\id2d1rendertarget_createlayer.htm
tech.root: Direct2D
ms.assetid: 074e9ffb-c5f2-4e7b-94c7-d457bf07c0b7
ms.date: 12/05/2018
ms.keywords: CreateLayer, CreateLayer methods [Direct2D], ID2D1RenderTarget.CreateLayer, ID2D1RenderTarget::CreateLayer, d2d1/CreateLayer, direct2d.id2d1rendertarget_createlayer
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - ID2D1RenderTarget::CreateLayer
 - d2d1/ID2D1RenderTarget::CreateLayer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - ID2D1RenderTarget::CreateLayer
---

## -description

Creates a layer resource that can be used with this render target and its compatible render targets.

## -parameters

### -param size

Type: [in] <b>const <a href="/windows/win32/Direct2D/d2d1-size-f">D2D1_SIZE_F</a>*</b>

If (0, 0) is specified, no backing store is created behind the layer resource. The layer resource is allocated to the minimum size when <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)">PushLayer</a> is called.

### -param layer

Type: [out] <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1layer">ID2D1Layer</a>**</b>

When the method returns, contains a pointer to a pointer to the new layer. This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -remarks

The layer automatically resizes itself, as needed.

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

