---
UID: NN:wincodec.IWICJpegFrameDecode
title: IWICJpegFrameDecode (wincodec.h)
description: Exposes methods for decoding JPEG images. Provides access to the Start Of Frame (SOF) header, Start of Scan (SOS) header, the Huffman and Quantization tables, and the compressed JPEG JPEG data. Also enables indexing for efficient random access.
old-location: wic\iwicjpegframedecode.htm
tech.root: wic
ms.assetid: E6310320-53A8-40F1-8964-D21D8054E1B8
ms.date: 12/05/2018
ms.keywords: IWICJpegFrameDecode, IWICJpegFrameDecode interface [Windows Imaging Component], IWICJpegFrameDecode interface [Windows Imaging Component],described, wic.iwicjpegframedecode, wincodec/IWICJpegFrameDecode
f1_keywords:
- wincodec/IWICJpegFrameDecode
dev_langs:
- c++
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
- IWICJpegFrameDecode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICJpegFrameDecode interface


## -description


Exposes methods for decoding JPEG images. Provides access to the Start Of Frame (SOF) header, Start of Scan (SOS) header, the Huffman and Quantization tables, and the compressed JPEG JPEG data. Also enables indexing for efficient random access. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICJpegFrameDecode</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICJpegFrameDecode</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicjpegframedecode-clearindexing">ClearIndexing</a>
</td>
<td align="left" width="63%">
Removes the indexing from a JPEG that has been indexed using <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicjpegframedecode-setindexing">IWICJpegFrameDecode::SetIndexing</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicjpegframedecode-copyscan">CopyScan</a>
</td>
<td align="left" width="63%">
Retrieves a copy of the compressed JPEG scan directly from the WIC decoder frame's output stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicjpegframedecode-doessupportindexing">DoesSupportIndexing</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether this decoder supports indexing for efficient random access.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicjpegframedecode-getachuffmantable">GetAcHuffmanTable</a>
</td>
<td align="left" width="63%">
Retrieves a copy of the AC Huffman table for the specified scan and table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicjpegframedecode-getdchuffmantable">GetDcHuffmanTable</a>
</td>
<td align="left" width="63%">
Retrieves a copy of the DC Huffman table for the specified scan and table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicjpegframedecode-getframeheader">GetFrameHeader</a>
</td>
<td align="left" width="63%">
Retrieves  header data from the entire frame. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicjpegframedecode-getquantizationtable">GetQuantizationTable</a>
</td>
<td align="left" width="63%">
Retrieves a copy of the quantization table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicjpegframedecode-getscanheader">GetScanHeader</a>
</td>
<td align="left" width="63%">
Retrieves parameters from the Start Of Scan (SOS) marker for the scan with the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicjpegframedecode-setindexing">SetIndexing</a>
</td>
<td align="left" width="63%">
Enables indexing of the JPEG for efficient random access.

</td>
</tr>
</table> 


## -remarks



Obtain this interface by calling <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> on the Windows-provided <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode">IWICBitmapFrameDecoder</a> interface for the JPEG decoder.



