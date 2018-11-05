---
UID: NN:dwrite.IDWriteTextAnalyzer
title: IDWriteTextAnalyzer
author: windows-sdk-content
description: Analyzes various text properties for complex script processing such as bidirectional (bidi) support for languages like Arabic, determination of line break opportunities, glyph placement, and number substitution.
old-location: directwrite\IDWriteTextAnalyzer.htm
tech.root: DirectWrite
ms.assetid: e832ffc4-31db-41b1-a008-04696d9a975e
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IDWriteTextAnalyzer, IDWriteTextAnalyzer interface [Direct Write], IDWriteTextAnalyzer interface [Direct Write],described, directwrite.IDWriteTextAnalyzer, dwrite/IDWriteTextAnalyzer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextAnalyzer interface


## -description


 Analyzes various text properties for complex script processing such as bidirectional (bidi) support for languages like Arabic, determination of line break opportunities, glyph placement, and number substitution.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteTextAnalyzer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDWriteTextAnalyzer</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/413d49d2-bacd-4e98-bfac-c0aea2650a7c">AnalyzeBidi</a>
</td>
<td align="left" width="63%">
 Analyzes a text range for script directionality, reading attributes
     from the source and reporting levels to the sink callback <a href="https://msdn.microsoft.com/f51bae22-b4a0-4f72-a341-4479d66cfec5">SetBidiLevel</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c676065-0226-456c-b8c4-10752a8daec8">AnalyzeLineBreakpoints</a>
</td>
<td align="left" width="63%">
 Analyzes a text range for potential breakpoint opportunities, reading
     attributes from the source and reporting breakpoint opportunities to
     the sink callback <a href="https://msdn.microsoft.com/423f1f0e-b2bd-48b6-aa3b-c79a2b542d5d">SetLineBreakpoints</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1cd53f79-5bbc-4a70-b66a-b807fe163a98">AnalyzeNumberSubstitution</a>
</td>
<td align="left" width="63%">
 Analyzes a text range for spans where number substitution is applicable,
     reading attributes from the source and reporting substitutable ranges
     to the sink callback <a href="https://msdn.microsoft.com/09b00b49-702e-4cef-bf1c-397c5d572513">SetNumberSubstitution</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e681f7c8-7d87-454b-a7b6-6c3fe38b0f92">AnalyzeScript</a>
</td>
<td align="left" width="63%">
 Analyzes a text range for script boundaries, reading text attributes
     from the source and reporting the Unicode script ID to the sink 
     callback <a href="https://msdn.microsoft.com/beae0420-b244-4c87-a3cb-a1b34562c3ed">SetScript</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49312b03-9ee9-44ef-b3eb-a35631a6e693">GetGdiCompatibleGlyphPlacements</a>
</td>
<td align="left" width="63%">
Place glyphs output from the <a href="https://msdn.microsoft.com/9bc373b6-9161-4ffc-a942-50d97d6509c3">GetGlyphs</a> method according to the font 
    and the writing system's rendering rules.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72e9af97-6fd2-4dd0-befc-2e9f809c12a2">GetGlyphPlacements</a>
</td>
<td align="left" width="63%">
 Places glyphs output from the <a href="https://msdn.microsoft.com/9bc373b6-9161-4ffc-a942-50d97d6509c3">GetGlyphs</a> method according to the font 
     and the writing system's rendering rules.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9bc373b6-9161-4ffc-a942-50d97d6509c3">GetGlyphs</a>
</td>
<td align="left" width="63%">
 Parses the input text string and maps it to the set of glyphs and associated glyph data
     according to the font and the writing system's rendering rules.

</td>
</tr>
</table> 

