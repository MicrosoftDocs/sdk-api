---
UID: NN:wincodec.IWICStream
title: IWICStream
author: windows-sdk-content
description: Represents a Windows Imaging Component (WIC) stream for referencing imaging and metadata content.
old-location: wic\_wic_codec_iwicstream.htm
old-project: wic
ms.assetid: bc398732-037d-4f48-940f-c70975447972
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWICStream, IWICStream interface [Windows Imaging Component], IWICStream interface [Windows Imaging Component],described, _wic_codec_iwicstream, wic._wic_codec_iwicstream, wincodec/IWICStream
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WICTiffCompressionOption
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
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICStream interface


## -description


Represents a Windows Imaging Component (WIC) stream for referencing imaging and metadata content.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICStream</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Aa380034(v=VS.85).aspx">IStream</a>. <b>IWICStream</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/b0942d23-9c49-4726-9d84-bf0d448124b3">InitializeFromFilename</a>
</td>
<td align="left" width="63%">
Initializes a stream from a particular file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bfe413e1-f579-4c9c-9e88-3b369235c529">InitializeFromIStream</a>
</td>
<td align="left" width="63%">
Initializes a stream from another stream. Access rights are inherited from the underlying stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/508e1972-22ef-4211-adcf-03f8138624c9">InitializeFromIStreamRegion</a>
</td>
<td align="left" width="63%">
Initializes the stream as a substream of another stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7e226759-61aa-4f06-b20f-d5853faf4e4b">InitializeFromMemory</a>
</td>
<td align="left" width="63%">
Initializes a stream to treat a block of memory as a stream. The stream cannot grow beyond the buffer size.

</td>
</tr>
</table> 


## -remarks



Decoders and metadata handlers are expected to create sub streams of whatever stream they hold when handing off control for embedded metadata to another metadata handler.  If the stream is not restricted then use MAXLONGLONG as the max size and offset 0.

The <b>IWICStream</b> interface methods do not enable you to provide a file sharing option.
            To create a file stream for an image, use the <a href="https://msdn.microsoft.com/en-us/library/Bb759866(v=VS.85).aspx">SHCreateStreamOnFileEx</a> function.
            This stream can then be used to create an <a href="https://msdn.microsoft.com/91dafd5e-e4fb-4691-a3d0-ca8b6ff0aaf7">IWICBitmapDecoder</a> using the <a href="https://msdn.microsoft.com/b9328715-54a0-4c9a-9977-3252068b7e4b">CreateDecoderFromStream</a> method.
         



