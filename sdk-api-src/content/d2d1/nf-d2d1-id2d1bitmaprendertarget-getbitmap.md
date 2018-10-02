---
UID: NF:d2d1.ID2D1BitmapRenderTarget.GetBitmap
title: ID2D1BitmapRenderTarget::GetBitmap
author: windows-sdk-content
description: Retrieves the bitmap for this render target. The returned bitmap can be used for drawing operations.
old-location: direct2d\ID2D1BitmapRenderTarget_GetBitmap.htm
tech.root: direct2d
ms.assetid: 173a3e2d-82b8-4c33-9a74-1bbf755bbf65
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: GetBitmap, GetBitmap method [Direct2D], GetBitmap method [Direct2D],ID2D1BitmapRenderTarget interface, ID2D1BitmapRenderTarget interface [Direct2D],GetBitmap method, ID2D1BitmapRenderTarget.GetBitmap, ID2D1BitmapRenderTarget::GetBitmap, d2d1/ID2D1BitmapRenderTarget::GetBitmap, direct2d.ID2D1BitmapRenderTarget_GetBitmap
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
 - ID2D1BitmapRenderTarget.GetBitmap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1BitmapRenderTarget::GetBitmap


## -description


Retrieves the bitmap for this render target. The returned bitmap can be used for drawing operations.


## -parameters




### -param bitmap [out]

Type: <b><a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a>**</b>

When this method returns, contains the address of a pointer to the bitmap for this render target. This bitmap can be used for drawing operations.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The DPI for the <a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a> obtained from <b>GetBitmap</b> will be the DPI of the <a href="https://msdn.microsoft.com/f298d4f7-acb8-4fbe-89f7-2410e3b753bd">ID2D1BitmapRenderTarget</a> when the render target was created. Changing the DPI of the <b>ID2D1BitmapRenderTarget</b> by calling  <a href="https://msdn.microsoft.com/603a838b-4abc-4adf-93a9-ec8535d42ed6">SetDpi</a> doesn't affect the DPI of the bitmap, even if <b>SetDpi</b> is called before <b>GetBitmap</b>. Using <b>SetDpi</b> to change the DPI of the <b>ID2D1BitmapRenderTarget</b> does affect how contents are rendered into the bitmap: it just doesn't affect the DPI of the bitmap retrieved by <b>GetBitmap</b>.


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




<a href="https://msdn.microsoft.com/f298d4f7-acb8-4fbe-89f7-2410e3b753bd">ID2D1BitmapRenderTarget</a>
 

 

