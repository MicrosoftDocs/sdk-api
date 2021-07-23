---
UID: NF:wincodec.IWICBitmapCodecInfo.DoesSupportAnimation
title: IWICBitmapCodecInfo::DoesSupportAnimation (wincodec.h)
description: Retrieves a value indicating whether the codec supports animation.
helpviewer_keywords: ["DoesSupportAnimation","DoesSupportAnimation method [Windows Imaging Component]","DoesSupportAnimation method [Windows Imaging Component]","IWICBitmapCodecInfo interface","IWICBitmapCodecInfo interface [Windows Imaging Component]","DoesSupportAnimation method","IWICBitmapCodecInfo.DoesSupportAnimation","IWICBitmapCodecInfo::DoesSupportAnimation","_wic_codec_iwicbitmapcodecinfo_doessupportanimation","wic._wic_codec_iwicbitmapcodecinfo_doessupportanimation","wincodec/IWICBitmapCodecInfo::DoesSupportAnimation"]
old-location: wic\_wic_codec_iwicbitmapcodecinfo_doessupportanimation.htm
tech.root: wic
ms.assetid: 17635459-e067-4fdb-a801-4ad6cc622215
ms.date: 12/05/2018
ms.keywords: DoesSupportAnimation, DoesSupportAnimation method [Windows Imaging Component], DoesSupportAnimation method [Windows Imaging Component],IWICBitmapCodecInfo interface, IWICBitmapCodecInfo interface [Windows Imaging Component],DoesSupportAnimation method, IWICBitmapCodecInfo.DoesSupportAnimation, IWICBitmapCodecInfo::DoesSupportAnimation, _wic_codec_iwicbitmapcodecinfo_doessupportanimation, wic._wic_codec_iwicbitmapcodecinfo_doessupportanimation, wincodec/IWICBitmapCodecInfo::DoesSupportAnimation
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
 - IWICBitmapCodecInfo::DoesSupportAnimation
 - wincodec/IWICBitmapCodecInfo::DoesSupportAnimation
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
 - IWICBitmapCodecInfo.DoesSupportAnimation
---

# IWICBitmapCodecInfo::DoesSupportAnimation


## -description

Retrieves a value indicating whether the codec supports animation.

## -parameters

### -param pfSupportAnimation [out]

Type: <b>BOOL*</b>

Receives <b>TRUE</b> if the codec supports images with timing information; otherwise, <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

