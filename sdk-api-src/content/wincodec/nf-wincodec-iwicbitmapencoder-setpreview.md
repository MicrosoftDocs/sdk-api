---
UID: NF:wincodec.IWICBitmapEncoder.SetPreview
title: IWICBitmapEncoder::SetPreview (wincodec.h)
description: Sets the global preview for the image.
helpviewer_keywords: ["IWICBitmapEncoder interface [Windows Imaging Component]","SetPreview method","IWICBitmapEncoder.SetPreview","IWICBitmapEncoder::SetPreview","SetPreview","SetPreview method [Windows Imaging Component]","SetPreview method [Windows Imaging Component]","IWICBitmapEncoder interface","_wic_codec_iwicbitmapencoder_setpreview","wic._wic_codec_iwicbitmapencoder_setpreview","wincodec/IWICBitmapEncoder::SetPreview"]
old-location: wic\_wic_codec_iwicbitmapencoder_setpreview.htm
tech.root: wic
ms.assetid: ca02236d-9434-4db5-84af-9331f23e20a7
ms.date: 12/05/2018
ms.keywords: IWICBitmapEncoder interface [Windows Imaging Component],SetPreview method, IWICBitmapEncoder.SetPreview, IWICBitmapEncoder::SetPreview, SetPreview, SetPreview method [Windows Imaging Component], SetPreview method [Windows Imaging Component],IWICBitmapEncoder interface, _wic_codec_iwicbitmapencoder_setpreview, wic._wic_codec_iwicbitmapencoder_setpreview, wincodec/IWICBitmapEncoder::SetPreview
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
 - IWICBitmapEncoder::SetPreview
 - wincodec/IWICBitmapEncoder::SetPreview
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
 - IWICBitmapEncoder.SetPreview
---

# IWICBitmapEncoder::SetPreview


## -description

Sets the global preview for the image.

## -parameters

### -param pIPreview [in]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a>*</b>

The <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a> to use as the global preview.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise.
            

Returns WINCODEC_ERR_UNSUPPORTEDOPERATION if the feature is not supported by the encoder.