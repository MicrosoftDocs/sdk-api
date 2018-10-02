---
UID: NN:wincodec.IWICJpegFrameEncode
title: IWICJpegFrameEncode
author: windows-sdk-content
description: Exposes methods for writing compressed JPEG scan data directly to the WIC encoder's output stream. Also provides access to the Huffman and quantization tables.
old-location: wic\iwicjpegframeencode.htm
tech.root: wic
ms.assetid: 631571A2-AA15-4A4B-B705-6CCC81392A6A
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWICJpegFrameEncode, IWICJpegFrameEncode interface [Windows Imaging Component], IWICJpegFrameEncode interface [Windows Imaging Component],described, wic.iwicjpegframeencode, wincodec/IWICJpegFrameEncode
ms.prod: windows
ms.technology: windows-sdk
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
 - IWICJpegFrameEncode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICJpegFrameEncode interface


## -description


Exposes methods for writing compressed JPEG scan data directly to the WIC encoder's output stream. Also provides access to the Huffman and quantization tables.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICJpegFrameEncode</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWICJpegFrameEncode</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICJpegFrameEncode</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ABE4C1E-52C7-4F08-8479-CB4F6FEE9ADA">GetAcHuffmanTable</a>
</td>
<td align="left" width="63%">
Retrieves a copy of the AC Huffman table for the specified scan and table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ACEFFBD-2F58-427D-8DB9-907A088A127B">GetDcHuffmanTable</a>
</td>
<td align="left" width="63%">
Retrieves a copy of the DC Huffman table for the specified scan and table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6FBDAEA2-78E6-4152-815D-FA6164FE396F">GetQuantizationTable</a>
</td>
<td align="left" width="63%">
Retrieves a copy of the quantization table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FED02403-E696-4988-BFB6-F1E37D9FA5F1">WriteScan</a>
</td>
<td align="left" width="63%">
Writes scan data to a JPEG frame.

</td>
</tr>
</table> 


## -remarks



Obtain this interface by calling <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a> on the Windows-provided <a href="https://msdn.microsoft.com/a8de774b-3783-46be-9a21-c9fec2f10ffd">IWICBitmapFrameEncoder</a> interface for the JPEG encoder.

The WIC JPEG encoder supports a smaller subset of JPEG features than the decoder does.

<ul>
<li>The encoder is limited to a single scan. It does not support encoding images that are multi-scan, either for progressive encoding or planar component data.</li>
<li>The encoder supports two quantization tables, two AC Huffman tables, and two DC Huffman tables. The luma tables are used for the Y channel and, in the case of YCCK, the black channel.  The chroma tables are used for the CbCr channels. </li>
<li>The encoder supports encoding gray, YCbCr (RGB), and YCCK (CMYK).</li>
<li>The encoder supports 4 fixed compontent subsampling, 4:2:0, 4:2:2, 4:4:0, and 4:4:4.  This subsamples chroma only.</li>
<li>The encoder does not support  restart markers.</li>
</ul>


