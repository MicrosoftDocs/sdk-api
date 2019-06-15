---
UID: NN:dwrite_3.IDWriteRemoteFontFileStream
title: IDWriteRemoteFontFileStream (dwrite_3.h)
author: windows-sdk-content
description: Represents a font file stream, parts of which may be non-local.
old-location: directwrite\idwriteremotefontfilestream.htm
tech.root: DirectWrite
ms.assetid: 2CC73CE0-162A-4808-ACB6-A9599FD4D09F
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDWriteRemoteFontFileStream, IDWriteRemoteFontFileStream interface [Direct Write], IDWriteRemoteFontFileStream interface [Direct Write],described, directwrite.idwriteremotefontfilestream, dwrite_3/IDWriteRemoteFontFileStream
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
 - IDWriteRemoteFontFileStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteRemoteFontFileStream interface


## -description


Represents a font file stream, parts of which may be non-local.
          Non-local data must be downloaded before it can be accessed using
          ReadFragment. The interface exposes methods to download font data and query the locality of font data.
      


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteRemoteFontFileStream</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nn-dwrite-idwritefontfilestream">IDWriteFontFileStream</a>. <b>IDWriteRemoteFontFileStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteRemoteFontFileStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_3/nf-dwrite_3-idwriteremotefontfilestream-begindownload">BeginDownload</a>
</td>
<td align="left" width="63%">
Begins downloading all or part of the font file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_3/nf-dwrite_3-idwriteremotefontfilestream-getfilefragmentlocality">GetFileFragmentLocality</a>
</td>
<td align="left" width="63%">
Returns information about the locality of a byte range (i.e., font fragment) within the font file stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_3/nf-dwrite_3-idwriteremotefontfilestream-getlocalfilesize">GetLocalFileSize</a>
</td>
<td align="left" width="63%">
GetLocalFileSize returns the number of bytes of the font file that are currently local, which should always be less than or equal to the full
          file size returned by <a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritefontfilestream-getfilesize">GetFileSize</a>. 
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_3/nf-dwrite_3-idwriteremotefontfilestream-getlocality">GetLocality</a>
</td>
<td align="left" width="63%">
Gets the current locality of the file.

</td>
</tr>
</table> 


## -remarks



For more information, see the description of IDWriteRemoteFontFileLoader.



