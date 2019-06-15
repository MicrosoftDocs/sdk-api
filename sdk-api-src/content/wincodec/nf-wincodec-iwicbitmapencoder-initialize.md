---
UID: NF:wincodec.IWICBitmapEncoder.Initialize
title: IWICBitmapEncoder::Initialize (wincodec.h)
author: windows-sdk-content
description: Initializes the encoder with an IStream which tells the encoder where to encode the bits.
old-location: wic\_wic_codec_iwicbitmapencoder_initialize.htm
tech.root: wic
ms.assetid: 344a9a9d-8557-4ae8-9604-4040c7d7095a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWICBitmapEncoder interface [Windows Imaging Component],Initialize method, IWICBitmapEncoder.Initialize, IWICBitmapEncoder::Initialize, Initialize, Initialize method [Windows Imaging Component], Initialize method [Windows Imaging Component],IWICBitmapEncoder interface, _wic_codec_iwicbitmapencoder_initialize, wic._wic_codec_iwicbitmapencoder_initialize, wincodec/IWICBitmapEncoder::Initialize
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICBitmapEncoder.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICBitmapEncoder::Initialize


## -description


Initializes the encoder with an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> which tells the encoder where to encode the bits.


## -parameters




### -param pIStream [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

The output stream.


### -param cacheOption [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/wincodec/ne-wincodec-wicbitmapencodercacheoption">WICBitmapEncoderCacheOption</a></b>

The <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/ne-wincodec-wicbitmapencodercacheoption">WICBitmapEncoderCacheOption</a> used on initialization.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



