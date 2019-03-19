---
UID: NN:dwrite_3.IDWriteFactory4
title: IDWriteFactory4 (dwrite_3.h)
author: windows-sdk-content
description: The root factory interface for all DirectWrite objects.
old-location: directwrite\idwritefactory4.htm
tech.root: DirectWrite
ms.assetid: D3C5E48A-A062-430A-A196-CAC621F346FC
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDWriteFactory4, IDWriteFactory4 interface [Direct Write], IDWriteFactory4 interface [Direct Write],described, directwrite.idwritefactory4, dwrite_3/IDWriteFactory4
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFactory4 interface


## -description


The root factory interface for all DirectWrite objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFactory4</b> interface inherits from <a href="https://msdn.microsoft.com/CCE68F89-6945-40F4-9C27-285AC8AB4D0B">IDWriteFactory3</a>. <b>IDWriteFactory4</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Mt725318(v=VS.85).aspx">ComputeGlyphOrigins</a>
</td>
<td align="left" width="63%">Overloaded. Converts glyph run placements to glyph origins.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D8C38635-8D7B-4C05-87D5-CCDCF31A4070">TranslateColorGlyphRun</a>
</td>
<td align="left" width="63%">
Translates a glyph run to a sequence of color glyph runs, which can be rendered to produce a color representation of the original "base" run.

</td>
</tr>
</table> 

