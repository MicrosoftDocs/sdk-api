---
UID: NN:dwrite_3.IDWriteGdiInterop1
title: IDWriteGdiInterop1 (dwrite_3.h)
author: windows-sdk-content
description: Provides interoperability with GDI, such as methods to convert a font face to a LOGFONT structure, or to convert a GDI font description into a font face. It is also used to create bitmap render target objects.
old-location: directwrite\idwritegdiinterop1.htm
tech.root: DirectWrite
ms.assetid: A69922D8-EF9F-4F46-91D3-F7F649CF4705
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDWriteGdiInterop1, IDWriteGdiInterop1 interface [Direct Write], IDWriteGdiInterop1 interface [Direct Write],described, directwrite.idwritegdiinterop1, dwrite_3/IDWriteGdiInterop1
ms.topic: interface
f1_keywords: 
 - "dwrite_3/IDWriteGdiInterop1"
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
 - IDWriteGdiInterop1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteGdiInterop1 interface


## -description


Provides interoperability with GDI, such as methods to convert a font face to a LOGFONT structure, or to convert a GDI font description into a font face. 
        It is also used to create bitmap render target objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteGdiInterop1</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nn-dwrite-idwritegdiinterop">IDWriteGdiInterop</a>. <b>IDWriteGdiInterop1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteGdiInterop1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_3/nf-dwrite_3-idwritegdiinterop1-createfontfromlogfont">CreateFontFromLOGFONT</a>
</td>
<td align="left" width="63%">
Creates a font object that matches the properties specified by the LOGFONT structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_3/nf-dwrite_3-getfontsignature">GetFontSignature</a>
</td>
<td align="left" width="63%">Overloaded. Retrieves a font signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_3/nf-dwrite_3-idwritegdiinterop1-getmatchingfontsbylogfont">GetMatchingFontsByLOGFONT</a>
</td>
<td align="left" width="63%">
Gets a list of matching fonts based on the specified LOGFONT values. Only fonts
        of that family name will be returned.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nn-dwrite-idwritegdiinterop">IDWriteGdiInterop</a>
 

 

