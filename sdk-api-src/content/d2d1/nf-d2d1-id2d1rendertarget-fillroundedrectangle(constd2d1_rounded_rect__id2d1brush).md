---
UID: NF:d2d1.ID2D1RenderTarget.FillRoundedRectangle(constD2D1_ROUNDED_RECT&,ID2D1Brush)
title: ID2D1RenderTarget::FillRoundedRectangle(const D2D1_ROUNDED_RECT &,ID2D1Brush) (d2d1.h)
description: Paints the interior of the specified rounded rectangle. (overload 1/2)
helpviewer_keywords: ["FillRoundedRectangle","FillRoundedRectangle method [Direct2D]","FillRoundedRectangle method [Direct2D]","ID2D1RenderTarget interface","ID2D1RenderTarget interface [Direct2D]","FillRoundedRectangle method","ID2D1RenderTarget.FillRoundedRectangle","ID2D1RenderTarget.FillRoundedRectangle(const D2D1_ROUNDED_RECT &","ID2D1Brush)","ID2D1RenderTarget::FillRoundedRectangle","ID2D1RenderTarget::FillRoundedRectangle(const D2D1_ROUNDED_RECT &","ID2D1Brush)","d2d1/ID2D1RenderTarget::FillRoundedRectangle","direct2d.ID2D1RenderTarget_FillRoundedRectangle_ref_D2D1_ROUNDED_RECT_ptr_ID2D1Brush"]
old-location: direct2d\ID2D1RenderTarget_FillRoundedRectangle_ref_D2D1_ROUNDED_RECT_ptr_ID2D1Brush.htm
tech.root: Direct2D
ms.assetid: db000907-eff2-4cf7-a805-be1ff4cb30fe
ms.date: 12/05/2018
ms.keywords: FillRoundedRectangle, FillRoundedRectangle method [Direct2D], FillRoundedRectangle method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],FillRoundedRectangle method, ID2D1RenderTarget.FillRoundedRectangle, ID2D1RenderTarget.FillRoundedRectangle(const D2D1_ROUNDED_RECT &,ID2D1Brush), ID2D1RenderTarget::FillRoundedRectangle, ID2D1RenderTarget::FillRoundedRectangle(const D2D1_ROUNDED_RECT &,ID2D1Brush), d2d1/ID2D1RenderTarget::FillRoundedRectangle, direct2d.ID2D1RenderTarget_FillRoundedRectangle_ref_D2D1_ROUNDED_RECT_ptr_ID2D1Brush
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
 - ID2D1RenderTarget::FillRoundedRectangle
 - d2d1/ID2D1RenderTarget::FillRoundedRectangle
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
 - ID2D1RenderTarget.FillRoundedRectangle
---

## -description

Paints the interior of the specified rounded rectangle.

## -parameters

### -param roundedRect

Type: [in] <b>const <a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_rounded_rect">D2D1_ROUNDED_RECT</a> &</b>

The dimensions of the rounded rectangle to paint, in device independent pixels.

### -param brush [in]

Type: [in] <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>*</b>

The brush used to paint the interior of the rounded rectangle.

## -remarks

This method doesn't return an error code if it fails. To determine whether a drawing operation (such as <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillroundedrectangle(constd2d1_rounded_rect_id2d1brush)">FillRoundedRectangle</a>) failed, check the result returned by the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">ID2D1RenderTarget::EndDraw</a> or <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush">ID2D1RenderTarget::Flush</a> methods. 

## Examples

The following example uses the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillroundedrectangle(constd2d1_rounded_rect_id2d1brush)">DrawRoundedRectangle</a> and <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillroundedrectangle(constd2d1_rounded_rect_id2d1brush)">FillRoundedRectangle</a> methods to outline and fill a rounded rectangle.  This example produces the output shown in the following illustration.

<img alt="Illustration of four rounded rectangles with different stroke styles and fills" src="images/drawroundedrectangle_scr.png"/>

```cpp
//  Called whenever the application needs to display the client
//  window.
HRESULT DrawAndFillRoundedRectangleExample::OnRender()
{
    HRESULT hr;

    // Create the render target and brushes if they
    // don't already exists.
    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        // Retrieve the size of the render target.
        D2D1_SIZE_F renderTargetSize = m_pRenderTarget->GetSize();

        m_pRenderTarget->BeginDraw();
        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());
        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        // Paint a grid background.
        m_pRenderTarget->FillRectangle(
            D2D1::RectF(0.0f, 0.0f, renderTargetSize.width, renderTargetSize.height),
            m_pGridPatternBitmapBrush
            );

        // Define a rounded rectangle.
        D2D1_ROUNDED_RECT roundedRect = D2D1::RoundedRect(
            D2D1::RectF(20.f, 20.f, 150.f, 100.f),
            10.f,
            10.f
            );

        // Draw the rectangle.
        m_pRenderTarget->DrawRoundedRectangle(roundedRect, m_pBlackBrush, 10.f);

        // Apply a translation transform.
        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Translation(200.f, 0.f));

        // Draw the rounded rectangle again, this time with a dashed stroke.
        m_pRenderTarget->DrawRoundedRectangle(roundedRect, m_pBlackBrush, 10.f, m_pStrokeStyle);

        // Apply another translation transform.
        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Translation(0.f, 150.f));

        // Draw, then fill the rounded rectangle.
        m_pRenderTarget->DrawRoundedRectangle(roundedRect, m_pBlackBrush, 10.f, m_pStrokeStyle);
        m_pRenderTarget->FillRoundedRectangle(roundedRect, m_pSilverBrush);

        // Apply another translation transform.
        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Translation(200.f, 150.f));

        // Fill, then draw the rounded rectangle.
        m_pRenderTarget->FillRoundedRectangle(roundedRect, m_pSilverBrush);
        m_pRenderTarget->DrawRoundedRectangle(roundedRect, m_pBlackBrush, 10.f, m_pStrokeStyle);

        hr = m_pRenderTarget->EndDraw();

        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
    }

    return hr;
}
```

## -see-also

<a href="/windows/win32/api/d2d1helper/nf-d2d1helper-roundedrect">D2D1::RoundedRect</a>

<a href="/windows/win32/Direct2D/how-to-draw-an-ellipse">How to Draw and Fill a Basic Shape</a>

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>

