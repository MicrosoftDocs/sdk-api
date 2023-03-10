---
UID: NF:d2d1.ID2D1RenderTarget.DrawLine
title: ID2D1RenderTarget::DrawLine (d2d1.h)
description: Draws a line between the specified points using the specified stroke style.
helpviewer_keywords: ["DrawLine","DrawLine method [Direct2D]","DrawLine method [Direct2D]","ID2D1RenderTarget interface","ID2D1RenderTarget interface [Direct2D]","DrawLine method","ID2D1RenderTarget.DrawLine","ID2D1RenderTarget::DrawLine","d2d1/ID2D1RenderTarget::DrawLine","direct2d.ID2D1RenderTarget_DrawLine"]
old-location: direct2d\ID2D1RenderTarget_DrawLine.htm
tech.root: Direct2D
ms.assetid: 7eb70308-4142-4d32-a070-9e937579b896
ms.date: 12/05/2018
ms.keywords: DrawLine, DrawLine method [Direct2D], DrawLine method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],DrawLine method, ID2D1RenderTarget.DrawLine, ID2D1RenderTarget::DrawLine, d2d1/ID2D1RenderTarget::DrawLine, direct2d.ID2D1RenderTarget_DrawLine
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
 - ID2D1RenderTarget::DrawLine
 - d2d1/ID2D1RenderTarget::DrawLine
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
 - ID2D1RenderTarget.DrawLine
---

# ID2D1RenderTarget::DrawLine


## -description

Draws a line between the specified points using the specified stroke style.

## -parameters

### -param point0

Type: <b><a href="/windows/win32/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

The start point of the line, in device-independent pixels.

### -param point1

Type: <b><a href="/windows/win32/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

The end point of the line, in device-independent pixels.

### -param brush [in]

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>*</b>

The brush used to paint the line's stroke.

### -param strokeWidth

Type: <b>FLOAT</b>

The width of the stroke, in device-independent pixels. The value must be greater than or equal to 0.0f. If this parameter isn't specified, it defaults to 1.0f. The stroke is centered on the line.

### -param strokeStyle [in, optional]

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle">ID2D1StrokeStyle</a>*</b>

The style of stroke to paint, or <b>NULL</b> to paint a solid line.

## -remarks

This method doesn't return an error code if it fails. To determine whether a drawing operation (such as <b>DrawLine</b>) failed, check the result returned by the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">ID2D1RenderTarget::EndDraw</a> or <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush">ID2D1RenderTarget::Flush</a> methods. 


## Examples

The following example uses the <b>DrawLine</b> method to create a grid that spans the width and height of the render target. The width and height information is provided by the <i>rtSize</i> variable.


```cpp
        // Draw a grid background.
        int width = static_cast<int>(rtSize.width);
        int height = static_cast<int>(rtSize.height);

        for (int x = 0; x < width; x += 10)
        {
            m_pRenderTarget->DrawLine(
                D2D1::Point2F(static_cast<FLOAT>(x), 0.0f),
                D2D1::Point2F(static_cast<FLOAT>(x), rtSize.height),
                m_pLightSlateGrayBrush,
                0.5f
                );
        }

        for (int y = 0; y < height; y += 10)
        {
            m_pRenderTarget->DrawLine(
                D2D1::Point2F(0.0f, static_cast<FLOAT>(y)),
                D2D1::Point2F(rtSize.width, static_cast<FLOAT>(y)),
                m_pLightSlateGrayBrush,
                0.5f
                );
        }

```

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>

