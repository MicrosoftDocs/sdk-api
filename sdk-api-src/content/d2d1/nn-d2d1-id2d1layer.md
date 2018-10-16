---
UID: NN:d2d1.ID2D1Layer
title: ID2D1Layer
author: windows-sdk-content
description: Represents the backing store required to render a layer.
old-location: direct2d\ID2D1Layer.htm
tech.root: direct2d
ms.assetid: ce7b2345-f0e5-4e44-9146-b1f140bb00ca
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: ID2D1Layer, ID2D1Layer interface [Direct2D], ID2D1Layer interface [Direct2D],described, d2d1/ID2D1Layer, direct2d.ID2D1Layer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Layer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Layer interface


## -description


Represents the backing store required to render a layer.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1Layer</b> interface inherits from <a href="https://msdn.microsoft.com/8f19e74a-f010-4082-a4da-d1dc3cfe3192">ID2D1Resource</a>. <b>ID2D1Layer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1Layer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e9bf2990-6bd8-4247-9339-4ee652e21743">GetSize</a>
</td>
<td align="left" width="63%">
Gets the size of the layer in device-independent pixels.

</td>
</tr>
</table> 


## -remarks



To create a layer, call the <a href="https://msdn.microsoft.com/943fbff6-1ad1-4d4b-9d52-e9605691e1ad">CreateLayer</a> method of the render target where the layer will be used. To draw to a layer, push the layer to the render target stack by calling the <a href="https://msdn.microsoft.com/0fc7ac38-ff74-4f3b-9aa2-025a99e6b013">PushLayer</a> method. After you have finished drawing to the layer, call the <a href="https://msdn.microsoft.com/6ab05160-4f42-477f-a5bf-f16863b0635c">PopLayer</a> method.

Between  <a href="https://msdn.microsoft.com/905e9c76-d09e-4df8-8343-520d856ec6b8">PushLayer</a> and <a href="https://msdn.microsoft.com/6ab05160-4f42-477f-a5bf-f16863b0635c">PopLayer</a> calls, the layer is in use and cannot be used by another render target. 

If the size of the layer is not specified, the corresponding <a href="https://msdn.microsoft.com/905e9c76-d09e-4df8-8343-520d856ec6b8">PushLayer</a> call determines the minimum layer size, based on the layer content bounds and the geometric mask. The layer resource can be larger than the size required by <b>PushLayer</b> without any rendering artifacts.

If the size of a layer is specified, or if the layer has been used and the required backing store size as calculated during <a href="https://msdn.microsoft.com/905e9c76-d09e-4df8-8343-520d856ec6b8">PushLayer</a> is larger than the layer, then the layer resource is expanded on each axis monotonically to ensure that it is large enough. The layer resource never shrinks in size.

<h3><a id="Creating_ID2D1Layer_Objects"></a><a id="creating_id2d1layer_objects"></a><a id="CREATING_ID2D1LAYER_OBJECTS"></a>Creating ID2D1Layer Objects</h3>
To create a layer, call the <a href="https://msdn.microsoft.com/943fbff6-1ad1-4d4b-9d52-e9605691e1ad">CreateLayer</a> method of the render target where the layer will be used.

A layer is a device-dependent resource: your application should create layers after it initializes the render target with which the layers will be used, and recreate the layers whenever the render target needs recreated. (For more information about resources, see <a href="https://msdn.microsoft.com/afd308a7-9524-4436-9a0e-8575383d96fa">Resources Overview</a>.)


#### Examples

The following example uses a layer to clip a drawing to a geometric mask. For the complete example, see <a href="https://msdn.microsoft.com/eaeb6cfd-de62-46f1-972d-a11e0ccc11d9">How to Clip to a Geometric Mask</a>.

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



<a href="https://msdn.microsoft.com/8f19e74a-f010-4082-a4da-d1dc3cfe3192">ID2D1Resource</a>



<a href="https://msdn.microsoft.com/22d161fb-8470-49cc-a523-309f90643ea9">Layers Overview</a>
 

 

