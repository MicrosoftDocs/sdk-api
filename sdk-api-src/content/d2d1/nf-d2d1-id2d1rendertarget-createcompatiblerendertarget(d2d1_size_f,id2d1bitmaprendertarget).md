---
UID: NF:d2d1.ID2D1RenderTarget.CreateCompatibleRenderTarget(D2D1_SIZE_F,ID2D1BitmapRenderTarget)
title: ID2D1RenderTarget::CreateCompatibleRenderTarget(D2D1_SIZE_F,ID2D1BitmapRenderTarget)
author: windows-sdk-content
description: Creates a new bitmap render target for use during intermediate offscreen drawing that is compatible with the current render target and has the same pixel format (but not alpha mode) as the current render target.
old-location: direct2d\ID2D1RenderTarget_CreateCompatibleRenderTarget_overload3.htm
tech.root: direct2d
ms.assetid: f8687186-abea-4412-83f7-b0d89b453d9d
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: CreateCompatibleRenderTarget, CreateCompatibleRenderTarget method [Direct2D], CreateCompatibleRenderTarget method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],CreateCompatibleRenderTarget method, ID2D1RenderTarget.CreateCompatibleRenderTarget, ID2D1RenderTarget.CreateCompatibleRenderTarget(D2D1_SIZE_F,ID2D1BitmapRenderTarget), ID2D1RenderTarget::CreateCompatibleRenderTarget, ID2D1RenderTarget::CreateCompatibleRenderTarget(D2D1_SIZE_F,ID2D1BitmapRenderTarget), d2d1/ID2D1RenderTarget::CreateCompatibleRenderTarget, direct2d.ID2D1RenderTarget_CreateCompatibleRenderTarget_D2D_SIZE_F_ptr_ptr_ID2D1BitmapRenderTarget, direct2d.ID2D1RenderTarget_CreateCompatibleRenderTarget_overload3
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ID2D1RenderTarget.CreateCompatibleRenderTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget::CreateCompatibleRenderTarget(D2D1_SIZE_F,ID2D1BitmapRenderTarget)


## -description


Creates a new  bitmap render target for use during intermediate offscreen drawing that is compatible with the current render target and has the same pixel format (but not alpha mode) as the current render target.


## -parameters




### -param desiredSize

Type: <b><a href="https://msdn.microsoft.com/c2fd41fb-72b3-418b-ad87-65549b04657d">D2D1_SIZE_F</a></b>

The desired size of the new render target in device-independent pixels. The pixel size is computed from the desired size using the parent target DPI. If the <i>desiredSize</i> maps to a integer-pixel size, the DPI of the compatible render target is the same as the DPI of the parent target.  If <i>desiredSize</i> maps to a fractional-pixel size, the pixel size is rounded up to the nearest integer and the DPI for the compatible render target is slightly higher than the DPI of the parent render target. In all cases, the coordinate (<i>desiredSize</i>.width, <i>desiredSize</i>.height) maps to the lower-right corner of the compatible render target.


### -param bitmapRenderTarget [out]

Type: <b><a href="https://msdn.microsoft.com/f298d4f7-acb8-4fbe-89f7-2410e3b753bd">ID2D1BitmapRenderTarget</a>**</b>

When this method returns, contains the address of  a pointer to a new bitmap render target. This parameter is passed uninitialized.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The bitmap render target created by this method is not compatible with GDI. 


#### Examples

The following example uses the <a href="https://msdn.microsoft.com/4a799a7c-0d2f-460f-99f9-24c6cf7c4537">CreateCompatibleRenderTarget</a> method to create an <a href="https://msdn.microsoft.com/f298d4f7-acb8-4fbe-89f7-2410e3b753bd">ID2D1BitmapRenderTarget</a> and uses it to  draw a grid pattern. The grid pattern is used as the source of an <a href="https://msdn.microsoft.com/22b14ffa-14cb-4e4d-bf80-7d81e4ae9ee4">ID2D1BitmapBrush</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT DemoApp::CreateGridPatternBrush(
    ID2D1RenderTarget *pRenderTarget,
    ID2D1BitmapBrush **ppBitmapBrush
    )
{
    // Create a compatible render target.
    ID2D1BitmapRenderTarget *pCompatibleRenderTarget = NULL;
    HRESULT hr = pRenderTarget-&gt;CreateCompatibleRenderTarget(
        D2D1::SizeF(10.0f, 10.0f),
        &amp;pCompatibleRenderTarget
        );
    if (SUCCEEDED(hr))
    {
        // Draw a pattern.
        ID2D1SolidColorBrush *pGridBrush = NULL;
        hr = pCompatibleRenderTarget-&gt;CreateSolidColorBrush(
            D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f)),
            &amp;pGridBrush
            );
        if (SUCCEEDED(hr))
        {
            pCompatibleRenderTarget-&gt;BeginDraw();
            pCompatibleRenderTarget-&gt;FillRectangle(D2D1::RectF(0.0f, 0.0f, 10.0f, 1.0f), pGridBrush);
            pCompatibleRenderTarget-&gt;FillRectangle(D2D1::RectF(0.0f, 0.1f, 1.0f, 10.0f), pGridBrush);
            pCompatibleRenderTarget-&gt;EndDraw();

            // Retrieve the bitmap from the render target.
            ID2D1Bitmap *pGridBitmap = NULL;
            hr = pCompatibleRenderTarget-&gt;GetBitmap(&amp;pGridBitmap);
            if (SUCCEEDED(hr))
            {
                // Choose the tiling mode for the bitmap brush.
                D2D1_BITMAP_BRUSH_PROPERTIES brushProperties =
                    D2D1::BitmapBrushProperties(D2D1_EXTEND_MODE_WRAP, D2D1_EXTEND_MODE_WRAP);

                // Create the bitmap brush.
                hr = m_pRenderTarget-&gt;CreateBitmapBrush(pGridBitmap, brushProperties, ppBitmapBrush);

                pGridBitmap-&gt;Release();
            }

            pGridBrush-&gt;Release();
        }

        pCompatibleRenderTarget-&gt;Release();
    }

    return hr;
}
</pre>
</td>
</tr>
</table></span></div>
The following code example uses the brush to paint a pattern.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Paint a grid background.
m_pRenderTarget-&gt;FillRectangle(
    D2D1::RectF(0.0f, 0.0f, renderTargetSize.width, renderTargetSize.height),
    m_pGridPatternBitmapBrush
    );
</pre>
</td>
</tr>
</table></span></div>
Code has been omitted from this example. 

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>



<a href="https://msdn.microsoft.com/09b1f9c6-1780-4733-ac22-9e8c21466b67">Supported Pixel  Formats and Alpha Modes</a>
 

 

