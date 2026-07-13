---
UID: NF:d2d1.ID2D1BitmapRenderTarget.GetBitmap
title: ID2D1BitmapRenderTarget::GetBitmap (d2d1.h)
description: Retrieves the bitmap for this render target. The returned bitmap can be used for drawing operations.
helpviewer_keywords: ["GetBitmap","GetBitmap method [Direct2D]","GetBitmap method [Direct2D]","ID2D1BitmapRenderTarget interface","ID2D1BitmapRenderTarget interface [Direct2D]","GetBitmap method","ID2D1BitmapRenderTarget.GetBitmap","ID2D1BitmapRenderTarget::GetBitmap","d2d1/ID2D1BitmapRenderTarget::GetBitmap","direct2d.ID2D1BitmapRenderTarget_GetBitmap"]
old-location: direct2d\ID2D1BitmapRenderTarget_GetBitmap.htm
tech.root: Direct2D
ms.assetid: 173a3e2d-82b8-4c33-9a74-1bbf755bbf65
ms.date: 12/05/2018
ms.keywords: GetBitmap, GetBitmap method [Direct2D], GetBitmap method [Direct2D],ID2D1BitmapRenderTarget interface, ID2D1BitmapRenderTarget interface [Direct2D],GetBitmap method, ID2D1BitmapRenderTarget.GetBitmap, ID2D1BitmapRenderTarget::GetBitmap, d2d1/ID2D1BitmapRenderTarget::GetBitmap, direct2d.ID2D1BitmapRenderTarget_GetBitmap
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
 - ID2D1BitmapRenderTarget::GetBitmap
 - d2d1/ID2D1BitmapRenderTarget::GetBitmap
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
 - ID2D1BitmapRenderTarget.GetBitmap
---

# ID2D1BitmapRenderTarget::GetBitmap


## -description

Retrieves the bitmap for this render target. The returned bitmap can be used for drawing operations.

## -parameters

### -param bitmap [out]

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a>**</b>

When this method returns, contains the address of a pointer to the bitmap for this render target. This bitmap can be used for drawing operations.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -remarks

The DPI for the <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a> obtained from <b>GetBitmap</b> will be the DPI of the <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget">ID2D1BitmapRenderTarget</a> when the render target was created. Changing the DPI of the <b>ID2D1BitmapRenderTarget</b> by calling  <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setdpi">SetDpi</a> doesn't affect the DPI of the bitmap, even if <b>SetDpi</b> is called before <b>GetBitmap</b>. Using <b>SetDpi</b> to change the DPI of the <b>ID2D1BitmapRenderTarget</b> does affect how contents are rendered into the bitmap: it just doesn't affect the DPI of the bitmap retrieved by <b>GetBitmap</b>.


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
        

<div class="code"></div>

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget">ID2D1BitmapRenderTarget</a>

