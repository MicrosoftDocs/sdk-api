---
UID: NN:dwrite_3.IDWriteFactory4
title: IDWriteFactory4 (dwrite_3.h)
description: The root factory interface for all DirectWrite objects.
old-location: directwrite\idwritefactory4.htm
tech.root: DirectWrite
ms.assetid: D3C5E48A-A062-430A-A196-CAC621F346FC
ms.date: 12/05/2018
ms.keywords: IDWriteFactory4, IDWriteFactory4 interface [Direct Write], IDWriteFactory4 interface [Direct Write],described, directwrite.idwritefactory4, dwrite_3/IDWriteFactory4
f1_keywords:
- dwrite_3/IDWriteFactory4
dev_langs:
- c++
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Dwrite.lib
- Dwrite.dll
api_name:
- IDWriteFactory4
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteFactory4 interface


## -description


The root factory interface for all DirectWrite objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFactory4</b> interface inherits from <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3">IDWriteFactory3</a>. <b>IDWriteFactory4</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteFactory4</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_3/nf-dwrite_3-computeglyphorigins">ComputeGlyphOrigins</a>
</td>
<td align="left" width="63%">Overloaded. Converts glyph run placements to glyph origins.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun">TranslateColorGlyphRun</a>
</td>
<td align="left" width="63%">
Translates a glyph run to a sequence of color glyph runs, which can be rendered to produce a color representation of the original "base" run.

</td>
</tr>
</table> 

