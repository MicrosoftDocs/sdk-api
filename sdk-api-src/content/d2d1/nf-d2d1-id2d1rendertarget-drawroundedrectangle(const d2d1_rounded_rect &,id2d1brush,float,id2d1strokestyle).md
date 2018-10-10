---
UID: NF:d2d1.ID2D1RenderTarget.DrawRoundedRectangle(const D2D1_ROUNDED_RECT &,ID2D1Brush,FLOAT,ID2D1StrokeStyle)
title: ID2D1RenderTarget::DrawRoundedRectangle(const D2D1_ROUNDED_RECT &,ID2D1Brush,FLOAT,ID2D1StrokeStyle)
author: windows-sdk-content
description: Draws the outline of the specified rounded rectangle using the specified stroke style.
old-location: direct2d\ID2D1RenderTarget_DrawRoundedRectangle_ref_D2D1_ROUNDED_RECT_ptr_ID2D1Brush_FLOAT_ptr_ID2D1StrokeStyle.htm
tech.root: Direct2D
ms.assetid: 599638af-ebbb-4a45-96cf-ba3852e87237
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: DrawRoundedRectangle, DrawRoundedRectangle method [Direct2D], DrawRoundedRectangle method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],DrawRoundedRectangle method, ID2D1RenderTarget.DrawRoundedRectangle, ID2D1RenderTarget.DrawRoundedRectangle(const D2D1_ROUNDED_RECT &,ID2D1Brush,FLOAT,ID2D1StrokeStyle), ID2D1RenderTarget::DrawRoundedRectangle, ID2D1RenderTarget::DrawRoundedRectangle(const D2D1_ROUNDED_RECT &,ID2D1Brush,FLOAT,ID2D1StrokeStyle), d2d1/ID2D1RenderTarget::DrawRoundedRectangle, direct2d.ID2D1RenderTarget_DrawRoundedRectangle_ref_D2D1_ROUNDED_RECT_ptr_ID2D1Brush_FLOAT_ptr_ID2D1StrokeStyle
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
 - ID2D1RenderTarget.DrawRoundedRectangle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget::DrawRoundedRectangle(const D2D1_ROUNDED_RECT &,ID2D1Brush,FLOAT,ID2D1StrokeStyle)


## -description


Draws the outline of the specified rounded rectangle using the specified stroke style.


## -parameters




### -param roundedRect [ref]

Type: <b>const <a href="https://msdn.microsoft.com/7069ca65-170e-42fc-8c1a-849a2f25c36f">D2D1_ROUNDED_RECT</a></b>

The dimensions of the rounded rectangle to draw, in device-independent pixels.


### -param brush [in]

Type: <b><a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>*</b>

The brush used to paint the rounded rectangle's outline.


### -param strokeWidth

Type: <b>FLOAT</b>

The width of the stroke, in device-independent pixels. The value must be greater than or equal to 0.0f. If this parameter isn't specified, it defaults to 1.0f. The stroke is centered on the line.


### -param strokeStyle [in, optional]

Type: <b><a href="https://msdn.microsoft.com/2cdf66dc-f34f-4132-8c06-7464648d3cef">ID2D1StrokeStyle</a>*</b>

The style of the rounded rectangle's stroke, or <b>NULL</b> to paint a solid stroke. The default value is <b>NULL</b>.


## -returns



This method does not return a value.




## -remarks



This method doesn't return an error code if it fails. To determine whether a drawing operation (such as <a href="https://msdn.microsoft.com/d718c355-ffd8-4a7f-90f3-9a10d37a19c8">DrawRoundedRectangle</a>) failed, check the result returned by the <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">ID2D1RenderTarget::EndDraw</a> or <a href="https://msdn.microsoft.com/3ad9c966-85f5-4ddb-a8c1-aefcba533509">ID2D1RenderTarget::Flush</a> methods. 


#### Examples

The following example uses the <a href="https://msdn.microsoft.com/d718c355-ffd8-4a7f-90f3-9a10d37a19c8">DrawRoundedRectangle</a> and <a href="https://msdn.microsoft.com/9c4765b0-858f-4a20-b044-0acf87a1f131">FillRoundedRectangle</a> methods to outline and fill a rounded rectangle.  This example produces the output shown in the following illustration.

<img alt="Illustration of four rounded rectangles with different stroke styles and fills" src="images/drawroundedrectangle_scr.png"/>

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>//  Called whenever the application needs to display the client
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
        D2D1_SIZE_F renderTargetSize = m_pRenderTarget-&gt;GetSize();

        m_pRenderTarget-&gt;BeginDraw();
        m_pRenderTarget-&gt;SetTransform(D2D1::Matrix3x2F::Identity());
        m_pRenderTarget-&gt;Clear(D2D1::ColorF(D2D1::ColorF::White));

        // Paint a grid background.
        m_pRenderTarget-&gt;FillRectangle(
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
        m_pRenderTarget-&gt;DrawRoundedRectangle(roundedRect, m_pBlackBrush, 10.f);

        // Apply a translation transform.
        m_pRenderTarget-&gt;SetTransform(D2D1::Matrix3x2F::Translation(200.f, 0.f));

        // Draw the rounded rectangle again, this time with a dashed stroke.
        m_pRenderTarget-&gt;DrawRoundedRectangle(roundedRect, m_pBlackBrush, 10.f, m_pStrokeStyle);

        // Apply another translation transform.
        m_pRenderTarget-&gt;SetTransform(D2D1::Matrix3x2F::Translation(0.f, 150.f));

        // Draw, then fill the rounded rectangle.
        m_pRenderTarget-&gt;DrawRoundedRectangle(roundedRect, m_pBlackBrush, 10.f, m_pStrokeStyle);
        m_pRenderTarget-&gt;FillRoundedRectangle(roundedRect, m_pSilverBrush);

        // Apply another translation transform.
        m_pRenderTarget-&gt;SetTransform(D2D1::Matrix3x2F::Translation(200.f, 150.f));

        // Fill, then draw the rounded rectangle.
        m_pRenderTarget-&gt;FillRoundedRectangle(roundedRect, m_pSilverBrush);
        m_pRenderTarget-&gt;DrawRoundedRectangle(roundedRect, m_pBlackBrush, 10.f, m_pStrokeStyle);

        hr = m_pRenderTarget-&gt;EndDraw();

        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
    }

    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/200119a2-941c-493f-9e56-c9f306dc5322">D2D1::RoundedRect</a>



<a href="https://msdn.microsoft.com/8a68fc3f-118c-447b-856c-05417ae4ef29">How to Draw and Fill a Basic Shape</a>



<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

