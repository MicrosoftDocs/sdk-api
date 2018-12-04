---
UID: NN:dwrite_2.IDWriteTextAnalyzer2
title: IDWriteTextAnalyzer2
author: windows-sdk-content
description: Analyzes various text properties for complex script processing.
old-location: directwrite\idwritetextanalyzer2.htm
tech.root: DirectWrite
ms.assetid: 62DF6E71-F99D-47E9-A9BE-2A481A60AEDD
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: IDWriteTextAnalyzer2, IDWriteTextAnalyzer2 interface [Direct Write], IDWriteTextAnalyzer2 interface [Direct Write],described, directwrite.idwritetextanalyzer2, dwrite_2/IDWriteTextAnalyzer2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextAnalyzer2 interface


## -description


Analyzes various text properties for complex script processing.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteTextAnalyzer2</b> interface inherits from <a href="https://msdn.microsoft.com/7F79BA25-5D79-4491-82E3-F9B96DD0C37D">IDWriteTextAnalyzer1</a>. <b>IDWriteTextAnalyzer2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/D929E654-1DF1-49AB-A311-010DB2D79E06">CheckTypographicFeature</a>
</td>
<td align="left" width="63%">
Checks if a typographic feature is available for a glyph or a set of glyphs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4483AB14-3BC6-4980-A455-131BCBEBBFB9">GetGlyphOrientationTransform</a>
</td>
<td align="left" width="63%">
Returns 2x3 transform matrix for the respective angle to draw the
    glyph run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36CAC2F8-9065-4FD9-8EFD-529B97CE94D8">GetTypographicFeatures</a>
</td>
<td align="left" width="63%">
Returns a complete list of OpenType features available for a script or font.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/7F79BA25-5D79-4491-82E3-F9B96DD0C37D">IDWriteTextAnalyzer1</a>
 

 

