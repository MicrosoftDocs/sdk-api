---
UID: NF:d2d1.ID2D1RenderTarget.DrawRectangle
title: ID2D1RenderTarget::DrawRectangle (d2d1.h)
author: windows-sdk-content
description: Draws the outline of a rectangle that has the specified dimensions and stroke style.
old-location: direct2d\id2d1rendertarget_drawrectangle.htm
tech.root: Direct2D
ms.assetid: 3f8c0754-fa68-4b5b-812f-24d8b544ba6e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DrawRectangle, DrawRectangle methods [Direct2D], ID2D1RenderTarget.DrawRectangle, ID2D1RenderTarget::DrawRectangle, d2d1_1/DrawRectangle, direct2d.id2d1rendertarget_drawrectangle
ms.topic: method
req.header: d2d1.h
req.include-header: D2d1.h
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
 - ID2D1RenderTarget::DrawRectangle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1RenderTarget::DrawRectangle


## -description


<span>Draws the outline of a rectangle that has the specified dimensions and stroke style.
    
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)">DrawRectangle(D2D1_RECT_F&,ID2D1Brush*,FLOAT,ID2D1StrokeStyle*)</a>
</td>
<td align="left" width="63%">
Draws the outline of a rectangle that has the specified dimensions and stroke style.
    

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)">DrawRectangle(D2D1_RECT_F*,ID2D1Brush*,FLOAT,ID2D1StrokeStyle*)</a>
</td>
<td align="left" width="63%">
Draws the outline of a rectangle that has the specified dimensions and stroke style.

</td>
</tr>
</table>

## -parameters


## -remarks



When this method fails, it does not return an error code. To determine whether a drawing method (such as <b>DrawRectangle</b>) failed, check the result returned by the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">ID2D1RenderTarget::EndDraw</a> or <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-flush">ID2D1RenderTarget::Flush</a> method. 


#### Examples

The following example uses an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget">ID2D1HwndRenderTarget</a> to draw and fill several rectangles. This example produces the output shown in the following illustration.

<img alt="Illustration of two rectangles on a grid background" src="images/drawrectangleexample_small.png"/>


```cpp
// This method discards device-specific
// resources if the Direct3D device dissapears during execution and
// recreates the resources the next time it's invoked.
HRESULT DemoApp::OnRender()
{
    HRESULT hr = S_OK;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();

        // Draw a grid background.
        int width = static_cast<int>(rtSize.width);
        int height = static_cast<int>(rtSize.height);

        for (int x = 0; x < width; x += 10)
        {
            m_pRenderTarget->DrawLine(
                D2D1::Point2F(static_cast<FLOAT>(x), 0.0f),
                D2D1::Point2F(static_cast<FLOAT>(x), rtSize.height),
                m_pLightSlateGrayBrush,
                0.5f
                );
        }

        for (int y = 0; y < height; y += 10)
        {
            m_pRenderTarget->DrawLine(
                D2D1::Point2F(0.0f, static_cast<FLOAT>(y)),
                D2D1::Point2F(rtSize.width, static_cast<FLOAT>(y)),
                m_pLightSlateGrayBrush,
                0.5f
                );
        }

        // Draw two rectangles.
        D2D1_RECT_F rectangle1 = D2D1::RectF(
            rtSize.width/2 - 50.0f,
            rtSize.height/2 - 50.0f,
            rtSize.width/2 + 50.0f,
            rtSize.height/2 + 50.0f
            );

        D2D1_RECT_F rectangle2 = D2D1::RectF(
            rtSize.width/2 - 100.0f,
            rtSize.height/2 - 100.0f,
            rtSize.width/2 + 100.0f,
            rtSize.height/2 + 100.0f
            );


        // Draw a filled rectangle.
        m_pRenderTarget->FillRectangle(&rectangle1, m_pLightSlateGrayBrush);

        // Draw the outline of a rectangle.
        m_pRenderTarget->DrawRectangle(&rectangle2, m_pCornflowerBlueBrush);

        hr = m_pRenderTarget->EndDraw();
    }

    if (hr == D2DERR_RECREATE_TARGET)
    {
        hr = S_OK;
        DiscardDeviceResources();
    }

    return hr;
}

```


For a related tutorial, see <a href="https://docs.microsoft.com/windows/desktop/Direct2D/direct2d-quickstart">Creating a Simple Direct2D Application</a>. 

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Direct2D/direct2d-quickstart">Creating a Simple Direct2D Application</a>



<a href="https://docs.microsoft.com/windows/desktop/Direct2D/how-to-draw-an-ellipse">How to Draw and Fill a Basic Shape</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>
 

 

