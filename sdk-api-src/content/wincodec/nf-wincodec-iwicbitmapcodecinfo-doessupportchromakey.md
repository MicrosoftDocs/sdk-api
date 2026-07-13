---
UID: NF:wincodec.IWICBitmapCodecInfo.DoesSupportChromakey
title: IWICBitmapCodecInfo::DoesSupportChromakey (wincodec.h)
description: Retrieves a value indicating whether the codec supports chromakeys.
helpviewer_keywords: ["DoesSupportChromakey","DoesSupportChromakey method [Windows Imaging Component]","DoesSupportChromakey method [Windows Imaging Component]","IWICBitmapCodecInfo interface","IWICBitmapCodecInfo interface [Windows Imaging Component]","DoesSupportChromakey method","IWICBitmapCodecInfo.DoesSupportChromakey","IWICBitmapCodecInfo::DoesSupportChromakey","_wic_codec_iwicbitmapcodecinfo_doessupportchromakey","wic._wic_codec_iwicbitmapcodecinfo_doessupportchromakey","wincodec/IWICBitmapCodecInfo::DoesSupportChromakey"]
old-location: wic\_wic_codec_iwicbitmapcodecinfo_doessupportchromakey.htm
tech.root: wic
ms.assetid: 662e213e-1ed2-445c-a7be-ff8a137fba2e
ms.date: 12/05/2018
ms.keywords: DoesSupportChromakey, DoesSupportChromakey method [Windows Imaging Component], DoesSupportChromakey method [Windows Imaging Component],IWICBitmapCodecInfo interface, IWICBitmapCodecInfo interface [Windows Imaging Component],DoesSupportChromakey method, IWICBitmapCodecInfo.DoesSupportChromakey, IWICBitmapCodecInfo::DoesSupportChromakey, _wic_codec_iwicbitmapcodecinfo_doessupportchromakey, wic._wic_codec_iwicbitmapcodecinfo_doessupportchromakey, wincodec/IWICBitmapCodecInfo::DoesSupportChromakey
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
 - IWICBitmapCodecInfo::DoesSupportChromakey
 - wincodec/IWICBitmapCodecInfo::DoesSupportChromakey
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
 - IWICBitmapCodecInfo.DoesSupportChromakey
---

# IWICBitmapCodecInfo::DoesSupportChromakey


## -description

Retrieves a value indicating whether the codec supports chromakeys.

## -parameters

### -param pfSupportChromakey [out]

Type: <b>BOOL*</b>

Receives <b>TRUE</b> if the codec supports chromakeys; otherwise, <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

