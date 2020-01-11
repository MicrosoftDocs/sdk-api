---
UID: NF:d2d1.ID2D1RenderTarget.CreateLayer(const D2D1_SIZE_F,ID2D1Layer)
title: ID2D1RenderTarget::CreateLayer (d2d1.h)
description: Creates a layer resource that can be used with this render target and its compatible render targets.
old-location: direct2d\id2d1rendertarget_createlayer.htm
tech.root: Direct2D
ms.assetid: 074e9ffb-c5f2-4e7b-94c7-d457bf07c0b7
ms.date: 12/05/2018
ms.keywords: CreateLayer, CreateLayer methods [Direct2D], ID2D1RenderTarget.CreateLayer, ID2D1RenderTarget::CreateLayer, d2d1/CreateLayer, direct2d.id2d1rendertarget_createlayer
f1_keywords:
- d2d1/ID2D1RenderTarget::CreateLayer
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- D2d1.dll
api_name:
- ID2D1RenderTarget::CreateLayer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1RenderTarget::CreateLayer


## -description


<span>Creates a layer resource that can be used with this render target and its compatible render targets. 
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)">CreateLayer(ID2D1Layer**)</a>
</td>
<td align="left" width="63%">
Creates a layer resource that can be used with this render target and its compatible render targets. 

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(d2d1_size_f_id2d1layer)">CreateLayer(D2D1_SIZE_F,ID2D1Layer**)</a>
</td>
<td align="left" width="63%">
Creates a layer resource that can be used with this render target and its compatible render targets. The new layer has the specified initial size. 

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(d2d1_size_f_id2d1layer)">CreateLayer(D2D1_SIZE_F*,ID2D1Layer**)</a>
</td>
<td align="left" width="63%">
Creates a layer resource that can be used with this render target and its compatible render targets. The new layer has the specified initial size. 

</td>
</tr>
</table>

## -parameters


## -remarks



The layer automatically resizes itself, as needed.  


#### Examples

The following example uses a layer to clip a bitmap to a geometric mask. For the complete example, see <a href="https://docs.microsoft.com/windows/desktop/Direct2D/how-to-clip-with-layers">How to Clip to a Geometric Mask</a>.


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




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>



<a href="https://docs.microsoft.com/windows/desktop/Direct2D/direct2d-layers-overview">Layers Overview</a>
 

 

