---
UID: NF:wincodec.IWICBitmapEncoderInfo.CreateInstance
title: IWICBitmapEncoderInfo::CreateInstance method
author: windows-driver-content
description: Creates a new IWICBitmapEncoder instance.
old-location: wic\_wic_codec_iwicbitmapencoderinfo_createinstance.htm
old-project: wic
ms.assetid: 333663d2-9b71-44ee-bf58-f6f283666b78
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: CreateInstance method [Windows Imaging Component], CreateInstance method [Windows Imaging Component], IWICBitmapEncoderInfo interface, CreateInstance,IWICBitmapEncoderInfo.CreateInstance, IWICBitmapEncoderInfo, IWICBitmapEncoderInfo interface [Windows Imaging Component], CreateInstance method, IWICBitmapEncoderInfo::CreateInstance, _wic_codec_iwicbitmapencoderinfo_createinstance, wic._wic_codec_iwicbitmapencoderinfo_createinstance, wincodec/IWICBitmapEncoderInfo::CreateInstance
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WICTiffCompressionOption
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.dll
api_name:
-	IWICBitmapEncoderInfo.CreateInstance
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICBitmapEncoderInfo::CreateInstance method


## -description


Creates a new <a href="https://msdn.microsoft.com/fe87c9ae-dedf-4ec2-ac11-0ea5fc6aa3ad">IWICBitmapEncoder</a> instance.


## -parameters




### -param ppIBitmapEncoder [out]

Type: <b><a href="https://msdn.microsoft.com/fe87c9ae-dedf-4ec2-ac11-0ea5fc6aa3ad">IWICBitmapEncoder</a>**</b>

A pointer that receives a pointer to a new <a href="https://msdn.microsoft.com/fe87c9ae-dedf-4ec2-ac11-0ea5fc6aa3ad">IWICBitmapEncoder</a> instance. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



