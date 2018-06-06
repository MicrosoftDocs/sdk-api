---
UID: NF:wincodec.IWICBitmapEncoder.GetEncoderInfo
title: IWICBitmapEncoder::GetEncoderInfo
author: windows-sdk-content
description: Retrieves an IWICBitmapEncoderInfo for the encoder.
old-location: wic\_wic_codec_iwicbitmapencoder_getencoderinfo.htm
old-project: wic
ms.assetid: af723a68-89c8-4d0c-88ef-cda4abaad6f7
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetEncoderInfo, GetEncoderInfo method [Windows Imaging Component], GetEncoderInfo method [Windows Imaging Component],IWICBitmapEncoder interface, IWICBitmapEncoder interface [Windows Imaging Component],GetEncoderInfo method, IWICBitmapEncoder.GetEncoderInfo, IWICBitmapEncoder::GetEncoderInfo, _wic_codec_iwicbitmapencoder_getencoderinfo, wic._wic_codec_iwicbitmapencoder_getencoderinfo, wincodec/IWICBitmapEncoder::GetEncoderInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WICTiffCompressionOption
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICBitmapEncoder.GetEncoderInfo
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICBitmapEncoder::GetEncoderInfo


## -description


Retrieves an <a href="https://msdn.microsoft.com/152b0dd2-1e5e-47fc-b6eb-a4c042e65047">IWICBitmapEncoderInfo</a> for the encoder.


## -parameters




### -param ppIEncoderInfo [out]

Type: <b><a href="https://msdn.microsoft.com/152b0dd2-1e5e-47fc-b6eb-a4c042e65047">IWICBitmapEncoderInfo</a>**</b>

A pointer that receives a pointer to an <a href="https://msdn.microsoft.com/152b0dd2-1e5e-47fc-b6eb-a4c042e65047">IWICBitmapEncoderInfo</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



