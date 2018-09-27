---
UID: NF:wincodec.IWICBitmapCodecInfo.DoesSupportChromakey
title: IWICBitmapCodecInfo::DoesSupportChromakey
author: windows-sdk-content
description: Retrieves a value indicating whether the codec supports chromakeys.
old-location: wic\_wic_codec_iwicbitmapcodecinfo_doessupportchromakey.htm
tech.root: wic
ms.assetid: 662e213e-1ed2-445c-a7be-ff8a137fba2e
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: DoesSupportChromakey, DoesSupportChromakey method [Windows Imaging Component], DoesSupportChromakey method [Windows Imaging Component],IWICBitmapCodecInfo interface, IWICBitmapCodecInfo interface [Windows Imaging Component],DoesSupportChromakey method, IWICBitmapCodecInfo.DoesSupportChromakey, IWICBitmapCodecInfo::DoesSupportChromakey, _wic_codec_iwicbitmapcodecinfo_doessupportchromakey, wic._wic_codec_iwicbitmapcodecinfo_doessupportchromakey, wincodec/IWICBitmapCodecInfo::DoesSupportChromakey
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
 - IWICBitmapCodecInfo.DoesSupportChromakey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



