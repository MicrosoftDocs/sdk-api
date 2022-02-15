---
UID: NF:wincodec.IWICBitmapDecoderInfo.CreateInstance
title: IWICBitmapDecoderInfo::CreateInstance (wincodec.h)
description: Creates a new IWICBitmapDecoder instance.
helpviewer_keywords: ["CreateInstance","CreateInstance method [Windows Imaging Component]","CreateInstance method [Windows Imaging Component]","IWICBitmapDecoderInfo interface","IWICBitmapDecoderInfo interface [Windows Imaging Component]","CreateInstance method","IWICBitmapDecoderInfo.CreateInstance","IWICBitmapDecoderInfo::CreateInstance","_wic_codec_iwicbitmapdecoderinfo_createinstance","wic._wic_codec_iwicbitmapdecoderinfo_createinstance","wincodec/IWICBitmapDecoderInfo::CreateInstance"]
old-location: wic\_wic_codec_iwicbitmapdecoderinfo_createinstance.htm
tech.root: wic
ms.assetid: 2bda1c2a-47b9-4e15-b0c1-52e3f85a6523
ms.date: 12/05/2018
ms.keywords: CreateInstance, CreateInstance method [Windows Imaging Component], CreateInstance method [Windows Imaging Component],IWICBitmapDecoderInfo interface, IWICBitmapDecoderInfo interface [Windows Imaging Component],CreateInstance method, IWICBitmapDecoderInfo.CreateInstance, IWICBitmapDecoderInfo::CreateInstance, _wic_codec_iwicbitmapdecoderinfo_createinstance, wic._wic_codec_iwicbitmapdecoderinfo_createinstance, wincodec/IWICBitmapDecoderInfo::CreateInstance
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
 - IWICBitmapDecoderInfo::CreateInstance
 - wincodec/IWICBitmapDecoderInfo::CreateInstance
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
 - IWICBitmapDecoderInfo.CreateInstance
---

# IWICBitmapDecoderInfo::CreateInstance


## -description

Creates a new <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder">IWICBitmapDecoder</a> instance.

## -parameters

### -param ppIBitmapDecoder [out]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder">IWICBitmapDecoder</a>**</b>

A pointer that receives a pointer to a new instance of the <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder">IWICBitmapDecoder</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.