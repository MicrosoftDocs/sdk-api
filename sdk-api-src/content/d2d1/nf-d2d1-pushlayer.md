---
UID: NF:d2d1.PushLayer
title: PushLayer function
author: windows-sdk-content
description: Adds the specified layer to the render target so that it receives all subsequent drawing operations until PopLayer is called.
old-location: direct2d\id2d1rendertarget_push_layer.htm
old-project: direct2d
ms.assetid: 9336662c-e94e-40ba-adbe-066d704958bc
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ID2D1RenderTarget::PushLayer, PushLayer, PushLayer methods [Direct2D], d2d1_1/PushLayer, direct2d.id2d1rendertarget_push_layer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: d2d1.h
req.include-header: D2d1.h
req.redist: 
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
tech.root: 
req.typenames: D2D1_WINDOW_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - ID2D1RenderTarget::PushLayer
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# PushLayer function


## -description


<span>Adds the specified layer to the render target so that it receives all subsequent drawing operations until <a href="https://msdn.microsoft.com/6ab05160-4f42-477f-a5bf-f16863b0635c">PopLayer</a> is called. 
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/905e9c76-d09e-4df8-8343-520d856ec6b8">PushLayer(D2D1_LAYER_PARAMETERS&,ID2D1Layer*)</a>
</td>
<td align="left" width="63%">
Adds the specified layer to the render target so that it receives all subsequent drawing operations until <a href="https://msdn.microsoft.com/6ab05160-4f42-477f-a5bf-f16863b0635c">PopLayer</a> is called.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0fc7ac38-ff74-4f3b-9aa2-025a99e6b013">PushLayer(D2D1_LAYER_PARAMETERS*,ID2D1Layer*)</a>
</td>
<td align="left" width="63%">
Adds the specified layer to the render target so that it receives all subsequent drawing operations until <a href="https://msdn.microsoft.com/6ab05160-4f42-477f-a5bf-f16863b0635c">PopLayer</a> is called. 

</td>
</tr>
</table>

## -parameters


## -remarks



The <a href="https://msdn.microsoft.com/905e9c76-d09e-4df8-8343-520d856ec6b8">PushLayer</a> method enables a caller to begin redirecting rendering to a layer. All rendering operations are valid in a layer. The location of the layer is affected by the world transform set on the render target. 

Each <b>PushLayer</b> must have a matching <a href="https://msdn.microsoft.com/6ab05160-4f42-477f-a5bf-f16863b0635c">PopLayer</a> call. If there are more <b>PopLayer</b> calls than <b>PushLayer</b> calls, the render target is placed into an error state. If <a href="https://msdn.microsoft.com/3ad9c966-85f5-4ddb-a8c1-aefcba533509">Flush</a> is called before all outstanding layers are popped, the render target is placed into an error state, and an error is returned. The error state can be cleared by a call to <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">EndDraw</a>.

A particular <a href="https://msdn.microsoft.com/ce7b2345-f0e5-4e44-9146-b1f140bb00ca">ID2D1Layer</a> resource can be active only at one time. In other words, you cannot call a <a href="https://msdn.microsoft.com/905e9c76-d09e-4df8-8343-520d856ec6b8">PushLayer</a>  method, and then immediately follow  with another <b>PushLayer</b> method with the same layer resource. Instead, you must call the second <b>PushLayer</b> method with different layer resources. 


For an example, see <a href="https://msdn.microsoft.com/eaeb6cfd-de62-46f1-972d-a11e0ccc11d9">How to Clip a Region with Layers</a>.

This method doesn't return an error code if it fails. To determine whether a drawing operation (such as <b>PushLayer</b>) failed, check the result returned by the <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">ID2D1RenderTarget::EndDraw</a> or <a href="https://msdn.microsoft.com/3ad9c966-85f5-4ddb-a8c1-aefcba533509">ID2D1RenderTarget::Flush</a> methods. 


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
 

 

