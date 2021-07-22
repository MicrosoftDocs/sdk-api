---
UID: NN:wincodec.IWICJpegFrameDecode
title: IWICJpegFrameDecode (wincodec.h)
description: Exposes methods for decoding JPEG images. Provides access to the Start Of Frame (SOF) header, Start of Scan (SOS) header, the Huffman and Quantization tables, and the compressed JPEG JPEG data. Also enables indexing for efficient random access.
helpviewer_keywords: ["IWICJpegFrameDecode","IWICJpegFrameDecode interface [Windows Imaging Component]","IWICJpegFrameDecode interface [Windows Imaging Component]","described","wic.iwicjpegframedecode","wincodec/IWICJpegFrameDecode"]
old-location: wic\iwicjpegframedecode.htm
tech.root: wic
ms.assetid: E6310320-53A8-40F1-8964-D21D8054E1B8
ms.date: 12/05/2018
ms.keywords: IWICJpegFrameDecode, IWICJpegFrameDecode interface [Windows Imaging Component], IWICJpegFrameDecode interface [Windows Imaging Component],described, wic.iwicjpegframedecode, wincodec/IWICJpegFrameDecode
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
 - IWICJpegFrameDecode
 - wincodec/IWICJpegFrameDecode
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
 - IWICJpegFrameDecode
---

# IWICJpegFrameDecode interface


## -description

Exposes methods for decoding JPEG images. Provides access to the Start Of Frame (SOF) header, Start of Scan (SOS) header, the Huffman and Quantization tables, and the compressed JPEG JPEG data. Also enables indexing for efficient random access.

## -inheritance

The <b>IWICJpegFrameDecode</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICJpegFrameDecode</b> also has these types of members:

## -remarks

Obtain this interface by calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> on the Windows-provided <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode">IWICBitmapFrameDecoder</a> interface for the JPEG decoder.
