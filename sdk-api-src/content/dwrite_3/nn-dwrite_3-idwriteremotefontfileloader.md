---
UID: NN:dwrite_3.IDWriteRemoteFontFileLoader
title: IDWriteRemoteFontFileLoader (dwrite_3.h)
description: Represents a font file loader that can access remote (i.e., downloadable) fonts.
old-location: directwrite\idwriteremotefontfileloader.htm
tech.root: DirectWrite
ms.assetid: 16CFF7ED-642A-48D8-8C72-3EC68B702E50
ms.date: 12/05/2018
ms.keywords: IDWriteRemoteFontFileLoader, IDWriteRemoteFontFileLoader interface [Direct Write], IDWriteRemoteFontFileLoader interface [Direct Write],described, directwrite.idwriteremotefontfileloader, dwrite_3/IDWriteRemoteFontFileLoader
ms.topic: interface
f1_keywords:
- dwrite_3/IDWriteRemoteFontFileLoader
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
- IDWriteRemoteFontFileLoader
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteRemoteFontFileLoader interface

## -description

Represents a font file loader that can access remote (i.e., downloadable) fonts. The <a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-createhttpfontfileloader">IDWriteFactory5::CreateHttpFontFileLoader</a> method returns an instance of this interface,
        which the client can use to load remote fonts without having to implement a custom loader. 
        A client can also create its own custom implementation, however. 
        In either case, the client is responsible for registering and unregistering the loader using IDWriteFactory::<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-registerfontfileloader">RegisterFontFileLoader</a> 
        and IDWriteFactory::<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-unregisterfontfileloader">UnregisterFontFileLoader</a>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteRemoteFontFileLoader</b> interface inherits from <a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader">IDWriteFontFileLoader</a>. <b>IDWriteRemoteFontFileLoader</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteRemoteFontFileLoader</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwriteremotefontfileloader-createfontfilereferencefromurl">CreateFontFileReferenceFromUrl</a>
</td>
<td align="left" width="63%">
Creates a font file reference from a URL if the loader supports this capability.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwriteremotefontfileloader-createremotestreamfromkey">CreateRemoteStreamFromKey</a>
</td>
<td align="left" width="63%">
Creates a remote font file stream object that encapsulates an open file resource and can be used to download remote file data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwriteremotefontfileloader-getlocalityfromkey">GetLocalityFromKey</a>
</td>
<td align="left" width="63%">
Gets the locality of the file resource identified by the unique key.

</td>
</tr>
</table> 

## -see-also

[Creating a custom font set using known, remote fonts on the Web](/windows/win32/directwrite/custom-font-sets-win10#creating-a-custom-font-set-using-known-remote-fonts-on-the-web)

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader">IDWriteFontFileLoader</a>
