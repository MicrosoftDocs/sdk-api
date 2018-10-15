---
UID: NF:d2d1.ID2D1RenderTarget.DrawLine
title: ID2D1RenderTarget::DrawLine
author: windows-sdk-content
description: Draws a line between the specified points using the specified stroke style.
old-location: direct2d\ID2D1RenderTarget_DrawLine.htm
tech.root: direct2d
ms.assetid: 7eb70308-4142-4d32-a070-9e937579b896
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: DrawLine, DrawLine method [Direct2D], DrawLine method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],DrawLine method, ID2D1RenderTarget.DrawLine, ID2D1RenderTarget::DrawLine, d2d1/ID2D1RenderTarget::DrawLine, direct2d.ID2D1RenderTarget_DrawLine
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
 - ID2D1RenderTarget.DrawLine
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget::DrawLine


## -description


Draws a line between the specified points using the specified stroke style.


## -parameters




### -param point0

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The start point of the line, in device-independent pixels.


### -param point1

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The end point of the line, in device-independent pixels.


### -param brush [in]

Type: <b><a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>*</b>

The brush used to paint the line's stroke.


### -param strokeWidth

Type: <b>FLOAT</b>

The width of the stroke, in device-independent pixels. The value must be greater than or equal to 0.0f. If this parameter isn't specified, it defaults to 1.0f. The stroke is centered on the line.


### -param strokeStyle [in, optional]

Type: <b><a href="https://msdn.microsoft.com/2cdf66dc-f34f-4132-8c06-7464648d3cef">ID2D1StrokeStyle</a>*</b>

The style of stroke to paint, or <b>NULL</b> to paint a solid line.


## -returns



This method does not return a value.




## -remarks



This method doesn't return an error code if it fails. To determine whether a drawing operation (such as <b>DrawLine</b>) failed, check the result returned by the <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">ID2D1RenderTarget::EndDraw</a> or <a href="https://msdn.microsoft.com/3ad9c966-85f5-4ddb-a8c1-aefcba533509">ID2D1RenderTarget::Flush</a> methods. 


#### Examples

The following example uses the <b>DrawLine</b> method to create a grid that spans the width and height of the render target. The width and height information is provided by the <i>rtSize</i> variable.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>        // Draw a grid background.
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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

