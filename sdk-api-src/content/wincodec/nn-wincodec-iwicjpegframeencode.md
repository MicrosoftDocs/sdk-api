---
UID: NN:wincodec.IWICJpegFrameEncode
title: IWICJpegFrameEncode (wincodec.h)
description: Exposes methods for writing compressed JPEG scan data directly to the WIC encoder's output stream. Also provides access to the Huffman and quantization tables.
helpviewer_keywords: ["IWICJpegFrameEncode","IWICJpegFrameEncode interface [Windows Imaging Component]","IWICJpegFrameEncode interface [Windows Imaging Component]","described","wic.iwicjpegframeencode","wincodec/IWICJpegFrameEncode"]
old-location: wic\iwicjpegframeencode.htm
tech.root: wic
ms.assetid: 631571A2-AA15-4A4B-B705-6CCC81392A6A
ms.date: 12/05/2018
ms.keywords: IWICJpegFrameEncode, IWICJpegFrameEncode interface [Windows Imaging Component], IWICJpegFrameEncode interface [Windows Imaging Component],described, wic.iwicjpegframeencode, wincodec/IWICJpegFrameEncode
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICJpegFrameEncode
 - wincodec/IWICJpegFrameEncode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICJpegFrameEncode
---

# IWICJpegFrameEncode interface


## -description

Exposes methods for writing compressed JPEG scan data directly to the WIC encoder's output stream. Also provides access to the Huffman and quantization tables.

## -inheritance

The <b>IWICJpegFrameEncode</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICJpegFrameEncode</b> also has these types of members:

## -remarks

Obtain this interface by calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> on the Windows-provided <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframeencode">IWICBitmapFrameEncoder</a> interface for the JPEG encoder.

The WIC JPEG encoder supports a smaller subset of JPEG features than the decoder does.

<ul>
<li>The encoder is limited to a single scan. It does not support encoding images that are multi-scan, either for progressive encoding or planar component data.</li>
<li>The encoder supports two quantization tables, two AC Huffman tables, and two DC Huffman tables. The luma tables are used for the Y channel and, in the case of YCCK, the black channel.  The chroma tables are used for the CbCr channels. </li>
<li>The encoder supports encoding gray, YCbCr (RGB), and YCCK (CMYK).</li>
<li>The encoder supports 4 fixed component subsampling, 4:2:0, 4:2:2, 4:4:0, and 4:4:4.  This subsamples chroma only.</li>
<li>The encoder does not support restart markers.</li>
</ul>
