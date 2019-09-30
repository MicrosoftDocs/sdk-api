---
UID: NF:wincodec.IWICBitmapEncoderInfo.CreateInstance
title: IWICBitmapEncoderInfo::CreateInstance (wincodec.h)
author: windows-sdk-content
description: Creates a new IWICBitmapEncoder instance.
old-location: wic\_wic_codec_iwicbitmapencoderinfo_createinstance.htm
tech.root: wic
ms.assetid: 333663d2-9b71-44ee-bf58-f6f283666b78
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateInstance, CreateInstance method [Windows Imaging Component], CreateInstance method [Windows Imaging Component],IWICBitmapEncoderInfo interface, IWICBitmapEncoderInfo interface [Windows Imaging Component],CreateInstance method, IWICBitmapEncoderInfo.CreateInstance, IWICBitmapEncoderInfo::CreateInstance, _wic_codec_iwicbitmapencoderinfo_createinstance, wic._wic_codec_iwicbitmapencoderinfo_createinstance, wincodec/IWICBitmapEncoderInfo::CreateInstance
ms.topic: method
f1_keywords: 
 - "wincodec/IWICBitmapEncoderInfo.CreateInstance"
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
 - IWICBitmapEncoderInfo.CreateInstance
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICBitmapEncoderInfo::CreateInstance


## -description


Creates a new <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder">IWICBitmapEncoder</a> instance.


## -parameters




### -param ppIBitmapEncoder [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder">IWICBitmapEncoder</a>**</b>

A pointer that receives a pointer to a new <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder">IWICBitmapEncoder</a> instance. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



