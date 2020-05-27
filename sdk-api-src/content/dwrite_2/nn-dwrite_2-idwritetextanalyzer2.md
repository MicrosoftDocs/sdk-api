---
UID: NN:dwrite_2.IDWriteTextAnalyzer2
title: IDWriteTextAnalyzer2 (dwrite_2.h)
description: Analyzes various text properties for complex script processing.
helpviewer_keywords: ["IDWriteTextAnalyzer2","IDWriteTextAnalyzer2 interface [Direct Write]","IDWriteTextAnalyzer2 interface [Direct Write]","described","directwrite.idwritetextanalyzer2","dwrite_2/IDWriteTextAnalyzer2"]
old-location: directwrite\idwritetextanalyzer2.htm
tech.root: DirectWrite
ms.assetid: 62DF6E71-F99D-47E9-A9BE-2A481A60AEDD
ms.date: 12/05/2018
ms.keywords: IDWriteTextAnalyzer2, IDWriteTextAnalyzer2 interface [Direct Write], IDWriteTextAnalyzer2 interface [Direct Write],described, directwrite.idwritetextanalyzer2, dwrite_2/IDWriteTextAnalyzer2
f1_keywords:
- dwrite_2/IDWriteTextAnalyzer2
dev_langs:
- c++
req.header: dwrite_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
- IDWriteTextAnalyzer2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteTextAnalyzer2 interface


## -description


Analyzes various text properties for complex script processing.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteTextAnalyzer2</b> interface inherits from <a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1">IDWriteTextAnalyzer1</a>. <b>IDWriteTextAnalyzer2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteTextAnalyzer2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-checktypographicfeature">CheckTypographicFeature</a>
</td>
<td align="left" width="63%">
Checks if a typographic feature is available for a glyph or a set of glyphs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-getglyphorientationtransform">GetGlyphOrientationTransform</a>
</td>
<td align="left" width="63%">
Returns 2x3 transform matrix for the respective angle to draw the
    glyph run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-gettypographicfeatures">GetTypographicFeatures</a>
</td>
<td align="left" width="63%">
Returns a complete list of OpenType features available for a script or font.

</td>
</tr>
</table> 


## -see-also




<a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1">IDWriteTextAnalyzer1</a>
 

 

