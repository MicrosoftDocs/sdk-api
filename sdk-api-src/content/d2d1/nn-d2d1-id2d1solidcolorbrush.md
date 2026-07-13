---
UID: NN:d2d1.ID2D1SolidColorBrush
title: ID2D1SolidColorBrush (d2d1.h)
description: Paints an area with a solid color.
helpviewer_keywords: ["ID2D1SolidColorBrush","ID2D1SolidColorBrush interface [Direct2D]","ID2D1SolidColorBrush interface [Direct2D]","described","d2d1/ID2D1SolidColorBrush","direct2d.ID2D1SolidColorBrush"]
old-location: direct2d\ID2D1SolidColorBrush.htm
tech.root: Direct2D
ms.assetid: a15c2696-3122-461e-806e-2195a50a3e92
ms.date: 12/05/2018
ms.keywords: ID2D1SolidColorBrush, ID2D1SolidColorBrush interface [Direct2D], ID2D1SolidColorBrush interface [Direct2D],described, d2d1/ID2D1SolidColorBrush, direct2d.ID2D1SolidColorBrush
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
 - ID2D1SolidColorBrush
 - d2d1/ID2D1SolidColorBrush
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
 - ID2D1SolidColorBrush
---

# ID2D1SolidColorBrush interface


## -description

Paints an area with a solid color.

## -inheritance

The <b>ID2D1SolidColorBrush</b> interface inherits from <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>. <b>ID2D1SolidColorBrush</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

<h3><a id="Creating_ID2D1SolidColorBrush_Objects"></a><a id="creating_id2d1solidcolorbrush_objects"></a><a id="CREATING_ID2D1SOLIDCOLORBRUSH_OBJECTS"></a>Creating ID2D1SolidColorBrush Objects</h3>

To create a solid color brush, use the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)">ID2D1RenderTarget::CreateSolidColorBrush</a> method of the render target on which the brush will be used. The brush can only be used with the render target that created it or with the compatible targets for that render target.


A solid color brush is a device-dependent resource. (For more information about resources, see <a href="/windows/win32/Direct2D/resources-and-resource-domains">Resources Overview</a>.)


## Examples

The following example uses the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)">CreateSolidColorBrush</a> method of a render target (<i>m_pRenderTarget</i>) to create two brushes. The example uses a predefined color (black) to specify the color of the first brush. It uses a hexadecimal color value (yellow) to specify the color of the second brush.



```cpp
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
        &m_pBlackBrush
        );
}

// Create a solid color brush with its rgb value 0x9ACD32.
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0x9ACD32, 1.0f)),  
        &m_pYellowGreenBrush
        );
}

```


The next code example calls the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)">FillRectangle</a> method to paint the interior of a rectangle with the yellow green brush and the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)">DrawRectangle</a> method to paint the outline of the rectangle with the black brush:


```cpp
m_pRenderTarget->FillRectangle(&rcBrushRect, m_pYellowGreenBrush);
m_pRenderTarget->DrawRectangle(&rcBrushRect, m_pBlackBrush, 1, NULL);

```


These examples produce the output shown in the following illustration.

<img alt="Illustration of a rectangle filled with a solid, yellow-green color" src="./images/brushes_ovw_solidcolor.png"/>

<div class="code"></div>

## -see-also

<a href="/windows/win32/Direct2D/direct2d-brushes-overview">Brushes Overview</a>



<a href="/windows/win32/api/d2d1helper/nl-d2d1helper-colorf">ColorF</a>



<a href="/windows/win32/Direct2D/how-to-create-a-solid-color-brush">How to Create a Solid Color Brush</a>



<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>

