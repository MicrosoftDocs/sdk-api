---
UID: NF:dwrite.IDWriteFontFace.GetGlyphRunOutline
title: IDWriteFontFace::GetGlyphRunOutline
author: windows-sdk-content
description: Computes the outline of a run of glyphs by calling back to the outline sink interface.
old-location: directwrite\IDWriteFontFace_GetGlyphRunOutline.htm
old-project: DirectWrite
ms.assetid: 06edbd68-efc3-44e5-875c-a84488fca252
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: GetGlyphRunOutline, GetGlyphRunOutline method [Direct Write], GetGlyphRunOutline method [Direct Write],IDWriteFontFace interface, IDWriteFontFace interface [Direct Write],GetGlyphRunOutline method, IDWriteFontFace.GetGlyphRunOutline, IDWriteFontFace::GetGlyphRunOutline, directwrite.IDWriteFontFace_GetGlyphRunOutline, dwrite/IDWriteFontFace::GetGlyphRunOutline
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dwrite.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFontFace.GetGlyphRunOutline
product: Windows
targetos: Windows
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDWriteFontFace::GetGlyphRunOutline


## -description


 Computes the outline of a run of glyphs by calling back to the outline sink interface.


## -parameters




### -param emSize

Type: <b>FLOAT</b>

The logical size of the font in DIP units. A DIP ("device-independent pixel") equals 1/96 inch.


### -param glyphIndices [in]

Type: <b>const UINT16*</b>

An array of glyph indices. The glyphs are in logical order and the advance direction depends on the <i>isRightToLeft</i> parameter. The array must be allocated and be able to contain the number of elements specified by <i>glyphCount</i>.


### -param glyphAdvances [in, optional]

Type: <b>const FLOAT*</b>

An optional array of glyph advances in DIPs. The advance of a glyph is the amount to advance the position (in the direction of the baseline) after drawing the glyph. <i>glyphAdvances</i> contains the number of elements specified by <i>glyphCount</i>.


### -param glyphOffsets [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/f5a231c0-78df-4fe0-99a8-81fcad517cda">DWRITE_GLYPH_OFFSET</a>*</b>

An optional array of glyph offsets, each of which specifies the offset along the baseline and offset perpendicular to the baseline of a glyph relative to the current pen position.   <i>glyphOffsets</i> contains the number of elements specified by <i>glyphCount</i>.


### -param glyphCount

Type: <b>UINT32</b>

The number of glyphs in the run.


### -param isSideways

Type: <b>BOOL</b>

If <b>TRUE</b>, the ascender of the glyph runs alongside the baseline. If <b>FALSE</b>, the glyph ascender runs perpendicular to the baseline. For example, an English alphabet on a vertical baseline would have <i>isSideways</i> set to <b>FALSE</b>.

A client can render a vertical run by setting <i>isSideways</i> to <b>TRUE</b> and rotating the resulting geometry 90 degrees to the
     right using a transform. The <i>isSideways</i> and <i>isRightToLeft</i> parameters cannot both be true.


### -param isRightToLeft

Type: <b>BOOL</b>

The visual order of the glyphs. If this parameter is <b>FALSE</b>, then glyph advances are from left to right. If <b>TRUE</b>, the advance direction is right to left. By default, the advance direction
     is left to right.


### -param geometrySink

Type: <b><a href="https://msdn.microsoft.com/78bd0236-459f-4c89-94d8-d2ca1e51af5e">IDWriteGeometrySink</a>*</b>

A pointer to the interface that is called back to perform outline drawing operations.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1b6bb9e2-cf01-413c-9ee8-42bb0f703ce8">IDWriteFontFace</a>
 

 

