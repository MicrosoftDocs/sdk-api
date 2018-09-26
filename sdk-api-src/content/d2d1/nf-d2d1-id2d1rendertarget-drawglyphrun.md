---
UID: NF:d2d1.ID2D1RenderTarget.DrawGlyphRun
title: ID2D1RenderTarget::DrawGlyphRun
author: windows-sdk-content
description: Draws the specified glyphs.
old-location: direct2d\ID2D1RenderTarget_DrawGlyphRun.htm
tech.root: direct2d
ms.assetid: 064ede6c-139c-4160-9c50-460179d46f97
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: DrawGlyphRun, DrawGlyphRun method [Direct2D], DrawGlyphRun method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],DrawGlyphRun method, ID2D1RenderTarget.DrawGlyphRun, ID2D1RenderTarget::DrawGlyphRun, d2d1/ID2D1RenderTarget::DrawGlyphRun, direct2d.ID2D1RenderTarget_DrawGlyphRun
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
 - ID2D1RenderTarget.DrawGlyphRun
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget::DrawGlyphRun


## -description


Draws the specified glyphs.


## -parameters




### -param baselineOrigin

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The origin, in device-independent pixels, of the glyphs' baseline.


### -param glyphRun [in]

Type: <b>const <a href="https://msdn.microsoft.com/2997d63f-8d33-44c3-9617-cfffe5f61f7d">DWRITE_GLYPH_RUN</a>*</b>

The glyphs to render.


### -param foregroundBrush [in]

Type: <b><a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>*</b>

The brush used to paint the specified glyphs.


### -param measuringMode

Type: <b><a href="https://msdn.microsoft.com/99e89754-8bc2-457d-bfdb-a3c9ccfe00c1">DWRITE_MEASURING_MODE</a></b>

A value that indicates how glyph metrics are used to measure text when it is formatted.  The default value is <a href="https://msdn.microsoft.com/99e89754-8bc2-457d-bfdb-a3c9ccfe00c1">DWRITE_MEASURING_MODE_NATURAL</a>. 


## -returns



This method does not return a value.




## -remarks



This method doesn't return an error code if it fails. To determine whether a drawing operation (such as <b>DrawGlyphRun</b>) failed, check the result returned by the <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">ID2D1RenderTarget::EndDraw</a> or <a href="https://msdn.microsoft.com/3ad9c966-85f5-4ddb-a8c1-aefcba533509">ID2D1RenderTarget::Flush</a> methods. 




## -see-also




<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

