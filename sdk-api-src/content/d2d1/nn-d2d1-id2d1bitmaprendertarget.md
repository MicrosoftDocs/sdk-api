---
UID: NN:d2d1.ID2D1BitmapRenderTarget
title: ID2D1BitmapRenderTarget
author: windows-sdk-content
description: Renders to an intermediate texture created by the CreateCompatibleRenderTarget method.
old-location: direct2d\ID2D1BitmapRenderTarget.htm
tech.root: Direct2D
ms.assetid: f298d4f7-acb8-4fbe-89f7-2410e3b753bd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID2D1BitmapRenderTarget, ID2D1BitmapRenderTarget interface [Direct2D], ID2D1BitmapRenderTarget interface [Direct2D],described, d2d1/ID2D1BitmapRenderTarget, direct2d.ID2D1BitmapRenderTarget
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
 - ID2D1BitmapRenderTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1BitmapRenderTarget interface


## -description


Renders to an intermediate texture created by the <a href="https://msdn.microsoft.com/en-us/library/Dd742780(v=VS.85).aspx">CreateCompatibleRenderTarget</a> method. 



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1BitmapRenderTarget</b> interface inherits from <a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>. <b>ID2D1BitmapRenderTarget</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1BitmapRenderTarget</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/173a3e2d-82b8-4c33-9a74-1bbf755bbf65">GetBitmap</a>
</td>
<td align="left" width="63%">
Retrieves the bitmap for this render target. The returned bitmap can be used for drawing operations.

</td>
</tr>
</table> 


## -remarks



An <b>ID2D1BitmapRenderTarget</b>  writes to an intermediate texture. It's useful for creating patterns for use with an <a href="https://msdn.microsoft.com/22b14ffa-14cb-4e4d-bf80-7d81e4ae9ee4">ID2D1BitmapBrush</a> or caching drawing data that will be used repeatedly. 

To write directly to a WIC bitmap instead, use the <a href="https://msdn.microsoft.com/93141743-c11d-40b4-83c5-07c9066836c7">ID2D1Factory::CreateWicBitmapRenderTarget</a> method. This method returns an <a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a> that writes to the specified WIC bitmap. 
      

<h3><a id="Creating_ID2D1BitmapRenderTarget_Objects"></a><a id="creating_id2d1bitmaprendertarget_objects"></a><a id="CREATING_ID2D1BITMAPRENDERTARGET_OBJECTS"></a>Creating ID2D1BitmapRenderTarget Objects</h3>
To create a bitmap render target, call the <a href="https://msdn.microsoft.com/en-us/library/Dd742780(v=VS.85).aspx">ID2D1RenderTarget::CreateCompatibleRenderTarget</a> method.

Like other render targets, an <b>ID2D1BitmapRenderTarget</b> is a device-dependent resource and must be recreated when the associated device becomes unavailable. For more information, see the <a href="https://msdn.microsoft.com/afd308a7-9524-4436-9a0e-8575383d96fa">Resources Overview</a>.


#### Examples

The following example uses the <a href="https://msdn.microsoft.com/en-us/library/Dd742780(v=VS.85).aspx">CreateCompatibleRenderTarget</a> method to create an <b>ID2D1BitmapRenderTarget</b> and uses it to  draw a grid pattern. The grid pattern is used as the source of an <a href="https://msdn.microsoft.com/22b14ffa-14cb-4e4d-bf80-7d81e4ae9ee4">ID2D1BitmapBrush</a>.


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




<a href="https://msdn.microsoft.com/en-us/library/Dd742780(v=VS.85).aspx">CreateCompatibleRenderTarget</a>



<a href="https://msdn.microsoft.com/93141743-c11d-40b4-83c5-07c9066836c7">ID2D1Factory::CreateWicBitmapRenderTarget</a>



<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

