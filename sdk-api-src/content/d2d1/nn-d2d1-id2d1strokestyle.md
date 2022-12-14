---
UID: NN:d2d1.ID2D1StrokeStyle
title: ID2D1StrokeStyle (d2d1.h)
description: Describes the caps, miter limit, line join, and dash information for a stroke. (ID2D1StrokeStyle)
helpviewer_keywords: ["ID2D1StrokeStyle","ID2D1StrokeStyle interface [Direct2D]","ID2D1StrokeStyle interface [Direct2D]","described","d2d1/ID2D1StrokeStyle","direct2d.ID2D1StrokeStyle"]
old-location: direct2d\ID2D1StrokeStyle.htm
tech.root: Direct2D
ms.assetid: 2cdf66dc-f34f-4132-8c06-7464648d3cef
ms.date: 12/05/2018
ms.keywords: ID2D1StrokeStyle, ID2D1StrokeStyle interface [Direct2D], ID2D1StrokeStyle interface [Direct2D],described, d2d1/ID2D1StrokeStyle, direct2d.ID2D1StrokeStyle
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
 - ID2D1StrokeStyle
 - d2d1/ID2D1StrokeStyle
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
 - ID2D1StrokeStyle
---

# ID2D1StrokeStyle interface


## -description

Describes the caps, miter limit, line join, and dash information for a stroke.

## -inheritance

The <b>ID2D1StrokeStyle</b> interface inherits from <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1resource">ID2D1Resource</a>. <b>ID2D1StrokeStyle</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

<h3><a id="Creating_ID2D1StrokeStyle_Objects"></a><a id="creating_id2d1strokestyle_objects"></a><a id="CREATING_ID2D1STROKESTYLE_OBJECTS"></a>Creating ID2D1StrokeStyle Objects</h3>
To create a stroke style, use the <a href="/windows/win32/Direct2D/id2d1factory-createstrokestyle">ID2D1Factory::CreateStrokeStyle</a> method.

A stroke style is a device-independent resource; you can create it once then retain it for the life of your application. For more information about resources, see the <a href="/windows/win32/Direct2D/resources-and-resource-domains">Resources Overview</a>.


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

## -see-also

<a href="/windows/win32/Direct2D/id2d1factory-createstrokestyle">ID2D1Factory::CreateStrokeStyle</a>



<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1resource">ID2D1Resource</a>

