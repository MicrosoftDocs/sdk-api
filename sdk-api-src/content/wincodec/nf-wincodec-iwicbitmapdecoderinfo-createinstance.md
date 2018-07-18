---
UID: NF:wincodec.IWICBitmapDecoderInfo.CreateInstance
title: IWICBitmapDecoderInfo::CreateInstance
author: windows-sdk-content
description: Creates a new IWICBitmapDecoder instance.
old-location: wic\_wic_codec_iwicbitmapdecoderinfo_createinstance.htm
old-project: wic
ms.assetid: 2bda1c2a-47b9-4e15-b0c1-52e3f85a6523
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: CreateInstance, CreateInstance method [Windows Imaging Component], CreateInstance method [Windows Imaging Component],IWICBitmapDecoderInfo interface, IWICBitmapDecoderInfo interface [Windows Imaging Component],CreateInstance method, IWICBitmapDecoderInfo.CreateInstance, IWICBitmapDecoderInfo::CreateInstance, _wic_codec_iwicbitmapdecoderinfo_createinstance, wic._wic_codec_iwicbitmapdecoderinfo_createinstance, wincodec/IWICBitmapDecoderInfo::CreateInstance
ms.prod: windows
ms.technology: windows-sdk
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
 - IWICBitmapDecoderInfo.CreateInstance
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICBitmapDecoderInfo::CreateInstance


## -description


Creates a new <a href="https://msdn.microsoft.com/91dafd5e-e4fb-4691-a3d0-ca8b6ff0aaf7">IWICBitmapDecoder</a> instance.


## -parameters




### -param ppIBitmapDecoder [out]

Type: <b><a href="https://msdn.microsoft.com/91dafd5e-e4fb-4691-a3d0-ca8b6ff0aaf7">IWICBitmapDecoder</a>**</b>

A pointer that receives a pointer to a new instance of the <a href="https://msdn.microsoft.com/91dafd5e-e4fb-4691-a3d0-ca8b6ff0aaf7">IWICBitmapDecoder</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



