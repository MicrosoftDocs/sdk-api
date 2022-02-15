---
UID: NF:wincodec.IWICBitmapDecoder.Initialize
title: IWICBitmapDecoder::Initialize (wincodec.h)
description: Initializes the decoder with the provided stream.
helpviewer_keywords: ["IWICBitmapDecoder interface [Windows Imaging Component]","Initialize method","IWICBitmapDecoder.Initialize","IWICBitmapDecoder::Initialize","Initialize","Initialize method [Windows Imaging Component]","Initialize method [Windows Imaging Component]","IWICBitmapDecoder interface","_wic_codec_iwicbitmapdecoder_initialize","wic._wic_codec_iwicbitmapdecoder_initialize","wincodec/IWICBitmapDecoder::Initialize"]
old-location: wic\_wic_codec_iwicbitmapdecoder_initialize.htm
tech.root: wic
ms.assetid: 60a7e0b8-202c-4fed-b105-f8c4fa9817a9
ms.date: 12/05/2018
ms.keywords: IWICBitmapDecoder interface [Windows Imaging Component],Initialize method, IWICBitmapDecoder.Initialize, IWICBitmapDecoder::Initialize, Initialize, Initialize method [Windows Imaging Component], Initialize method [Windows Imaging Component],IWICBitmapDecoder interface, _wic_codec_iwicbitmapdecoder_initialize, wic._wic_codec_iwicbitmapdecoder_initialize, wincodec/IWICBitmapDecoder::Initialize
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICBitmapDecoder::Initialize
 - wincodec/IWICBitmapDecoder::Initialize
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
 - IWICBitmapDecoder.Initialize
---

# IWICBitmapDecoder::Initialize


## -description

Initializes the decoder with the provided stream.

## -parameters

### -param pIStream [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

The stream to use for initialization.

The stream contains the encoded pixels which are decoded each time the <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-copypixels">CopyPixels</a> method on the <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode">IWICBitmapFrameDecode</a> interface (see <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoder-getframe">GetFrame</a>) is invoked.

### -param cacheOptions [in]

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicdecodeoptions">WICDecodeOptions</a></b>

The <a href="/windows/desktop/api/wincodec/ne-wincodec-wicdecodeoptions">WICDecodeOptions</a> to use for initialization.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.