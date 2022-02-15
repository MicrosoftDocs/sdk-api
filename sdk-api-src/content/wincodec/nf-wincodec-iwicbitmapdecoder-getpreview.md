---
UID: NF:wincodec.IWICBitmapDecoder.GetPreview
title: IWICBitmapDecoder::GetPreview (wincodec.h)
description: Retrieves a preview image, if supported.
helpviewer_keywords: ["GetPreview","GetPreview method [Windows Imaging Component]","GetPreview method [Windows Imaging Component]","IWICBitmapDecoder interface","IWICBitmapDecoder interface [Windows Imaging Component]","GetPreview method","IWICBitmapDecoder.GetPreview","IWICBitmapDecoder::GetPreview","_wic_codec_iwicbitmapdecoder_getpreview","wic._wic_codec_iwicbitmapdecoder_getpreview","wincodec/IWICBitmapDecoder::GetPreview"]
old-location: wic\_wic_codec_iwicbitmapdecoder_getpreview.htm
tech.root: wic
ms.assetid: 8e726eba-bb74-45b8-be6b-63d9ce00c272
ms.date: 12/05/2018
ms.keywords: GetPreview, GetPreview method [Windows Imaging Component], GetPreview method [Windows Imaging Component],IWICBitmapDecoder interface, IWICBitmapDecoder interface [Windows Imaging Component],GetPreview method, IWICBitmapDecoder.GetPreview, IWICBitmapDecoder::GetPreview, _wic_codec_iwicbitmapdecoder_getpreview, wic._wic_codec_iwicbitmapdecoder_getpreview, wincodec/IWICBitmapDecoder::GetPreview
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
 - IWICBitmapDecoder::GetPreview
 - wincodec/IWICBitmapDecoder::GetPreview
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
 - IWICBitmapDecoder.GetPreview
---

# IWICBitmapDecoder::GetPreview


## -description

Retrieves a preview image, if supported.

## -parameters

### -param ppIBitmapSource [out]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a>**</b>

Receives a pointer to the preview bitmap if supported.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Not all formats support previews. Only the native Microsoft Windows Digital Photo (WDP) codec support previews.