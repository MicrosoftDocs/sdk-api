---
UID: NN:dwrite_3.IDWriteFactory5
title: IDWriteFactory5 (dwrite_3.h)
description: The root factory interface for all DirectWrite objects.
old-location: directwrite\idwritefactory5.htm
tech.root: DirectWrite
ms.assetid: 2F3E30DC-A965-4C68-A337-73F338CF2563
ms.date: 12/05/2018
ms.keywords: IDWriteFactory5, IDWriteFactory5 interface [Direct Write], IDWriteFactory5 interface [Direct Write],described, directwrite.idwritefactory5, dwrite_3/IDWriteFactory5
f1_keywords:
- dwrite_3/IDWriteFactory5
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
- IDWriteFactory5
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteFactory5 interface


## -description


The root factory interface for all DirectWrite objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFactory5</b> interface inherits from <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory4">IDWriteFactory4</a>. <b>IDWriteFactory5</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteFactory5</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-analyzecontainertype">AnalyzeContainerType</a>
</td>
<td align="left" width="63%">
The AnalyzeContainerType method analyzes the specified file data to determine whether it is a known font container format (e.g., WOFF or WOFF2).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-createfontsetbuilder">CreateFontSetBuilder</a>
</td>
<td align="left" width="63%">
Creates an empty font set builder to add font face references and create a custom font set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-createhttpfontfileloader">CreateHttpFontFileLoader</a>
</td>
<td align="left" width="63%">
Creates a remote font file loader that can create font file references from HTTP or HTTPS URLs. The caller is responsible for registering and unregistering the loader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-createinmemoryfontfileloader">CreateInMemoryFontFileLoader</a>
</td>
<td align="left" width="63%">
Creates a loader object that can be used to create font file references to in-memory fonts. The caller is responsible for registering and unregistering the loader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-unpackfontfile">UnpackFontFile</a>
</td>
<td align="left" width="63%">
The UnpackFontFile method unpacks font data from a container file (WOFF or WOFF2) and returns the unpacked font data in the form of a font file stream.

</td>
</tr>
</table> 


## -see-also




<a href="/windows/win32/DirectWrite/custom-font-sets-win10">Custom Font Sets</a>



<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory4">IDWriteFactory4</a>
 

 

