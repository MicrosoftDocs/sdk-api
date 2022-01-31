---
UID: NE:d2d1.D2D1_DASH_STYLE
title: D2D1_DASH_STYLE (d2d1.h)
description: Describes the sequence of dashes and gaps in a stroke.
helpviewer_keywords: ["D2D1_DASH_STYLE","D2D1_DASH_STYLE enumeration [Direct2D]","D2D1_DASH_STYLE_CUSTOM","D2D1_DASH_STYLE_DASH","D2D1_DASH_STYLE_DASH_DOT","D2D1_DASH_STYLE_DASH_DOT_DOT","D2D1_DASH_STYLE_DOT","D2D1_DASH_STYLE_SOLID","d2d1/D2D1_DASH_STYLE","d2d1/D2D1_DASH_STYLE_CUSTOM","d2d1/D2D1_DASH_STYLE_DASH","d2d1/D2D1_DASH_STYLE_DASH_DOT","d2d1/D2D1_DASH_STYLE_DASH_DOT_DOT","d2d1/D2D1_DASH_STYLE_DOT","d2d1/D2D1_DASH_STYLE_SOLID","direct2d.D2D1_DASH_STYLE"]
old-location: direct2d\D2D1_DASH_STYLE.htm
tech.root: Direct2D
ms.assetid: 0c1807e3-51e6-440a-bd80-9b43ed7a39f5
ms.date: 12/05/2018
ms.keywords: D2D1_DASH_STYLE, D2D1_DASH_STYLE enumeration [Direct2D], D2D1_DASH_STYLE_CUSTOM, D2D1_DASH_STYLE_DASH, D2D1_DASH_STYLE_DASH_DOT, D2D1_DASH_STYLE_DASH_DOT_DOT, D2D1_DASH_STYLE_DOT, D2D1_DASH_STYLE_SOLID, d2d1/D2D1_DASH_STYLE, d2d1/D2D1_DASH_STYLE_CUSTOM, d2d1/D2D1_DASH_STYLE_DASH, d2d1/D2D1_DASH_STYLE_DASH_DOT, d2d1/D2D1_DASH_STYLE_DASH_DOT_DOT, d2d1/D2D1_DASH_STYLE_DOT, d2d1/D2D1_DASH_STYLE_SOLID, direct2d.D2D1_DASH_STYLE
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_DASH_STYLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_DASH_STYLE
 - d2d1/D2D1_DASH_STYLE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_DASH_STYLE
---

# D2D1_DASH_STYLE enumeration


## -description

Describes the sequence of dashes and gaps in a stroke.

## -enum-fields

### -field D2D1_DASH_STYLE_SOLID:0

A solid line with no breaks.

### -field D2D1_DASH_STYLE_DASH:1

A dash followed by a gap of equal length. The dash and the gap are each twice as long as the stroke thickness.

The equivalent dash  array for  <b>D2D1_DASH_STYLE_DASH</b> is {2, 2}.

### -field D2D1_DASH_STYLE_DOT:2

A dot followed by a longer gap.

The equivalent dash  array for  <b>D2D1_DASH_STYLE_DOT</b> is {0, 2}.

### -field D2D1_DASH_STYLE_DASH_DOT:3

A dash, followed by a gap, followed by a dot, followed by another gap.

The equivalent dash array for  <b>D2D1_DASH_STYLE_DASH_DOT</b> is {2, 2, 0, 2}.

### -field D2D1_DASH_STYLE_DASH_DOT_DOT:4

A dash, followed by a gap, followed by a dot, followed by another gap, followed by another dot, followed by another gap.

The equivalent dash array for  <b>D2D1_DASH_STYLE_DASH_DOT_DOT</b> is {2, 2, 0, 2, 0, 2}.

### -field D2D1_DASH_STYLE_CUSTOM:5

The dash pattern is specified by an array of floating-point values.

### -field D2D1_DASH_STYLE_FORCE_DWORD:0xffffffff

## -remarks

The following illustration shows several available dash styles. 
      

<img alt="Illustration of available dash styles" src="./images/StrokeStyle_DashStyle.png"/>

## Examples

The following example creates a stroke that uses a custom dash pattern.
        
        


```cpp
// Dash array for dashStyle D2D1_DASH_STYLE_CUSTOM
float dashes[] = {1.0f, 2.0f, 2.0f, 3.0f, 2.0f, 2.0f};

// Stroke Style with Dash Style -- Custom
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreateStrokeStyle(
        D2D1::StrokeStyleProperties(
            D2D1_CAP_STYLE_FLAT,
            D2D1_CAP_STYLE_FLAT,
            D2D1_CAP_STYLE_ROUND,
            D2D1_LINE_JOIN_MITER,
            10.0f,
            D2D1_DASH_STYLE_CUSTOM,
            0.0f),
        dashes,
        ARRAYSIZE(dashes),
        &m_pStrokeStyleCustomOffsetZero
        );
}

```


The next example uses the stroke style when drawing a line.


```cpp
m_pRenderTarget->DrawLine(
    D2D1::Point2F(0, 310),
    D2D1::Point2F(200, 310),
    m_pCornflowerBlueBrush,
    10.0f,
    m_pStrokeStyleCustomOffsetZero
    );

```

