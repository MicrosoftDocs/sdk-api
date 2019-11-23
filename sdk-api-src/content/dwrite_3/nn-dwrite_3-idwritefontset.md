---
UID: NN:dwrite_3.IDWriteFontSet
title: IDWriteFontSet (dwrite_3.h)

description: Represents a font set.
old-location: directwrite\idwritefontset.htm
tech.root: DirectWrite
ms.assetid: 0178f248-8dc0-c0ee-63c1-8db3f6ef94c3

ms.date: 12/05/2018
ms.keywords: IDWriteFontSet, IDWriteFontSet interface [Direct Write], IDWriteFontSet interface [Direct Write],described, directwrite.idwritefontset, dwrite_3/IDWriteFontSet
ms.topic: interface
f1_keywords: 
 - "dwrite_3/IDWriteFontSet"
dev_langs:
 - c++
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
 - IDWriteFontSet
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteFontSet interface


## -description


Represents a font set.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFontSet</b> interface inherits from the <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDWriteFontSet</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteFontSet</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-findfontface">FindFontFace</a>
</td>
<td align="left" width="63%">
Gets the index of the matching font face reference in the font set, with the same file, face index, and simulations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-findfontfacereference">FindFontFaceReference</a>
</td>
<td align="left" width="63%">
Gets the index of the matching font face reference in the font set, with the same file, face index, and simulations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getfontcount">GetFontCount</a>
</td>
<td align="left" width="63%">
Get the number of total fonts in the set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getfontfacereference">GetFontFaceReference</a>
</td>
<td align="left" width="63%">
Gets a reference to the font at the specified index, which may be local or remote.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/DirectWrite/idwritefontset-getmatchingfonts-overload">GetMatchingFonts</a>
</td>
<td align="left" width="63%">Overloaded. Returns a subset of fonts matching the specified criteria.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyoccurrencecount">GetPropertyOccurrenceCount</a>
</td>
<td align="left" width="63%">
Returns how many times a given property value occurs in the set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_3/nf-dwrite_3-getpropertyvalues">GetPropertyValues</a>
</td>
<td align="left" width="63%">Overloaded. Returns property values for the font set.

</td>
</tr>
</table> 

