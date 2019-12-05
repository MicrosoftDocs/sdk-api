---
UID: NN:dwrite_2.IDWriteFontFallbackBuilder
title: IDWriteFontFallbackBuilder (dwrite_2.h)
description: Allows you to create Unicode font fallback mappings and create a font fall back object from those mappings.
old-location: directwrite\idwritefontfallbackbuilder.htm
tech.root: DirectWrite
ms.assetid: 462AC12E-C856-4D8F-83AF-FAC3221425C2
ms.date: 12/05/2018
ms.keywords: IDWriteFontFallbackBuilder, IDWriteFontFallbackBuilder interface [Direct Write], IDWriteFontFallbackBuilder interface [Direct Write],described, directwrite.idwritefontfallbackbuilder, dwrite_2/IDWriteFontFallbackBuilder
ms.topic: interface
f1_keywords:
- dwrite_2/IDWriteFontFallbackBuilder
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
- IDWriteFontFallbackBuilder
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteFontFallbackBuilder interface


## -description


Allows you to create Unicode font fallback mappings and create a font fall back object from those mappings.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFontFallbackBuilder</b> interface inherits from the <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDWriteFontFallbackBuilder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteFontFallbackBuilder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/DirectWrite/idwritefontfallbackbuilder-addmapping">AddMapping</a>
</td>
<td align="left" width="63%">
Appends a single mapping to the list. Call this once for each additional mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefontfallbackbuilder-addmappings">AddMappings</a>
</td>
<td align="left" width="63%">
Add all the mappings from an existing font fallback object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefontfallbackbuilder-createfontfallback">CreateFontFallback</a>
</td>
<td align="left" width="63%">
Creates the finalized fallback object from the mappings added.

</td>
</tr>
</table> 

