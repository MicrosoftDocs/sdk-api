---
UID: NN:wincodec.IWICStream
title: IWICStream (wincodec.h)
author: windows-sdk-content
description: Represents a Windows Imaging Component (WIC) stream for referencing imaging and metadata content.
old-location: wic\_wic_codec_iwicstream.htm
tech.root: wic
ms.assetid: bc398732-037d-4f48-940f-c70975447972
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWICStream, IWICStream interface [Windows Imaging Component], IWICStream interface [Windows Imaging Component],described, _wic_codec_iwicstream, wic._wic_codec_iwicstream, wincodec/IWICStream
ms.topic: interface
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICStream interface


## -description


Represents a Windows Imaging Component (WIC) stream for referencing imaging and metadata content.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICStream</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>. <b>IWICStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicstream-initializefromfilename">InitializeFromFilename</a>
</td>
<td align="left" width="63%">
Initializes a stream from a particular file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicstream-initializefromistream">InitializeFromIStream</a>
</td>
<td align="left" width="63%">
Initializes a stream from another stream. Access rights are inherited from the underlying stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicstream-initializefromistreamregion">InitializeFromIStreamRegion</a>
</td>
<td align="left" width="63%">
Initializes the stream as a substream of another stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicstream-initializefrommemory">InitializeFromMemory</a>
</td>
<td align="left" width="63%">
Initializes a stream to treat a block of memory as a stream. The stream cannot grow beyond the buffer size.

</td>
</tr>
</table> 


## -remarks



Decoders and metadata handlers are expected to create sub streams of whatever stream they hold when handing off control for embedded metadata to another metadata handler.  If the stream is not restricted then use MAXLONGLONG as the max size and offset 0.

The <b>IWICStream</b> interface methods do not enable you to provide a file sharing option.
            To create a file stream for an image, use the <a href="https://docs.microsoft.com/windows/desktop/api/shlwapi/nf-shlwapi-shcreatestreamonfileex">SHCreateStreamOnFileEx</a> function.
            This stream can then be used to create an <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder">IWICBitmapDecoder</a> using the <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream">CreateDecoderFromStream</a> method.
         



