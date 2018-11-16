---
UID: NF:wincodec.IWICBitmapDecoder.Initialize
title: IWICBitmapDecoder::Initialize
author: windows-sdk-content
description: Initializes the decoder with the provided stream.
old-location: wic\_wic_codec_iwicbitmapdecoder_initialize.htm
tech.root: wic
ms.assetid: 60a7e0b8-202c-4fed-b105-f8c4fa9817a9
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IWICBitmapDecoder interface [Windows Imaging Component],Initialize method, IWICBitmapDecoder.Initialize, IWICBitmapDecoder::Initialize, Initialize, Initialize method [Windows Imaging Component], Initialize method [Windows Imaging Component],IWICBitmapDecoder interface, _wic_codec_iwicbitmapdecoder_initialize, wic._wic_codec_iwicbitmapdecoder_initialize, wincodec/IWICBitmapDecoder::Initialize
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWICBitmapDecoder.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wincodec.h
: 
- IWICBitmapDecoder.Initialize
: 
---

# IWICBitmapDecoder::Initialize


## -description


Initializes the decoder with the provided stream.


## -parameters




### -param pIStream [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

The stream to use for initialization.

The stream contains the encoded pixels which are decoded each time the <a href="https://msdn.microsoft.com/d4908a75-e7de-4b8f-bdc8-d86cf6b49f8c">CopyPixels</a> method on the <a href="https://msdn.microsoft.com/1498b800-6449-440f-bed7-85891637e559">IWICBitmapFrameDecode</a> interface (see <a href="https://msdn.microsoft.com/5e8c1cfd-50f3-431c-aedb-6e57d1368695">GetFrame</a>) is invoked.


### -param cacheOptions [in]

Type: <b><a href="https://msdn.microsoft.com/27b9d6e1-e171-4c7f-8f96-fa5a93923e35">WICDecodeOptions</a></b>

The <a href="https://msdn.microsoft.com/27b9d6e1-e171-4c7f-8f96-fa5a93923e35">WICDecodeOptions</a> to use for initialization.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



