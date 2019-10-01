---
UID: NN:dwrite_2.IDWriteFactory2
title: IDWriteFactory2 (dwrite_2.h)
author: windows-sdk-content
description: The root factory interface for all DirectWrite objects.
old-location: directwrite\idwritefactory2.htm
tech.root: DirectWrite
ms.assetid: 1D3EEC28-EAB3-4FA2-98E9-7A8FDAF6E6FE
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDWriteFactory1, IDWriteFactory1 interface [Direct Write], IDWriteFactory1 interface [Direct Write],described, IDWriteFactory2, directwrite.idwritefactory2, dwrite_2/IDWriteFactory2
ms.topic: interface
f1_keywords: 
 - "dwrite_2/IDWriteFactory1"
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
 - IDWriteFactory1
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteFactory2 interface


## -description


The root factory interface for all <a href="/windows/win32/DirectWrite/direct-write-portal">DirectWrite</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFactory1</b> interface inherits from <a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1">IDWriteFactory1</a>. <b>IDWriteFactory2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteFactory1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/DirectWrite/idwritefactory2-createcustomrenderingparams">CreateCustomRenderingParams</a>
</td>
<td align="left" width="63%">
Creates a rendering parameters object with the specified properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-createfontfallbackbuilder">CreateFontFallbackBuilder</a>
</td>
<td align="left" width="63%">
Creates a font fallback builder object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/DirectWrite/idwritefactory2-createglyphrunanalysis">CreateGlyphRunAnalysis</a>
</td>
<td align="left" width="63%">
Creates a glyph run analysis object, which encapsulates information used to render a glyph run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/DirectWrite/idwritefactory2-getsystemfontfallback">GetSystemFontFallback</a>
</td>
<td align="left" width="63%">
Creates a font fallback object from the system font fallback list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-translatecolorglyphrun">TranslateColorGlyphRun</a>
</td>
<td align="left" width="63%">
This method is called on a glyph run to translate it in to multiple color glyph runs.

</td>
</tr>
</table> 


## -see-also




<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>



<a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1">IDWriteFactory1</a>
 

 

