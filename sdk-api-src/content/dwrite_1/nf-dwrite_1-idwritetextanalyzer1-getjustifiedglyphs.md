---
UID: NF:dwrite_1.IDWriteTextAnalyzer1.GetJustifiedGlyphs
title: IDWriteTextAnalyzer1::GetJustifiedGlyphs (dwrite_1.h)
author: windows-sdk-content
description: Fills in new glyphs for complex scripts where justification increased the advances of glyphs, such as Arabic with kashida.
old-location: directwrite\idwritetextanalyzer1_getjustifiedglyphs.htm
tech.root: DirectWrite
ms.assetid: 8F7BB9EC-90AE-48BD-A596-EAF2EDC4053F
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetJustifiedGlyphs, GetJustifiedGlyphs method [Direct Write], GetJustifiedGlyphs method [Direct Write],IDWriteTextAnalyzer1 interface, IDWriteTextAnalyzer1 interface [Direct Write],GetJustifiedGlyphs method, IDWriteTextAnalyzer1.GetJustifiedGlyphs, IDWriteTextAnalyzer1::GetJustifiedGlyphs, directwrite.idwritetextanalyzer1_getjustifiedglyphs, dwrite_1/IDWriteTextAnalyzer1::GetJustifiedGlyphs
ms.topic: method
req.header: dwrite_1.h
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
 - IDWriteTextAnalyzer1.GetJustifiedGlyphs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextAnalyzer1::GetJustifiedGlyphs


## -description


Fills in new glyphs for complex scripts where justification increased
    the advances of glyphs, such as Arabic with kashida.


## -parameters




### -param fontFace

Type: <b><a href="https://msdn.microsoft.com/1DB7156F-0578-46A0-8C96-E1E34FF4E49E">IDWriteFontFace</a>*</b>

Font face used for shaping.

May be NULL.


### -param fontEmSize

Type: <b>FLOAT</b>

Font em size used for the glyph run.


### -param scriptAnalysis

Type: <b><a href="https://msdn.microsoft.com/dafda5f6-39aa-4577-9213-898bdeddc7c2">DWRITE_SCRIPT_ANALYSIS</a></b>

Script of the text from the itemizer.


### -param textLength

Type: <b>UINT32</b>

Length of the text.


### -param glyphCount

Type: <b>UINT32</b>

Number of glyphs.


### -param maxGlyphCount

Type: <b>UINT32</b>

Maximum number of output glyphs allocated
    by caller.


### -param clusterMap [in, optional]

Type: <b>const UINT16*</b>

Clustermap produced from shaping.


### -param glyphIndices [in]

Type: <b>const UINT16*</b>

Original glyphs produced from shaping.


### -param glyphAdvances [in]

Type: <b>const FLOAT*</b>

Original glyph advances produced from shaping.


### -param justifiedGlyphAdvances [in]

Type: <b>const FLOAT*</b>

Justified glyph advances from
    <a href="https://msdn.microsoft.com/BFBFEA4A-A0D4-4114-B0AB-4338A832ECD4">IDWriteTextAnalyzer1::JustifyGlyphAdvances</a>. 


### -param justifiedGlyphOffsets [in]

Type: <b>const <a href="https://msdn.microsoft.com/f5a231c0-78df-4fe0-99a8-81fcad517cda">DWRITE_GLYPH_OFFSET</a>*</b>

Justified glyph offsets from
    <a href="https://msdn.microsoft.com/BFBFEA4A-A0D4-4114-B0AB-4338A832ECD4">IDWriteTextAnalyzer1::JustifyGlyphAdvances</a>. 


### -param glyphProperties [in]

Type: <b>const <a href="https://msdn.microsoft.com/debaa84f-8883-4117-9be0-962857b55020">DWRITE_SHAPING_GLYPH_PROPERTIES</a>*</b>

Properties of each glyph, from <a href="https://msdn.microsoft.com/9bc373b6-9161-4ffc-a942-50d97d6509c3">IDWriteTextAnalyzer::GetGlyphs</a>. 


### -param actualGlyphCount [out]

Type: <b>UINT32*</b>

The new glyph count written to the
    modified arrays, or the needed glyph count if the size is not
    large enough.


### -param modifiedClusterMap [out, optional]

Type: <b>UINT16*</b>

Updated clustermap.


### -param modifiedGlyphIndices [out]

Type: <b>UINT16*</b>

Updated glyphs with new glyphs
    inserted where needed.


### -param modifiedGlyphAdvances [out]

Type: <b>FLOAT*</b>

Updated glyph advances.


### -param modifiedGlyphOffsets [out]

Type: <b><a href="https://msdn.microsoft.com/f5a231c0-78df-4fe0-99a8-81fcad517cda">DWRITE_GLYPH_OFFSET</a>*</b>

Updated glyph offsets.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You call <b>GetJustifiedGlyphs</b> after the line has been justified, and it is per-run.

You should call <b>GetJustifiedGlyphs</b> if <a href="https://msdn.microsoft.com/CBC1DA09-6D3D-42D8-8E77-CFDBA733C228">IDWriteTextAnalyzer1::GetScriptProperties</a> returns a non-null <a href="https://msdn.microsoft.com/5210C04E-618B-4FE9-A6FC-6F0FF17A64D5">DWRITE_SCRIPT_PROPERTIES.justificationCharacter</a> for that script.

 Use  <b>GetJustifiedGlyphs</b> mainly for cursive scripts
    like Arabic. If <i>maxGlyphCount</i> is not large enough, <b>GetJustifiedGlyphs</b> returns the error
    E_NOT_SUFFICIENT_BUFFER and fills the variable  to which <i>actualGlyphCount</i>  points with
    the needed glyph count.




## -see-also




<a href="https://msdn.microsoft.com/7F79BA25-5D79-4491-82E3-F9B96DD0C37D">IDWriteTextAnalyzer1</a>



<a href="https://msdn.microsoft.com/CBC1DA09-6D3D-42D8-8E77-CFDBA733C228">IDWriteTextAnalyzer1::GetScriptProperties</a>



<a href="https://msdn.microsoft.com/BFBFEA4A-A0D4-4114-B0AB-4338A832ECD4">IDWriteTextAnalyzer1::JustifyGlyphAdvances</a>



<a href="https://msdn.microsoft.com/9bc373b6-9161-4ffc-a942-50d97d6509c3">IDWriteTextAnalyzer::GetGlyphs</a>
 

 

