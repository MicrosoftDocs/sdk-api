---
UID: NF:d2d1_3.ID2D1DeviceContext4.DrawTextLayout
title: ID2D1DeviceContext4::DrawTextLayout
author: windows-sdk-content
description: Draws a text layout object. If the layout is not subsequently changed, this can be more efficient than DrawText when drawing the same layout repeatedly.
old-location: direct2d\id2d1devicecontext4_drawtextlayout.htm
tech.root: direct2d
ms.assetid: 54993EFD-A649-4613-8A9C-744FE22F7BFC
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DrawTextLayout, DrawTextLayout method [Direct2D], DrawTextLayout method [Direct2D],ID2D1DeviceContext4 interface, ID2D1DeviceContext4 interface [Direct2D],DrawTextLayout method, ID2D1DeviceContext4.DrawTextLayout, ID2D1DeviceContext4::DrawTextLayout, d2d1_3/ID2D1DeviceContext4::DrawTextLayout, direct2d.id2d1devicecontext4_drawtextlayout
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ID2D1DeviceContext4.DrawTextLayout
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext4::DrawTextLayout


## -description


Draws a text layout object. If the layout is not subsequently changed, this can be more efficient than DrawText when drawing the same layout repeatedly.


## -parameters




### -param origin

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The point, described in device-independent pixels, at which the upper-left corner of the text described by <i>textLayout</i> is drawn.


### -param textLayout [in]

Type: <b><a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a>*</b>

The formatted text to draw. Any drawing effects that do not inherit from <a href="https://msdn.microsoft.com/8f19e74a-f010-4082-a4da-d1dc3cfe3192">ID2D1Resource</a> are ignored. If there are drawing effects that inherit from <b>ID2D1Resource</b> that are not brushes, this method fails and the render target is put in an error state. 


### -param defaultFillBrush [in, optional]

Type: <b><a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>*</b>

The brush used to paint the text.


### -param svgGlyphStyle [in, optional]

Type: <b><a href="https://msdn.microsoft.com/FE01771A-D82A-4610-8014-E0C0C0C5402E">ID2D1SvgGlyphStyle</a>*</b>

The values for context-fill, context-stroke, and context-value that are used when rendering SVG glyphs.


### -param colorPaletteIndex

Type: <b>UINT32</b>

The index used to select a color palette within a color font.


### -param options

Type: <b><a href="https://msdn.microsoft.com/30f5be4a-83c2-4039-8e09-00e842fc5eb2">D2D1_DRAW_TEXT_OPTIONS</a></b>

A value that indicates whether the text should be snapped to pixel boundaries and whether the text should be clipped to the layout rectangle. 
            The default value is <a href="https://msdn.microsoft.com/30f5be4a-83c2-4039-8e09-00e842fc5eb2">D2D1_DRAW_TEXT_OPTIONS_NONE</a>, 
            which indicates that text should be snapped to pixel boundaries and it should not be clipped to the layout rectangle.
          


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/59E1F73B-BAD9-4826-BF5B-435E760CC546">ID2D1DeviceContext4</a>
 

 

