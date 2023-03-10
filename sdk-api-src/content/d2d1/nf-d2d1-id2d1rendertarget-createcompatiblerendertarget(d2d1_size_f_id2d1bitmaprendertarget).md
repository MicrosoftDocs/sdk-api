---
UID: NF:d2d1.ID2D1RenderTarget.CreateCompatibleRenderTarget(D2D1_SIZE_F,ID2D1BitmapRenderTarget)
title: ID2D1RenderTarget::CreateCompatibleRenderTarget(D2D1_SIZE_F,ID2D1BitmapRenderTarget) (d2d1.h)
description: Creates a new bitmap render target for use during intermediate offscreen drawing that is compatible with the current render target and has the same pixel format (but not alpha mode) as the current render target.
helpviewer_keywords: ["CreateCompatibleRenderTarget","CreateCompatibleRenderTarget method [Direct2D]","CreateCompatibleRenderTarget method [Direct2D]","ID2D1RenderTarget interface","ID2D1RenderTarget interface [Direct2D]","CreateCompatibleRenderTarget method","ID2D1RenderTarget.CreateCompatibleRenderTarget","ID2D1RenderTarget.CreateCompatibleRenderTarget(D2D1_SIZE_F","ID2D1BitmapRenderTarget)","ID2D1RenderTarget::CreateCompatibleRenderTarget","ID2D1RenderTarget::CreateCompatibleRenderTarget(D2D1_SIZE_F","ID2D1BitmapRenderTarget)","d2d1/ID2D1RenderTarget::CreateCompatibleRenderTarget","direct2d.ID2D1RenderTarget_CreateCompatibleRenderTarget_D2D_SIZE_F_ptr_ptr_ID2D1BitmapRenderTarget","direct2d.ID2D1RenderTarget_CreateCompatibleRenderTarget_overload3"]
old-location: direct2d\ID2D1RenderTarget_CreateCompatibleRenderTarget_overload3.htm
tech.root: Direct2D
ms.assetid: f8687186-abea-4412-83f7-b0d89b453d9d
ms.date: 12/05/2018
ms.keywords: CreateCompatibleRenderTarget, CreateCompatibleRenderTarget method [Direct2D], CreateCompatibleRenderTarget method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],CreateCompatibleRenderTarget method, ID2D1RenderTarget.CreateCompatibleRenderTarget, ID2D1RenderTarget.CreateCompatibleRenderTarget(D2D1_SIZE_F,ID2D1BitmapRenderTarget), ID2D1RenderTarget::CreateCompatibleRenderTarget, ID2D1RenderTarget::CreateCompatibleRenderTarget(D2D1_SIZE_F,ID2D1BitmapRenderTarget), d2d1/ID2D1RenderTarget::CreateCompatibleRenderTarget, direct2d.ID2D1RenderTarget_CreateCompatibleRenderTarget_D2D_SIZE_F_ptr_ptr_ID2D1BitmapRenderTarget, direct2d.ID2D1RenderTarget_CreateCompatibleRenderTarget_overload3
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
 - ID2D1RenderTarget::CreateCompatibleRenderTarget
 - d2d1/ID2D1RenderTarget::CreateCompatibleRenderTarget
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
 - ID2D1RenderTarget.CreateCompatibleRenderTarget
---

## -description

Creates a bitmap render target for use during intermediate offscreen drawing that is compatible with the current render target.

## -parameters

### -param desiredSize

Type: [in] <b><a href="/windows/win32/Direct2D/d2d1-size-f">D2D1_SIZE_F</a></b>

The desired size of the new render target in device-independent pixels. The pixel size is computed from the desired size using the parent target DPI. If the <i>desiredSize</i> maps to a integer-pixel size, the DPI of the compatible render target is the same as the DPI of the parent target. If <i>desiredSize</i> maps to a fractional-pixel size, the pixel size is rounded up to the nearest integer and the DPI for the compatible render target is slightly higher than the DPI of the parent render target. In all cases, the coordinate (<i>desiredSize</i>.width, <i>desiredSize</i>.height) maps to the lower-right corner of the compatible render target.

### -param bitmapRenderTarget

Type: [out] <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget">ID2D1BitmapRenderTarget</a>**</b>

When this method returns, contains a pointer to a pointer to a new bitmap render target. This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -remarks

The bitmap render target created by this method is not compatible with GDI. 

## Examples

The following example uses the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(constd2d1_size_f_constd2d1_size_u_constd2d1_pixel_format_d2d1_compatible_render_target_options_id2d1bitmaprendertarget)">CreateCompatibleRenderTarget</a> method to create an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget">ID2D1BitmapRenderTarget</a> and uses it to  draw a grid pattern. The grid pattern is used as the source of an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush">ID2D1BitmapBrush</a>.

```cpp
HRESULT DemoApp::CreateGridPatternBrush(
    ID2D1RenderTarget *pRenderTarget,
    ID2D1BitmapBrush **ppBitmapBrush
    )
{
    // Create a compatible render target.
    ID2D1BitmapRenderTarget *pCompatibleRenderTarget = NULL;
    HRESULT hr = pRenderTarget->CreateCompatibleRenderTarget(
        D2D1::SizeF(10.0f, 10.0f),
        &pCompatibleRenderTarget
        );
    if (SUCCEEDED(hr))
    {
        // Draw a pattern.
        ID2D1SolidColorBrush *pGridBrush = NULL;
        hr = pCompatibleRenderTarget->CreateSolidColorBrush(
            D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f)),
            &pGridBrush
            );
        if (SUCCEEDED(hr))
        {
            pCompatibleRenderTarget->BeginDraw();
            pCompatibleRenderTarget->FillRectangle(D2D1::RectF(0.0f, 0.0f, 10.0f, 1.0f), pGridBrush);
            pCompatibleRenderTarget->FillRectangle(D2D1::RectF(0.0f, 0.1f, 1.0f, 10.0f), pGridBrush);
            pCompatibleRenderTarget->EndDraw();

            // Retrieve the bitmap from the render target.
            ID2D1Bitmap *pGridBitmap = NULL;
            hr = pCompatibleRenderTarget->GetBitmap(&pGridBitmap);
            if (SUCCEEDED(hr))
            {
                // Choose the tiling mode for the bitmap brush.
                D2D1_BITMAP_BRUSH_PROPERTIES brushProperties =
                    D2D1::BitmapBrushProperties(D2D1_EXTEND_MODE_WRAP, D2D1_EXTEND_MODE_WRAP);

                // Create the bitmap brush.
                hr = m_pRenderTarget->CreateBitmapBrush(pGridBitmap, brushProperties, ppBitmapBrush);

                pGridBitmap->Release();
            }

            pGridBrush->Release();
        }

        pCompatibleRenderTarget->Release();
    }

    return hr;
}
```

The following code example uses the brush to paint a pattern.

```cpp
// Paint a grid background.
m_pRenderTarget->FillRectangle(
    D2D1::RectF(0.0f, 0.0f, renderTargetSize.width, renderTargetSize.height),
    m_pGridPatternBitmapBrush
    );
```

Code has been omitted from this example.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>

<a href="/windows/win32/Direct2D/supported-pixel-formats-and-alpha-modes">Supported Pixel  Formats and Alpha Modes</a>

