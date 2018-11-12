---
UID: NF:dwrite_2.IDWriteTextRenderer1.DrawGlyphRun
title: IDWriteTextRenderer1::DrawGlyphRun
author: windows-sdk-content
description: IDWriteTextLayout::Draw calls this function to instruct the client to render a run of glyphs.
old-location: directwrite\idwritetextrenderer1_drawglyphrun.htm
tech.root: DirectWrite
ms.assetid: b5f24a23-fb81-90f3-85de-55d8599a18d3
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: DrawGlyphRun, DrawGlyphRun method [Direct Write], DrawGlyphRun method [Direct Write],IDWriteTextRenderer1 interface, IDWriteTextRenderer1 interface [Direct Write],DrawGlyphRun method, IDWriteTextRenderer1.DrawGlyphRun, IDWriteTextRenderer1::DrawGlyphRun, directwrite.idwritetextrenderer1_drawglyphrun, dwrite_2/IDWriteTextRenderer1::DrawGlyphRun
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dwrite_2.h
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
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteTextRenderer1.DrawGlyphRun
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextRenderer1::DrawGlyphRun


## -description


 IDWriteTextLayout::<a href="https://msdn.microsoft.com/cbaa3341-e43a-4d3f-89c7-dda758a63e7d">Draw</a> calls this function to instruct the client to
     render a run of glyphs.


## -parameters




### -param clientDrawingContext

Type: <b>void*</b>

The application-defined drawing context passed to 
     <a href="https://msdn.microsoft.com/8d92a7c3-4804-47f6-bfca-5322be119cbb">IDWriteTextLayout::Draw</a>.


### -param baselineOriginX

Type: <b>FLOAT</b>

The pixel location (X-coordinate) at the baseline origin of the glyph run.


### -param baselineOriginY

Type: <b>FLOAT</b>

The pixel location (Y-coordinate) at the baseline origin of the glyph run.


### -param orientationAngle

Type: <b><a href="https://msdn.microsoft.com/BD9D0C11-B286-4E4A-B641-1DB9F75803B0">DWRITE_GLYPH_ORIENTATION_ANGLE</a></b>

Orientation of the glyph run.


### -param measuringMode

Type: <b><a href="https://msdn.microsoft.com/99e89754-8bc2-457d-bfdb-a3c9ccfe00c1">DWRITE_MEASURING_MODE</a></b>

The measuring method for glyphs in the run, used with the other properties to determine the rendering mode.


### -param glyphRun [in]

Type: <b>const <a href="https://msdn.microsoft.com/2997d63f-8d33-44c3-9617-cfffe5f61f7d">DWRITE_GLYPH_RUN</a>*</b>

Pointer to the glyph run instance to render. 


### -param glyphRunDescription [in]

Type: <b>const <a href="https://msdn.microsoft.com/0fb25253-274a-42b7-8491-525d0550ce39">DWRITE_GLYPH_RUN_DESCRIPTION</a>*</b>

A pointer to the glyph run description instance which contains properties of the characters 
     associated with this run.


### -param clientDrawingEffect

Type: <b>IUnknown*</b>

Application-defined drawing effects for the glyphs to render. Usually this argument represents effects such as the foreground brush filling the interior of text.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <a href="https://msdn.microsoft.com/8d92a7c3-4804-47f6-bfca-5322be119cbb">IDWriteTextLayout::Draw</a> function calls this callback function with all the information about glyphs to render. The application implements this callback by mostly delegating the call to the underlying platform's graphics API such as <a href="https://msdn.microsoft.com/03b3b91c-9751-4f8d-af24-85067f06930b">Direct2D</a> to draw glyphs on the drawing context. An application that uses GDI can implement this callback in terms of the <a href="https://msdn.microsoft.com/d766d2d1-6be7-468a-a10e-c7cab421b9a7">IDWriteBitmapRenderTarget::DrawGlyphRun</a> method.




## -see-also




<a href="https://msdn.microsoft.com/A8C39C54-AF98-4A27-9BCF-9C132F4CD3B1">IDWriteTextRenderer1</a>
 

 

