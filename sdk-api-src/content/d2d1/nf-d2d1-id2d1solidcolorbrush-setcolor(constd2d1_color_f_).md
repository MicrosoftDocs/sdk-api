---
UID: NF:d2d1.ID2D1SolidColorBrush.SetColor(constD2D1_COLOR_F&)
title: ID2D1SolidColorBrush::SetColor(const D2D1_COLOR_F &) (d2d1.h)
description: Specifies the color of this solid-color brush.
helpviewer_keywords: ["ID2D1SolidColorBrush interface [Direct2D]","SetColor method","ID2D1SolidColorBrush.SetColor","ID2D1SolidColorBrush.SetColor(const D2D1_COLOR_F &)","ID2D1SolidColorBrush::SetColor","ID2D1SolidColorBrush::SetColor(const D2D1_COLOR_F &)","SetColor","SetColor method [Direct2D]","SetColor method [Direct2D]","ID2D1SolidColorBrush interface","d2d1/ID2D1SolidColorBrush::SetColor","direct2d.ID2D1SolidColorBrush_SetColor_ref_COLOR_F"]
old-location: direct2d\ID2D1SolidColorBrush_SetColor_ref_COLOR_F.htm
tech.root: Direct2D
ms.assetid: f11d3528-e444-4a55-b522-0dad6ddcd735
ms.date: 12/05/2018
ms.keywords: ID2D1SolidColorBrush interface [Direct2D],SetColor method, ID2D1SolidColorBrush.SetColor, ID2D1SolidColorBrush.SetColor(const D2D1_COLOR_F &), ID2D1SolidColorBrush::SetColor, ID2D1SolidColorBrush::SetColor(const D2D1_COLOR_F &), SetColor, SetColor method [Direct2D], SetColor method [Direct2D],ID2D1SolidColorBrush interface, d2d1/ID2D1SolidColorBrush::SetColor, direct2d.ID2D1SolidColorBrush_SetColor_ref_COLOR_F
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
 - ID2D1SolidColorBrush::SetColor
 - d2d1/ID2D1SolidColorBrush::SetColor
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
 - ID2D1SolidColorBrush.SetColor
---

# ID2D1SolidColorBrush::SetColor(const D2D1_COLOR_F &)


## -description

Specifies the color of this solid-color brush.

## -parameters

### -param color [ref]

Type: <b>const <a href="/windows/win32/Direct2D/d2d1-color-f">D2D1_COLOR_F</a></b>

The color of this solid-color brush.

## -remarks

To help create colors, Direct2D provides the <a href="/windows/win32/api/d2d1helper/nl-d2d1helper-colorf">ColorF</a> class. It offers several helper methods for creating colors and provides a set or predefined colors. 


## Examples

The following code shows  how to use this method.


```cpp
        m_pSolidColorBrush->SetColor(
            D2D1::ColorF(
                0.0f,
                intensity,
                1.0f - intensity
                ));

        hr = m_pRealization->Fill(
                m_pRT,
                m_pSolidColorBrush,
                m_useRealizations ?
                    REALIZATION_RENDER_MODE_DEFAULT :
                    REALIZATION_RENDER_MODE_FORCE_UNREALIZED
                );

```

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush">ID2D1SolidColorBrush</a>

