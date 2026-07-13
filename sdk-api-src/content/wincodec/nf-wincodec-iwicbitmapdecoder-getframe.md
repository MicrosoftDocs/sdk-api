---
UID: NF:wincodec.IWICBitmapDecoder.GetFrame
title: IWICBitmapDecoder::GetFrame (wincodec.h)
description: Retrieves the specified frame of the image.
helpviewer_keywords: ["GetFrame","GetFrame method [Windows Imaging Component]","GetFrame method [Windows Imaging Component]","IWICBitmapDecoder interface","IWICBitmapDecoder interface [Windows Imaging Component]","GetFrame method","IWICBitmapDecoder.GetFrame","IWICBitmapDecoder::GetFrame","_wic_codec_iwicbitmapdecoder_getframe","wic._wic_codec_iwicbitmapdecoder_getframe","wincodec/IWICBitmapDecoder::GetFrame"]
old-location: wic\_wic_codec_iwicbitmapdecoder_getframe.htm
tech.root: wic
ms.assetid: 5e8c1cfd-50f3-431c-aedb-6e57d1368695
ms.date: 12/05/2018
ms.keywords: GetFrame, GetFrame method [Windows Imaging Component], GetFrame method [Windows Imaging Component],IWICBitmapDecoder interface, IWICBitmapDecoder interface [Windows Imaging Component],GetFrame method, IWICBitmapDecoder.GetFrame, IWICBitmapDecoder::GetFrame, _wic_codec_iwicbitmapdecoder_getframe, wic._wic_codec_iwicbitmapdecoder_getframe, wincodec/IWICBitmapDecoder::GetFrame
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
 - IWICBitmapDecoder::GetFrame
 - wincodec/IWICBitmapDecoder::GetFrame
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
 - IWICBitmapDecoder.GetFrame
---

# IWICBitmapDecoder::GetFrame


## -description

Retrieves the specified frame of the image.

## -parameters

### -param index [in]

Type: <b>UINT</b>

The particular frame to retrieve.

### -param ppIBitmapFrame [out]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode">IWICBitmapFrameDecode</a>**</b>

A pointer that receives a pointer to the <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode">IWICBitmapFrameDecode</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.