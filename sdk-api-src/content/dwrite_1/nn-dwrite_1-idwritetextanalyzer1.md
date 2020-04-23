---
UID: NN:dwrite_1.IDWriteTextAnalyzer1
title: IDWriteTextAnalyzer1 (dwrite_1.h)
description: Analyzes various text properties for complex script processing.helpviewer_keywords: ["IDWriteTextAnalyzer1","IDWriteTextAnalyzer1 interface [Direct Write]","IDWriteTextAnalyzer1 interface [Direct Write]","described","directwrite.idwritetextanalyzer1","dwrite_1/IDWriteTextAnalyzer1"]
old-location: directwrite\idwritetextanalyzer1.htm
tech.root: DirectWrite
ms.assetid: 7F79BA25-5D79-4491-82E3-F9B96DD0C37D
ms.date: 12/05/2018
ms.keywords: IDWriteTextAnalyzer1, IDWriteTextAnalyzer1 interface [Direct Write], IDWriteTextAnalyzer1 interface [Direct Write],described, directwrite.idwritetextanalyzer1, dwrite_1/IDWriteTextAnalyzer1
f1_keywords:
- dwrite_1/IDWriteTextAnalyzer1
dev_langs:
- c++
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
- IDWriteTextAnalyzer1
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteTextAnalyzer1 interface


## -description


Analyzes various text properties for complex script processing.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteTextAnalyzer1</b> interface inherits from <a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer">IDWriteTextAnalyzer</a>. <b>IDWriteTextAnalyzer1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteTextAnalyzer1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-analyzeverticalglyphorientation">AnalyzeVerticalGlyphOrientation</a>
</td>
<td align="left" width="63%">
Analyzes a text range for script orientation, reading text and
    attributes from the source and reporting results to the sink callback <a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalysissink1-setglyphorientation">SetGlyphOrientation</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-applycharacterspacing">ApplyCharacterSpacing</a>
</td>
<td align="left" width="63%">
Applies spacing between characters, properly adjusting glyph clusters
    and diacritics.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getbaseline">GetBaseline</a>
</td>
<td align="left" width="63%">
Retrieves the given baseline from the font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getglyphorientationtransform">GetGlyphOrientationTransform</a>
</td>
<td align="left" width="63%">
Returns 2x3 transform matrix for the respective angle to draw the
    glyph run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getjustificationopportunities">GetJustificationOpportunities</a>
</td>
<td align="left" width="63%">
Retrieves justification opportunity information for each of the glyphs
    given the text and shaping glyph properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getjustifiedglyphs">GetJustifiedGlyphs</a>
</td>
<td align="left" width="63%">
Fills in new glyphs for complex scripts where justification increased
    the advances of glyphs, such as Arabic with kashida.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getscriptproperties">GetScriptProperties</a>
</td>
<td align="left" width="63%">
Retrieves the properties for a given script.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-gettextcomplexity">GetTextComplexity</a>
</td>
<td align="left" width="63%">
Determines the complexity of text, and whether you need to call <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs">IDWriteTextAnalyzer::GetGlyphs</a> for full script
    shaping. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-justifyglyphadvances">JustifyGlyphAdvances</a>
</td>
<td align="left" width="63%">
Justifies an array of glyph advances to fit the line width.

</td>
</tr>
</table> 


## -see-also




<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer">IDWriteTextAnalyzer</a>
 

 

