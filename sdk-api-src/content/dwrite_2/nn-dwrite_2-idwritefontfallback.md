---
UID: NN:dwrite_2.IDWriteFontFallback
title: IDWriteFontFallback (dwrite_2.h)
description: Allows you to access fallback fonts from the font list.
helpviewer_keywords: ["IDWriteFontFallback","IDWriteFontFallback interface [Direct Write]","IDWriteFontFallback interface [Direct Write]","described","directwrite.idwritefontfallback","dwrite_2/IDWriteFontFallback"]
old-location: directwrite\idwritefontfallback.htm
tech.root: DirectWrite
ms.assetid: CBC4100A-756B-429E-8368-D5D018A2B0AC
ms.date: 12/05/2018
ms.keywords: IDWriteFontFallback, IDWriteFontFallback interface [Direct Write], IDWriteFontFallback interface [Direct Write],described, directwrite.idwritefontfallback, dwrite_2/IDWriteFontFallback
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteFontFallback
 - dwrite_2/IDWriteFontFallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFontFallback
---

# IDWriteFontFallback interface


## -description

Allows you to access fallback fonts from the font list.

The <b>IDWriteFontFallback</b> interface defines a fallback sequence to map character ranges to fonts, which is either created via <a href="/windows/win32/DirectWrite/idwritefontfallbackbuilder">IDWriteFontFallbackBuilder</a> or retrieved from <a href="/windows/win32/DirectWrite/idwritefactory2-getsystemfontfallback">IDWriteFactory2::GetSystemFontFallback</a>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFontFallback</b> interface inherits from the <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDWriteFontFallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteFontFallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/DirectWrite/idwritefontfallback-mapcharacters">MapCharacters</a>
</td>
<td align="left" width="63%">
Determines an appropriate font to use to render the beginning range of text.

</td>
</tr>
</table>

