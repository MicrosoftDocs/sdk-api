---
UID: NF:wincodec.IWICBitmapDecoder.GetThumbnail
title: IWICBitmapDecoder::GetThumbnail (wincodec.h)
description: Retrieves a bitmap thumbnail of the image, if one exists
helpviewer_keywords: ["GetThumbnail","GetThumbnail method [Windows Imaging Component]","GetThumbnail method [Windows Imaging Component]","IWICBitmapDecoder interface","IWICBitmapDecoder interface [Windows Imaging Component]","GetThumbnail method","IWICBitmapDecoder.GetThumbnail","IWICBitmapDecoder::GetThumbnail","_wic_codec_iwicbitmapdecoder_getthumbnail","wic._wic_codec_iwicbitmapdecoder_getthumbnail","wincodec/IWICBitmapDecoder::GetThumbnail"]
old-location: wic\_wic_codec_iwicbitmapdecoder_getthumbnail.htm
tech.root: wic
ms.assetid: dbfe61d9-50ca-4d44-a8a3-2acae3413985
ms.date: 12/05/2018
ms.keywords: GetThumbnail, GetThumbnail method [Windows Imaging Component], GetThumbnail method [Windows Imaging Component],IWICBitmapDecoder interface, IWICBitmapDecoder interface [Windows Imaging Component],GetThumbnail method, IWICBitmapDecoder.GetThumbnail, IWICBitmapDecoder::GetThumbnail, _wic_codec_iwicbitmapdecoder_getthumbnail, wic._wic_codec_iwicbitmapdecoder_getthumbnail, wincodec/IWICBitmapDecoder::GetThumbnail
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
 - IWICBitmapDecoder::GetThumbnail
 - wincodec/IWICBitmapDecoder::GetThumbnail
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
 - IWICBitmapDecoder.GetThumbnail
---

# IWICBitmapDecoder::GetThumbnail


## -description

Retrieves a bitmap thumbnail of the image, if one exists

## -parameters

### -param ppIThumbnail [out]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a>**</b>

Receives a pointer to the <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a> of the thumbnail.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The returned thumbnail can be of any size, so the caller should scale the thumbnail to the desired size. The only Windows provided image formats that support thumbnails are JPEG, TIFF, and JPEG-XR. If the thumbnail is not available, this will return <a href="/windows/desktop/wic/-wic-codec-error-codes">WINCODEC_ERR_CODECNOTHUMBNAIL</a>.