---
UID: NF:d2d1_1.ID2D1DeviceContext.DrawGlyphRun
title: ID2D1DeviceContext::DrawGlyphRun
author: windows-sdk-content
description: Draws a series of glyphs to the device context.
old-location: direct2d\id2d1devicecontext_drawglyphrun.htm
tech.root: direct2d
ms.assetid: a169604c-64d6-401f-83f5-fb322230e110
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: DrawGlyphRun, DrawGlyphRun method [Direct2D], DrawGlyphRun method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],DrawGlyphRun method, ID2D1DeviceContext.DrawGlyphRun, ID2D1DeviceContext::DrawGlyphRun, d2d1_1/ID2D1DeviceContext::DrawGlyphRun, direct2d.id2d1devicecontext_drawglyphrun
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - ID2D1DeviceContext.DrawGlyphRun
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext::DrawGlyphRun


## -description


Draws a series of glyphs to the device context.


## -parameters




### -param baselineOrigin

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

Origin of first glyph in the series.


### -param glyphRun [in]

Type: <b>const <a href="https://msdn.microsoft.com/2997d63f-8d33-44c3-9617-cfffe5f61f7d">DWRITE_GLYPH_RUN</a>*</b>

The glyphs to render.


### -param glyphRunDescription [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/0fb25253-274a-42b7-8491-525d0550ce39">DWRITE_GLYPH_RUN_DESCRIPTION</a>*</b>

Supplementary glyph series information.


### -param foregroundBrush [in]

Type: <b><a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>*</b>

The brush that defines the text color.


### -param measuringMode

Type: <b><a href="https://msdn.microsoft.com/99e89754-8bc2-457d-bfdb-a3c9ccfe00c1">DWRITE_MEASURING_MODE</a></b>

The measuring mode of the glyph series, used to determine the advances and offsets. The default value is DWRITE_MEASURING_MODE_NATURAL.


## -returns



This method does not return a value.




## -remarks



The <i>glyphRunDescription</i> is ignored when rendering, but can be useful for printing and serialization of rendering commands, such as to an XPS or SVG file. This extends <a href="https://msdn.microsoft.com/064ede6c-139c-4160-9c50-460179d46f97">ID2D1RenderTarget::DrawGlyphRun</a>, which lacked the glyph run description.




## -see-also




<a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>



<a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>



<a href="https://msdn.microsoft.com/064ede6c-139c-4160-9c50-460179d46f97">ID2D1RenderTarget::DrawGlyphRun</a>
 

 

