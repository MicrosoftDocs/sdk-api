---
UID: NN:wincodec.IWICJpegFrameDecode
title: IWICJpegFrameDecode
author: windows-driver-content
description: Exposes methods for decoding JPEG images. Provides access to the Start Of Frame (SOF) header, Start of Scan (SOS) header, the Huffman and Quantization tables, and the compressed JPEG JPEG data. Also enables indexing for efficient random access.
old-location: wic\iwicjpegframedecode.htm
old-project: wic
ms.assetid: E6310320-53A8-40F1-8964-D21D8054E1B8
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: IWICJpegFrameDecode, IWICJpegFrameDecode interface [Windows Imaging Component], IWICJpegFrameDecode interface [Windows Imaging Component], described, wic.iwicjpegframedecode, wincodec/IWICJpegFrameDecode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WICTiffCompressionOption
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.dll
api_name:
-	IWICJpegFrameDecode
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICJpegFrameDecode interface


## -description


Exposes methods for decoding JPEG images. Provides access to the Start Of Frame (SOF) header, Start of Scan (SOS) header, the Huffman and Quantization tables, and the compressed JPEG JPEG data. Also enables indexing for efficient random access. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICJpegFrameDecode</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWICJpegFrameDecode</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICJpegFrameDecode</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/467E0100-F00B-4D2D-BF2A-8138765C787E">ClearIndexing</a>
</td>
<td align="left" width="63%">
Removes the indexing from a JPEG that has been indexed using <a href="https://msdn.microsoft.com/D97A48E5-0398-460C-AFA9-2E1B8744926B">IWICJpegFrameDecode::SetIndexing</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19579C0B-AB96-424D-B433-6A88BE64A434">CopyScan</a>
</td>
<td align="left" width="63%">
Retrieves a copy of the compressed JPEG scan directly from the WIC decoder frame's output stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/99486168-6BF9-40C2-B9D8-903A73AAD125">DoesSupportIndexing</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether this decoder supports indexing for efficient random access.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6063E147-70A4-46F8-940E-42DBD87A500F">GetAcHuffmanTable</a>
</td>
<td align="left" width="63%">
Retrieves a copy of the AC Huffman table for the specified scan and table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3C4FAF86-87CD-4844-94BC-CEE861681760">GetDcHuffmanTable</a>
</td>
<td align="left" width="63%">
Retrieves a copy of the DC Huffman table for the specified scan and table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CE29251F-C2E2-422B-B6BD-034D6B479009">GetFrameHeader</a>
</td>
<td align="left" width="63%">
Retrieves  header data from the entire frame. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58A0FA55-7626-4FB7-BA35-1806B6C3AAAA">GetQuantizationTable</a>
</td>
<td align="left" width="63%">
Retrieves a copy of the quantization table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FD434498-CC04-4702-ACD3-EDD1DDE0B3AA">GetScanHeader</a>
</td>
<td align="left" width="63%">
Retrieves parameters from the Start Of Scan (SOS) marker for the scan with the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D97A48E5-0398-460C-AFA9-2E1B8744926B">SetIndexing</a>
</td>
<td align="left" width="63%">
Enables indexing of the JPEG for efficient random access.

</td>
</tr>
</table> 


## -remarks



Obtain this interface by calling <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a> on the Windows-provided <a href="https://msdn.microsoft.com/1498b800-6449-440f-bed7-85891637e559">IWICBitmapFrameDecoder</a> interface for the JPEG decoder.



