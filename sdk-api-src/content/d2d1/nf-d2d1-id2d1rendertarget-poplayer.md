---
UID: NF:d2d1.ID2D1RenderTarget.PopLayer
title: ID2D1RenderTarget::PopLayer
author: windows-sdk-content
description: Stops redirecting drawing operations to the layer that is specified by the last PushLayer call.
old-location: direct2d\ID2D1RenderTarget_PopLayer.htm
old-project: direct2d
ms.assetid: 6ab05160-4f42-477f-a5bf-f16863b0635c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ID2D1RenderTarget interface [Direct2D],PopLayer method, ID2D1RenderTarget.PopLayer, ID2D1RenderTarget::PopLayer, PopLayer, PopLayer method [Direct2D], PopLayer method [Direct2D],ID2D1RenderTarget interface, d2d1/ID2D1RenderTarget::PopLayer, direct2d.ID2D1RenderTarget_PopLayer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d2d1.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D2D1_WINDOW_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1RenderTarget.PopLayer
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# ID2D1RenderTarget::PopLayer


## -description


Stops redirecting drawing operations to the layer that is specified by the last <a href="https://msdn.microsoft.com/0fc7ac38-ff74-4f3b-9aa2-025a99e6b013">PushLayer</a> call. 


## -parameters






## -returns



This method does not return a value.




## -remarks



A <b>PopLayer</b>  must match a previous <a href="https://msdn.microsoft.com/0fc7ac38-ff74-4f3b-9aa2-025a99e6b013">PushLayer</a> call.

This method doesn't return an error code if it fails. To determine whether a drawing operation (such as <b>PopLayer</b>) failed, check the result returned by the <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">ID2D1RenderTarget::EndDraw</a> or <a href="https://msdn.microsoft.com/3ad9c966-85f5-4ddb-a8c1-aefcba533509">ID2D1RenderTarget::Flush</a> methods. 


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



<a href="https://msdn.microsoft.com/0fc7ac38-ff74-4f3b-9aa2-025a99e6b013">PushLayer</a>
 

 

