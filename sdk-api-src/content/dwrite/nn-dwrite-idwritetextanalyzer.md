---
UID: NN:dwrite.IDWriteTextAnalyzer
title: IDWriteTextAnalyzer (dwrite.h)
description: Analyzes various text properties for complex script processing such as bidirectional (bidi) support for languages like Arabic, determination of line break opportunities, glyph placement, and number substitution.
old-location: directwrite\IDWriteTextAnalyzer.htm
tech.root: DirectWrite
ms.assetid: e832ffc4-31db-41b1-a008-04696d9a975e
ms.date: 12/05/2018
ms.keywords: IDWriteTextAnalyzer, IDWriteTextAnalyzer interface [Direct Write], IDWriteTextAnalyzer interface [Direct Write],described, directwrite.IDWriteTextAnalyzer, dwrite/IDWriteTextAnalyzer
ms.topic: interface
f1_keywords:
- dwrite/IDWriteTextAnalyzer
dev_langs:
- c++
req.header: dwrite.h
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
- IDWriteTextAnalyzer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteTextAnalyzer interface


## -description


 Analyzes various text properties for complex script processing such as bidirectional (bidi) support for languages like Arabic, determination of line break opportunities, glyph placement, and number substitution.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteTextAnalyzer</b> interface inherits from the <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDWriteTextAnalyzer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteTextAnalyzer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-analyzebidi">AnalyzeBidi</a>
</td>
<td align="left" width="63%">
 Analyzes a text range for script directionality, reading attributes
     from the source and reporting levels to the sink callback <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalysissink-setbidilevel">SetBidiLevel</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-analyzelinebreakpoints">AnalyzeLineBreakpoints</a>
</td>
<td align="left" width="63%">
 Analyzes a text range for potential breakpoint opportunities, reading
     attributes from the source and reporting breakpoint opportunities to
     the sink callback <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalysissink-setlinebreakpoints">SetLineBreakpoints</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-analyzenumbersubstitution">AnalyzeNumberSubstitution</a>
</td>
<td align="left" width="63%">
 Analyzes a text range for spans where number substitution is applicable,
     reading attributes from the source and reporting substitutable ranges
     to the sink callback <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalysissink-setnumbersubstitution">SetNumberSubstitution</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-analyzescript">AnalyzeScript</a>
</td>
<td align="left" width="63%">
 Analyzes a text range for script boundaries, reading text attributes
     from the source and reporting the Unicode script ID to the sink 
     callback <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalysissink-setscriptanalysis">SetScript</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/DirectWrite/idwritetextanalyzer-getgdicompatibleglyphplacements">GetGdiCompatibleGlyphPlacements</a>
</td>
<td align="left" width="63%">
Place glyphs output from the <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs">GetGlyphs</a> method according to the font 
    and the writing system's rendering rules.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphplacements">GetGlyphPlacements</a>
</td>
<td align="left" width="63%">
 Places glyphs output from the <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs">GetGlyphs</a> method according to the font 
     and the writing system's rendering rules.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs">GetGlyphs</a>
</td>
<td align="left" width="63%">
 Parses the input text string and maps it to the set of glyphs and associated glyph data
     according to the font and the writing system's rendering rules.

</td>
</tr>
</table> 

