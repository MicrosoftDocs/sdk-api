---
UID: NF:wincodec.IWICBitmapDecoder.GetFrameCount
title: IWICBitmapDecoder::GetFrameCount
author: windows-sdk-content
description: Retrieves the total number of frames in the image.
old-location: wic\_wic_codec_iwicbitmapdecoder_getframecount.htm
tech.root: wic
ms.assetid: 16eb613d-f649-436d-a121-e6468cd2581a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetFrameCount, GetFrameCount method [Windows Imaging Component], GetFrameCount method [Windows Imaging Component],IWICBitmapDecoder interface, IWICBitmapDecoder interface [Windows Imaging Component],GetFrameCount method, IWICBitmapDecoder.GetFrameCount, IWICBitmapDecoder::GetFrameCount, _wic_codec_iwicbitmapdecoder_getframecount, wic._wic_codec_iwicbitmapdecoder_getframecount, wincodec/IWICBitmapDecoder::GetFrameCount
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
 - IWICBitmapDecoder.GetFrameCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICBitmapDecoder::GetFrameCount


## -description


Retrieves the total number of frames in the image.


## -parameters




### -param pCount [out]

Type: <b>UINT*</b>

A pointer that receives the total number of frames in the image.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



