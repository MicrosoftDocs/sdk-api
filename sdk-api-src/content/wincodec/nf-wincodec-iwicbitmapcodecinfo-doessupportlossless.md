---
UID: NF:wincodec.IWICBitmapCodecInfo.DoesSupportLossless
title: IWICBitmapCodecInfo::DoesSupportLossless (wincodec.h)
description: Retrieves a value indicating whether the codec supports lossless formats.
helpviewer_keywords: ["DoesSupportLossless","DoesSupportLossless method [Windows Imaging Component]","DoesSupportLossless method [Windows Imaging Component]","IWICBitmapCodecInfo interface","IWICBitmapCodecInfo interface [Windows Imaging Component]","DoesSupportLossless method","IWICBitmapCodecInfo.DoesSupportLossless","IWICBitmapCodecInfo::DoesSupportLossless","_wic_codec_iwicbitmapcodecinfo_doessupportlossless","wic._wic_codec_iwicbitmapcodecinfo_doessupportlossless","wincodec/IWICBitmapCodecInfo::DoesSupportLossless"]
old-location: wic\_wic_codec_iwicbitmapcodecinfo_doessupportlossless.htm
tech.root: wic
ms.assetid: 90a1f4cf-2641-4033-a369-ad6bf6fe5f43
ms.date: 12/05/2018
ms.keywords: DoesSupportLossless, DoesSupportLossless method [Windows Imaging Component], DoesSupportLossless method [Windows Imaging Component],IWICBitmapCodecInfo interface, IWICBitmapCodecInfo interface [Windows Imaging Component],DoesSupportLossless method, IWICBitmapCodecInfo.DoesSupportLossless, IWICBitmapCodecInfo::DoesSupportLossless, _wic_codec_iwicbitmapcodecinfo_doessupportlossless, wic._wic_codec_iwicbitmapcodecinfo_doessupportlossless, wincodec/IWICBitmapCodecInfo::DoesSupportLossless
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
 - IWICBitmapCodecInfo::DoesSupportLossless
 - wincodec/IWICBitmapCodecInfo::DoesSupportLossless
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
 - IWICBitmapCodecInfo.DoesSupportLossless
---

# IWICBitmapCodecInfo::DoesSupportLossless


## -description

Retrieves a value indicating whether the codec supports lossless formats.

## -parameters

### -param pfSupportLossless [out]

Type: <b>BOOL*</b>

Receives <b>TRUE</b> if the codec supports lossless formats; otherwise, <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

