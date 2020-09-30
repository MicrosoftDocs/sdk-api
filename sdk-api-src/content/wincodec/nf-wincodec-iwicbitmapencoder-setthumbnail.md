---
UID: NF:wincodec.IWICBitmapEncoder.SetThumbnail
title: IWICBitmapEncoder::SetThumbnail (wincodec.h)
description: Sets the global thumbnail for the image.
helpviewer_keywords: ["IWICBitmapEncoder interface [Windows Imaging Component]","SetThumbnail method","IWICBitmapEncoder.SetThumbnail","IWICBitmapEncoder::SetThumbnail","SetThumbnail","SetThumbnail method [Windows Imaging Component]","SetThumbnail method [Windows Imaging Component]","IWICBitmapEncoder interface","_wic_codec_iwicbitmapencoder_setthumbnail","wic._wic_codec_iwicbitmapencoder_setthumbnail","wincodec/IWICBitmapEncoder::SetThumbnail"]
old-location: wic\_wic_codec_iwicbitmapencoder_setthumbnail.htm
tech.root: wic
ms.assetid: ecabfde8-0079-4059-8691-bbe3f0baa934
ms.date: 12/05/2018
ms.keywords: IWICBitmapEncoder interface [Windows Imaging Component],SetThumbnail method, IWICBitmapEncoder.SetThumbnail, IWICBitmapEncoder::SetThumbnail, SetThumbnail, SetThumbnail method [Windows Imaging Component], SetThumbnail method [Windows Imaging Component],IWICBitmapEncoder interface, _wic_codec_iwicbitmapencoder_setthumbnail, wic._wic_codec_iwicbitmapencoder_setthumbnail, wincodec/IWICBitmapEncoder::SetThumbnail
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
 - IWICBitmapEncoder::SetThumbnail
 - wincodec/IWICBitmapEncoder::SetThumbnail
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
 - IWICBitmapEncoder.SetThumbnail
---

# IWICBitmapEncoder::SetThumbnail


## -description

Sets the global thumbnail for the image.

## -parameters

### -param pIThumbnail [in]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a>*</b>

The <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a> to set as the global thumbnail.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise.
            

Returns WINCODEC_ERR_UNSUPPORTEDOPERATION if the feature is not supported by the encoder.