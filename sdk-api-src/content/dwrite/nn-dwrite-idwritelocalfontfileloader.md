---
UID: NN:dwrite.IDWriteLocalFontFileLoader
title: IDWriteLocalFontFileLoader (dwrite.h)
description: A built-in implementation of the IDWriteFontFileLoader interface, that operates on local font files and exposes local font file information from the font file reference key.
old-location: directwrite\idwritelocalfontfileloader.htm
tech.root: DirectWrite
ms.assetid: acb777c8-24c6-452e-8f58-8fb2ad8c0b6c
ms.date: 12/05/2018
ms.keywords: IDWriteLocalFontFileLoader, IDWriteLocalFontFileLoader interface [Direct Write], IDWriteLocalFontFileLoader interface [Direct Write],described, directwrite.idwritelocalfontfileloader, dwrite/IDWriteLocalFontFileLoader
f1_keywords:
- dwrite/IDWriteLocalFontFileLoader
dev_langs:
- c++
req.header: dwrite.h
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
- IDWriteLocalFontFileLoader
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteLocalFontFileLoader interface


## -description


A built-in implementation of the <a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader">IDWriteFontFileLoader</a> interface, that operates on local font files
and exposes local font file information from the font file reference key. Font file references created using <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference">CreateFontFileReference</a> use this font file loader.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteLocalFontFileLoader</b> interface inherits from the <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDWriteLocalFontFileLoader</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteLocalFontFileLoader</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/DirectWrite/idwritelocalfontfileloader-getfilepathfromkey">GetFilePathFromKey</a>
</td>
<td align="left" width="63%">
Obtains the absolute font file path from the font file reference key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/DirectWrite/idwritelocalfontfileloader-getfilepathlengthfromkey">GetFilePathLengthFromKey</a>
</td>
<td align="left" width="63%">
Obtains the length of the absolute file path from the font file reference key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/DirectWrite/idwritelocalfontfileloader-getlastwritetimefromkey">GetLastWriteTimeFromKey</a>
</td>
<td align="left" width="63%">
Obtains the last write time of the file from the font file reference key.

</td>
</tr>
</table> 

