---
UID: NN:dwrite.IDWriteFontFileEnumerator
title: IDWriteFontFileEnumerator (dwrite.h)
description: Encapsulates a collection of font files. The font system uses this interface to enumerate font files when building a font collection.
old-location: directwrite\IDWriteFontFileEnumerator.htm
tech.root: DirectWrite
ms.assetid: d89efffd-ccda-4d55-8419-de142b0f9652
ms.date: 12/05/2018
ms.keywords: IDWriteFontFileEnumerator, IDWriteFontFileEnumerator interface [Direct Write], IDWriteFontFileEnumerator interface [Direct Write],described, directwrite.IDWriteFontFileEnumerator, dwrite/IDWriteFontFileEnumerator
f1_keywords:
- dwrite/IDWriteFontFileEnumerator
dev_langs:
- c++
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
- IDWriteFontFileEnumerator
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteFontFileEnumerator interface


## -description


 Encapsulates a collection of font files. The font system uses this interface to enumerate font files when building a font collection.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFontFileEnumerator</b> interface inherits from the <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDWriteFontFileEnumerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteFontFileEnumerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-getcurrentfontfile">GetCurrentFontFile</a>
</td>
<td align="left" width="63%">
 Gets a reference to the current font file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-movenext">MoveNext</a>
</td>
<td align="left" width="63%">
 Advances to the next font file in the collection. When it is first created, the enumerator is positioned
     before the first element of the collection and the first call to <b>MoveNext</b> advances to the first file.

</td>
</tr>
</table> 

