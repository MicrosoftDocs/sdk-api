---
UID: NF:wincodec.IWICBitmapCodecInfo.DoesSupportMultiframe
title: IWICBitmapCodecInfo::DoesSupportMultiframe
author: windows-sdk-content
description: Retrieves a value indicating whether the codec supports multi frame images.
old-location: wic\_wic_codec_iwicbitmapcodecinfo_doessupportmultiframe.htm
old-project: wic
ms.assetid: b20bceb4-71aa-4ef6-865a-0afb4850e316
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DoesSupportMultiframe, DoesSupportMultiframe method [Windows Imaging Component], DoesSupportMultiframe method [Windows Imaging Component],IWICBitmapCodecInfo interface, IWICBitmapCodecInfo interface [Windows Imaging Component],DoesSupportMultiframe method, IWICBitmapCodecInfo.DoesSupportMultiframe, IWICBitmapCodecInfo::DoesSupportMultiframe, _wic_codec_iwicbitmapcodecinfo_doessupportmultiframe, wic._wic_codec_iwicbitmapcodecinfo_doessupportmultiframe, wincodec/IWICBitmapCodecInfo::DoesSupportMultiframe
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.redist: 
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
 - IWICBitmapCodecInfo.DoesSupportMultiframe
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICBitmapCodecInfo::DoesSupportMultiframe


## -description


Retrieves a value indicating whether the codec supports multi frame images.


## -parameters




### -param pfSupportMultiframe [out]

Type: <b>BOOL*</b>

Receives <b>TRUE</b> if the codec supports multi frame images; otherwise, <b>FALSE</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



