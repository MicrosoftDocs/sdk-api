---
UID: NF:d2d1.ID2D1RenderTarget.FillRectangle(constD2D1_RECT_F&,ID2D1Brush)
title: ID2D1RenderTarget::FillRectangle(const D2D1_RECT_F &,ID2D1Brush) (d2d1.h)
description: Paints the interior of the specified rectangle.
helpviewer_keywords: ["FillRectangle","FillRectangle method [Direct2D]","FillRectangle method [Direct2D]","ID2D1RenderTarget interface","ID2D1RenderTarget interface [Direct2D]","FillRectangle method","ID2D1RenderTarget.FillRectangle","ID2D1RenderTarget.FillRectangle(const D2D1_RECT_F &","ID2D1Brush)","ID2D1RenderTarget::FillRectangle","ID2D1RenderTarget::FillRectangle(const D2D1_RECT_F &","ID2D1Brush)","d2d1/ID2D1RenderTarget::FillRectangle","direct2d.ID2D1RenderTarget_FillRectangle_ref_D2D_RECT_F_ptr_ID2D1Brush"]
old-location: direct2d\ID2D1RenderTarget_FillRectangle_ref_D2D_RECT_F_ptr_ID2D1Brush.htm
tech.root: Direct2D
ms.assetid: b5d7ca28-0751-4799-8480-f221fd5fe276
ms.date: 12/05/2018
ms.keywords: FillRectangle, FillRectangle method [Direct2D], FillRectangle method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],FillRectangle method, ID2D1RenderTarget.FillRectangle, ID2D1RenderTarget.FillRectangle(const D2D1_RECT_F &,ID2D1Brush), ID2D1RenderTarget::FillRectangle, ID2D1RenderTarget::FillRectangle(const D2D1_RECT_F &,ID2D1Brush), d2d1/ID2D1RenderTarget::FillRectangle, direct2d.ID2D1RenderTarget_FillRectangle_ref_D2D_RECT_F_ptr_ID2D1Brush
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
 - ID2D1RenderTarget::FillRectangle
 - d2d1/ID2D1RenderTarget::FillRectangle
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
 - ID2D1RenderTarget.FillRectangle
---

## -description

Paints the interior of the specified rectangle.

## -parameters

### -param rect

Type: [in] <b>const <a href="/windows/win32/Direct2D/d2d1-rect-f">D2D1_RECT_F</a> &</b>

The dimension of the rectangle to paint, in device-independent pixels.

### -param brush

Type: [in] <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>*</b>

The brush used to paint the rectangle's interior.

## -remarks

This method doesn't return an error code if it fails. To determine whether a drawing operation (such as <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f_id2d1brush)">FillRectangle</a>) failed, check the result returned by the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">ID2D1RenderTarget::EndDraw</a> or <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush">ID2D1RenderTarget::Flush</a> methods. 

## Examples

The following example uses an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget">ID2D1HwndRenderTarget</a> to draw and fill several rectangles. This example produces the output shown in the following illustration.

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

For a related tutorial, see <a href="/windows/win32/Direct2D/direct2d-quickstart">Creating a Simple Direct2D Application</a>.

## -see-also

<a href="/windows/win32/Direct2D/direct2d-quickstart">Creating a Simple Direct2D Application</a>

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>

