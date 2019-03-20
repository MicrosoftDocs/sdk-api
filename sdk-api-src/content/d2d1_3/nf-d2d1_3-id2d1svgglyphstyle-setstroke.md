---
UID: NF:d2d1_3.ID2D1SvgGlyphStyle.SetStroke
title: ID2D1SvgGlyphStyle::SetStroke (d2d1_3.h)
author: windows-sdk-content
description: Provides values to an SVG glyph for stroke properties. The brush with opacity set to 1 is used as the 'context-stroke'. The opacity of the brush is used as the 'context-stroke-opacity' value.
old-location: direct2d\id2d1svgglyphstyle_setstroke.htm
tech.root: Direct2D
ms.assetid: 3C7734DF-3EA6-43A8-8913-8D174ABAAA56
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID2D1SvgGlyphStyle interface [Direct2D],SetStroke method, ID2D1SvgGlyphStyle.SetStroke, ID2D1SvgGlyphStyle::SetStroke, SetStroke, SetStroke method [Direct2D], SetStroke method [Direct2D],ID2D1SvgGlyphStyle interface, d2d1_3/ID2D1SvgGlyphStyle::SetStroke, direct2d.id2d1svgglyphstyle_setstroke
ms.topic: method
req.header: d2d1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - ID2D1SvgGlyphStyle.SetStroke
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1SvgGlyphStyle::SetStroke


## -description


Provides values to an SVG glyph for stroke properties. The brush with opacity
        set to 1 is used as the 'context-stroke'. The opacity of the brush is used as
        the 'context-stroke-opacity' value.


## -parameters




### -param brush [in, optional]

Type: <b><a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>*</b>

Describes how the stroke is painted. A null brush will cause the context-stroke value to be none.


### -param strokeWidth

Type: <b>FLOAT</b>

Specifies the 'context-value' for the 'stroke-width' property.


### -param dashes [in, optional]

Type: <b>const FLOAT*</b>

Specifies the 'context-value' for the 'stroke-dasharray'
          property. A null value will cause the stroke-dasharray to be set to 'none'.


### -param dashesCount

Type: <b>UINT32</b>

The the number of dashes in the dash array.


### -param dashOffset

Type: <b>FLOAT</b>

Specifies the 'context-value' for the 'stroke-dashoffset' property.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -see-also




<a href="https://msdn.microsoft.com/FE01771A-D82A-4610-8014-E0C0C0C5402E">ID2D1SvgGlyphStyle</a>
 

 

