---
UID: NF:d2d1.ID2D1RenderTarget.CreateLayer(const D2D1_SIZE_F,ID2D1Layer)
title: ID2D1RenderTarget::CreateLayer(const D2D1_SIZE_F,ID2D1Layer)
author: windows-sdk-content
description: Creates a layer resource that can be used with this render target and its compatible render targets.
old-location: direct2d\id2d1rendertarget_createlayer.htm
tech.root: Direct2D
ms.assetid: 074e9ffb-c5f2-4e7b-94c7-d457bf07c0b7
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: CreateLayer, CreateLayer methods [Direct2D], ID2D1RenderTarget.CreateLayer, ID2D1RenderTarget.CreateLayer(const D2D1_SIZE_F,ID2D1Layer), ID2D1RenderTarget::CreateLayer, ID2D1RenderTarget::CreateLayer(const D2D1_SIZE_F,ID2D1Layer), d2d1/CreateLayer, direct2d.id2d1rendertarget_createlayer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget::CreateLayer(const D2D1_SIZE_F,ID2D1Layer)


## -description


<span>Creates a layer resource that can be used with this render target and its compatible render targets. 
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a3377fb-f847-454f-9716-70a7b65fe96c">CreateLayer(ID2D1Layer**)</a>
</td>
<td align="left" width="63%">
Creates a layer resource that can be used with this render target and its compatible render targets. 

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c21596a3-2b10-4a96-9a01-cf9325e51fe3">CreateLayer(D2D1_SIZE_F,ID2D1Layer**)</a>
</td>
<td align="left" width="63%">
Creates a layer resource that can be used with this render target and its compatible render targets. The new layer has the specified initial size. 

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/943fbff6-1ad1-4d4b-9d52-e9605691e1ad">CreateLayer(D2D1_SIZE_F*,ID2D1Layer**)</a>
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

The following example uses a layer to clip a bitmap to a geometric mask. For the complete example, see <a href="https://msdn.microsoft.com/eaeb6cfd-de62-46f1-972d-a11e0ccc11d9">How to Clip to a Geometric Mask</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT DemoApp::RenderWithLayer(ID2D1RenderTarget *pRT)
{
    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT-&gt;CreateLayer(NULL, &amp;pLayer);

    if (SUCCEEDED(hr))
    {
        pRT-&gt;SetTransform(D2D1::Matrix3x2F::Translation(350, 50));

        // Push the layer with the geometric mask.
        pRT-&gt;PushLayer(
            D2D1::LayerParameters(D2D1::InfiniteRect(), m_pPathGeometry),
            pLayer
            );
            
  
        pRT-&gt;DrawBitmap(m_pOrigBitmap, D2D1::RectF(0, 0, 200, 133));
        pRT-&gt;FillRectangle(D2D1::RectF(0.f, 0.f, 25.f, 25.f), m_pSolidColorBrush);  
        pRT-&gt;FillRectangle(D2D1::RectF(25.f, 25.f, 50.f, 50.f), m_pSolidColorBrush);
        pRT-&gt;FillRectangle(D2D1::RectF(50.f, 50.f, 75.f, 75.f), m_pSolidColorBrush); 
        pRT-&gt;FillRectangle(D2D1::RectF(75.f, 75.f, 100.f, 100.f), m_pSolidColorBrush);    
        pRT-&gt;FillRectangle(D2D1::RectF(100.f, 100.f, 125.f, 125.f), m_pSolidColorBrush); 
        pRT-&gt;FillRectangle(D2D1::RectF(125.f, 125.f, 150.f, 150.f), m_pSolidColorBrush);    
        

        pRT-&gt;PopLayer();
    }

    SafeRelease(&amp;pLayer);

    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>



<a href="https://msdn.microsoft.com/22d161fb-8470-49cc-a523-309f90643ea9">Layers Overview</a>
 

 

