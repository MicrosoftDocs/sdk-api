---
UID: NF:wincodec.IWICBitmapEncoder.Initialize
title: IWICBitmapEncoder::Initialize (wincodec.h)
description: Initializes the encoder with an IStream which tells the encoder where to encode the bits.
helpviewer_keywords: ["IWICBitmapEncoder interface [Windows Imaging Component]","Initialize method","IWICBitmapEncoder.Initialize","IWICBitmapEncoder::Initialize","Initialize","Initialize method [Windows Imaging Component]","Initialize method [Windows Imaging Component]","IWICBitmapEncoder interface","_wic_codec_iwicbitmapencoder_initialize","wic._wic_codec_iwicbitmapencoder_initialize","wincodec/IWICBitmapEncoder::Initialize"]
old-location: wic\_wic_codec_iwicbitmapencoder_initialize.htm
tech.root: wic
ms.assetid: 344a9a9d-8557-4ae8-9604-4040c7d7095a
ms.date: 12/05/2018
ms.keywords: IWICBitmapEncoder interface [Windows Imaging Component],Initialize method, IWICBitmapEncoder.Initialize, IWICBitmapEncoder::Initialize, Initialize, Initialize method [Windows Imaging Component], Initialize method [Windows Imaging Component],IWICBitmapEncoder interface, _wic_codec_iwicbitmapencoder_initialize, wic._wic_codec_iwicbitmapencoder_initialize, wincodec/IWICBitmapEncoder::Initialize
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
 - IWICBitmapEncoder::Initialize
 - wincodec/IWICBitmapEncoder::Initialize
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
 - IWICBitmapEncoder.Initialize
---

# IWICBitmapEncoder::Initialize


## -description

Initializes the encoder with an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> which tells the encoder where to encode the bits.

## -parameters

### -param pIStream [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

The output stream.

### -param cacheOption [in]

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicbitmapencodercacheoption">WICBitmapEncoderCacheOption</a></b>

The <a href="/windows/desktop/api/wincodec/ne-wincodec-wicbitmapencodercacheoption">WICBitmapEncoderCacheOption</a> used on initialization.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.