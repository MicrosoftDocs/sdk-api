---
UID: NF:d2d1_1.ID2D1CommandSink.DrawGlyphRun
title: ID2D1CommandSink::DrawGlyphRun
author: windows-sdk-content
description: Indicates the glyphs to be drawn.
old-location: direct2d\id2d1commandsink_drawglyphrun.htm
tech.root: direct2d
ms.assetid: 5b40a999-0046-458e-b7bc-95037d73833c
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: DrawGlyphRun, DrawGlyphRun method [Direct2D], DrawGlyphRun method [Direct2D],ID2D1CommandSink interface, ID2D1CommandSink interface [Direct2D],DrawGlyphRun method, ID2D1CommandSink.DrawGlyphRun, ID2D1CommandSink::DrawGlyphRun, d2d1_1/ID2D1CommandSink::DrawGlyphRun, direct2d.id2d1commandsink_drawglyphrun
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
 - ID2D1CommandSink.DrawGlyphRun
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1CommandSink::DrawGlyphRun


## -description


Indicates the glyphs to be drawn.


## -parameters




### -param baselineOrigin

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The upper left corner of the baseline.


### -param glyphRun [in]

Type: <b>const <a href="https://msdn.microsoft.com/2997d63f-8d33-44c3-9617-cfffe5f61f7d">DWRITE_GLYPH_RUN</a>*</b>

The glyphs to render.


### -param glyphRunDescription [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/0fb25253-274a-42b7-8491-525d0550ce39">DWRITE_GLYPH_RUN_DESCRIPTION</a>*</b>

Additional non-rendering information about the glyphs.


### -param foregroundBrush [in]

Type: <b><a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>*</b>

The brush used to fill the glyphs.


### -param measuringMode

Type: <b><a href="https://msdn.microsoft.com/99e89754-8bc2-457d-bfdb-a3c9ccfe00c1">DWRITE_MEASURING_MODE</a></b>

The measuring mode to apply to the glyphs.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code. 





## -remarks




<a href="https://msdn.microsoft.com/7cda7854-f9df-48d3-bc62-6aaee769e6f9">DrawText</a> and <a href="https://msdn.microsoft.com/9356071a-35ca-462a-8a77-887e63850586">DrawTextLayout</a> are broken down into glyph runs and rectangles by the time the command sink is processed. So, these methods aren't available on the command sink. Since the application may require additional callback processing when calling <b>DrawTextLayout</b>, this semantic can't be easily preserved in the command list.




## -see-also




<a href="https://msdn.microsoft.com/52e6da86-c7c6-48e7-b0ff-a54770663f14">ID2D1CommandList::Stream</a>



<a href="https://msdn.microsoft.com/4e0ce837-7f4e-4b93-8dd7-68f60cfb1105">ID2D1CommandSink</a>



<a href="https://msdn.microsoft.com/a169604c-64d6-401f-83f5-fb322230e110">ID2D1DeviceContext::DrawGlyphRun</a>
 

 

