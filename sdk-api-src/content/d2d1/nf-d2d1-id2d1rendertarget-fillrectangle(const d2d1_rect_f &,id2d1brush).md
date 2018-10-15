---
UID: NF:d2d1.ID2D1RenderTarget.FillRectangle(const D2D1_RECT_F &,ID2D1Brush)
title: ID2D1RenderTarget::FillRectangle(const D2D1_RECT_F &,ID2D1Brush)
author: windows-sdk-content
description: Paints the interior of the specified rectangle.
old-location: direct2d\ID2D1RenderTarget_FillRectangle_ref_D2D_RECT_F_ptr_ID2D1Brush.htm
tech.root: direct2d
ms.assetid: b5d7ca28-0751-4799-8480-f221fd5fe276
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: FillRectangle, FillRectangle method [Direct2D], FillRectangle method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],FillRectangle method, ID2D1RenderTarget.FillRectangle, ID2D1RenderTarget.FillRectangle(const D2D1_RECT_F &,ID2D1Brush), ID2D1RenderTarget::FillRectangle, ID2D1RenderTarget::FillRectangle(const D2D1_RECT_F &,ID2D1Brush), d2d1/ID2D1RenderTarget::FillRectangle, direct2d.ID2D1RenderTarget_FillRectangle_ref_D2D_RECT_F_ptr_ID2D1Brush
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
 - ID2D1RenderTarget.FillRectangle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget::FillRectangle(const D2D1_RECT_F &,ID2D1Brush)


## -description


Paints the interior of the specified rectangle.


## -parameters




### -param rect [ref]

Type: <b>const <a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a></b>

The dimension of the rectangle to paint, in device-independent pixels.


### -param brush [in]

Type: <b><a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>*</b>

The brush used to paint the rectangle's interior.


## -returns



This method does not return a value.




## -remarks



This method doesn't return an error code if it fails. To determine whether a drawing operation (such as <a href="https://msdn.microsoft.com/08e498f9-b564-4da6-ba9b-bff08964ce08">FillRectangle</a>) failed, check the result returned by the <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">ID2D1RenderTarget::EndDraw</a> or <a href="https://msdn.microsoft.com/3ad9c966-85f5-4ddb-a8c1-aefcba533509">ID2D1RenderTarget::Flush</a> methods. 


#### Examples

The following example uses an <a href="https://msdn.microsoft.com/860342cc-989c-4432-b879-07f3da07d50a">ID2D1HwndRenderTarget</a> to draw and fill several rectangles. This example produces the output shown in the following illustration.

<img alt="Illustration of two rectangles on a grid background" src="images/drawrectangleexample_small.png"/>

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// This method discards device-specific
// resources if the Direct3D device dissapears during execution and
// recreates the resources the next time it's invoked.
HRESULT DemoApp::OnRender()
{
    HRESULT hr = S_OK;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        m_pRenderTarget-&gt;BeginDraw();

        m_pRenderTarget-&gt;SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget-&gt;Clear(D2D1::ColorF(D2D1::ColorF::White));

        D2D1_SIZE_F rtSize = m_pRenderTarget-&gt;GetSize();

        // Draw a grid background.
        int width = static_cast&lt;int&gt;(rtSize.width);
        int height = static_cast&lt;int&gt;(rtSize.height);

        for (int x = 0; x &lt; width; x += 10)
        {
            m_pRenderTarget-&gt;DrawLine(
                D2D1::Point2F(static_cast&lt;FLOAT&gt;(x), 0.0f),
                D2D1::Point2F(static_cast&lt;FLOAT&gt;(x), rtSize.height),
                m_pLightSlateGrayBrush,
                0.5f
                );
        }

        for (int y = 0; y &lt; height; y += 10)
        {
            m_pRenderTarget-&gt;DrawLine(
                D2D1::Point2F(0.0f, static_cast&lt;FLOAT&gt;(y)),
                D2D1::Point2F(rtSize.width, static_cast&lt;FLOAT&gt;(y)),
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
        m_pRenderTarget-&gt;FillRectangle(&amp;rectangle1, m_pLightSlateGrayBrush);

        // Draw the outline of a rectangle.
        m_pRenderTarget-&gt;DrawRectangle(&amp;rectangle2, m_pCornflowerBlueBrush);

        hr = m_pRenderTarget-&gt;EndDraw();
    }

    if (hr == D2DERR_RECREATE_TARGET)
    {
        hr = S_OK;
        DiscardDeviceResources();
    }

    return hr;
}
</pre>
</td>
</tr>
</table></span></div>
For a related tutorial, see <a href="https://msdn.microsoft.com/a627523e-417a-40cd-82c0-4f0380a3a0b1">Creating a Simple Direct2D Application</a>. 

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/a627523e-417a-40cd-82c0-4f0380a3a0b1">Creating a Simple Direct2D Application</a>



<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

