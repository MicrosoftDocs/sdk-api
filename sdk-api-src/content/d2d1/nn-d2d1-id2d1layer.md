---
UID: NN:d2d1.ID2D1Layer
title: ID2D1Layer (d2d1.h)
description: Represents the backing store required to render a layer.
helpviewer_keywords: ["ID2D1Layer","ID2D1Layer interface [Direct2D]","ID2D1Layer interface [Direct2D]","described","d2d1/ID2D1Layer","direct2d.ID2D1Layer"]
old-location: direct2d\ID2D1Layer.htm
tech.root: Direct2D
ms.assetid: ce7b2345-f0e5-4e44-9146-b1f140bb00ca
ms.date: 12/05/2018
ms.keywords: ID2D1Layer, ID2D1Layer interface [Direct2D], ID2D1Layer interface [Direct2D],described, d2d1/ID2D1Layer, direct2d.ID2D1Layer
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
 - ID2D1Layer
 - d2d1/ID2D1Layer
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
 - ID2D1Layer
---

# ID2D1Layer interface


## -description

Represents the backing store required to render a layer.

## -inheritance

The <b>ID2D1Layer</b> interface inherits from <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1resource">ID2D1Resource</a>. <b>ID2D1Layer</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To create a layer, call the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(d2d1_size_f_id2d1layer)">CreateLayer</a> method of the render target where the layer will be used. To draw to a layer, push the layer to the render target stack by calling the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)">PushLayer</a> method. After you have finished drawing to the layer, call the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer">PopLayer</a> method.

Between  <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)">PushLayer</a> and <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer">PopLayer</a> calls, the layer is in use and cannot be used by another render target. 

If the size of the layer is not specified, the corresponding <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)">PushLayer</a> call determines the minimum layer size, based on the layer content bounds and the geometric mask. The layer resource can be larger than the size required by <b>PushLayer</b> without any rendering artifacts.

If the size of a layer is specified, or if the layer has been used and the required backing store size as calculated during <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)">PushLayer</a> is larger than the layer, then the layer resource is expanded on each axis monotonically to ensure that it is large enough. The layer resource never shrinks in size.

<h3><a id="Creating_ID2D1Layer_Objects"></a><a id="creating_id2d1layer_objects"></a><a id="CREATING_ID2D1LAYER_OBJECTS"></a>Creating ID2D1Layer Objects</h3>
To create a layer, call the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(d2d1_size_f_id2d1layer)">CreateLayer</a> method of the render target where the layer will be used.

A layer is a device-dependent resource: your application should create layers after it initializes the render target with which the layers will be used, and recreate the layers whenever the render target needs recreated. (For more information about resources, see <a href="/windows/win32/Direct2D/resources-and-resource-domains">Resources Overview</a>.)


## Examples

The following example uses a layer to clip a drawing to a geometric mask. For the complete example, see <a href="/windows/win32/Direct2D/how-to-clip-with-layers">How to Clip to a Geometric Mask</a>.


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



<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1resource">ID2D1Resource</a>



<a href="/windows/win32/Direct2D/direct2d-layers-overview">Layers Overview</a>

