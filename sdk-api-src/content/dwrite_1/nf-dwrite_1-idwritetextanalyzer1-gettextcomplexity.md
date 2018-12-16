---
UID: NF:dwrite_1.IDWriteTextAnalyzer1.GetTextComplexity
title: IDWriteTextAnalyzer1::GetTextComplexity
author: windows-sdk-content
description: Determines the complexity of text, and whether you need to call IDWriteTextAnalyzer::GetGlyphs for full script shaping.
old-location: directwrite\idwritetextanalyzer1_gettextcomplexity.htm
tech.root: DirectWrite
ms.assetid: EC9364F7-4A00-4DEE-B51A-F26FBBA5683F
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetTextComplexity, GetTextComplexity method [Direct Write], GetTextComplexity method [Direct Write],IDWriteTextAnalyzer1 interface, IDWriteTextAnalyzer1 interface [Direct Write],GetTextComplexity method, IDWriteTextAnalyzer1.GetTextComplexity, IDWriteTextAnalyzer1::GetTextComplexity, directwrite.idwritetextanalyzer1_gettextcomplexity, dwrite_1/IDWriteTextAnalyzer1::GetTextComplexity
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
 - IDWriteTextAnalyzer1.GetTextComplexity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextAnalyzer1::GetTextComplexity


## -description


Determines the complexity of text, and whether you need to call <a href="https://msdn.microsoft.com/9bc373b6-9161-4ffc-a942-50d97d6509c3">IDWriteTextAnalyzer::GetGlyphs</a> for full script
    shaping. 


## -parameters




### -param textString [in]

Type: <b>const WCHAR*</b>

The text to check for complexity. This string
    may be UTF-16, but any supplementary characters will be considered
    complex.


### -param textLength

Type: <b>UINT32</b>

Length of the text to check.


### -param fontFace

Type: <b><a href="https://msdn.microsoft.com/1DB7156F-0578-46A0-8C96-E1E34FF4E49E">IDWriteFontFace</a>*</b>

The font face to read.


### -param isTextSimple [out]

Type: <b>BOOL*</b>

If true, the text is simple, and the
    <i>glyphIndices</i> array will already have the nominal glyphs for you.
    Otherwise, you need to call <a href="https://msdn.microsoft.com/9bc373b6-9161-4ffc-a942-50d97d6509c3">IDWriteTextAnalyzer::GetGlyphs</a> to properly shape complex
    scripts and OpenType features.


### -param textLengthRead [out]

Type: <b>UINT32*</b>

The length read of the text run with the
    same complexity, simple or complex. You may call again from that
    point onward.


### -param glyphIndices [out, optional]

Type: <b>UINT16*</b>

Optional glyph indices for the text. If the
    function returned that the text was simple, you already have the
    glyphs you need. Otherwise the glyph indices are not meaningful,
    and you need to call <a href="https://msdn.microsoft.com/9bc373b6-9161-4ffc-a942-50d97d6509c3">IDWriteTextAnalyzer::GetGlyphs</a> for shaping instead.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Text is not simple if the characters are part of a script that has
    complex shaping requirements, require bidi analysis, combine with
    other characters, reside in the supplementary planes, or have glyphs
    that participate in standard OpenType features. The length returned
    will not split combining marks from their base characters.




## -see-also




<a href="https://msdn.microsoft.com/7F79BA25-5D79-4491-82E3-F9B96DD0C37D">IDWriteTextAnalyzer1</a>



<a href="https://msdn.microsoft.com/9bc373b6-9161-4ffc-a942-50d97d6509c3">IDWriteTextAnalyzer::GetGlyphs</a>
 

 

