---
UID: NN:dwrite_1.IDWriteTextAnalyzer1
title: IDWriteTextAnalyzer1 (dwrite_1.h)
author: windows-sdk-content
description: Analyzes various text properties for complex script processing.
old-location: directwrite\idwritetextanalyzer1.htm
tech.root: DirectWrite
ms.assetid: 7F79BA25-5D79-4491-82E3-F9B96DD0C37D
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDWriteTextAnalyzer1, IDWriteTextAnalyzer1 interface [Direct Write], IDWriteTextAnalyzer1 interface [Direct Write],described, directwrite.idwritetextanalyzer1, dwrite_1/IDWriteTextAnalyzer1
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextAnalyzer1 interface


## -description


Analyzes various text properties for complex script processing.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteTextAnalyzer1</b> interface inherits from <a href="https://msdn.microsoft.com/e832ffc4-31db-41b1-a008-04696d9a975e">IDWriteTextAnalyzer</a>. <b>IDWriteTextAnalyzer1</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/E89C7E50-9EDA-4AC9-9FC0-B70E493ED1B4">AnalyzeVerticalGlyphOrientation</a>
</td>
<td align="left" width="63%">
Analyzes a text range for script orientation, reading text and
    attributes from the source and reporting results to the sink callback <a href="https://msdn.microsoft.com/81BD4C36-273B-4C28-A89E-88BABCAD511A">SetGlyphOrientation</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E4BACB7E-0032-450C-AEA8-87434329F33C">ApplyCharacterSpacing</a>
</td>
<td align="left" width="63%">
Applies spacing between characters, properly adjusting glyph clusters
    and diacritics.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ACD5075-BD96-41FC-AE36-8D5D03F2EB54">GetBaseline</a>
</td>
<td align="left" width="63%">
Retrieves the given baseline from the font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/583AFE54-F816-4098-844B-C3F838BE46B0">GetGlyphOrientationTransform</a>
</td>
<td align="left" width="63%">
Returns 2x3 transform matrix for the respective angle to draw the
    glyph run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85D3841F-FA2B-4636-B786-DCD68C72209A">GetJustificationOpportunities</a>
</td>
<td align="left" width="63%">
Retrieves justification opportunity information for each of the glyphs
    given the text and shaping glyph properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8F7BB9EC-90AE-48BD-A596-EAF2EDC4053F">GetJustifiedGlyphs</a>
</td>
<td align="left" width="63%">
Fills in new glyphs for complex scripts where justification increased
    the advances of glyphs, such as Arabic with kashida.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CBC1DA09-6D3D-42D8-8E77-CFDBA733C228">GetScriptProperties</a>
</td>
<td align="left" width="63%">
Retrieves the properties for a given script.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EC9364F7-4A00-4DEE-B51A-F26FBBA5683F">GetTextComplexity</a>
</td>
<td align="left" width="63%">
Determines the complexity of text, and whether you need to call <a href="https://msdn.microsoft.com/9bc373b6-9161-4ffc-a942-50d97d6509c3">IDWriteTextAnalyzer::GetGlyphs</a> for full script
    shaping. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BFBFEA4A-A0D4-4114-B0AB-4338A832ECD4">JustifyGlyphAdvances</a>
</td>
<td align="left" width="63%">
Justifies an array of glyph advances to fit the line width.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e832ffc4-31db-41b1-a008-04696d9a975e">IDWriteTextAnalyzer</a>
 

 

