---
UID: NF:wincodec.IWICBitmapSource.GetSize
title: IWICBitmapSource::GetSize
author: windows-sdk-content
description: Retrieves the pixel width and height of the bitmap.
old-location: wic\_wic_codec_iwicbitmapsource_getsize.htm
tech.root: wic
ms.assetid: 2fba35fd-288c-4095-83b8-d2320dc5916c
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetSize, GetSize method [Windows Imaging Component], GetSize method [Windows Imaging Component],IWICBitmapSource interface, IWICBitmapSource interface [Windows Imaging Component],GetSize method, IWICBitmapSource.GetSize, IWICBitmapSource::GetSize, _wic_codec_iwicbitmapsource_getsize, wic._wic_codec_iwicbitmapsource_getsize, wincodec/IWICBitmapSource::GetSize
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
 - IWICBitmapSource.GetSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICBitmapSource::GetSize


## -description


Retrieves the pixel width and height of the bitmap.


## -parameters




### -param puiWidth [out]

Type: <b>UINT*</b>

A pointer that receives the pixel width of the bitmap.


### -param puiHeight [out]

Type: <b>UINT*</b>

A pointer that receives the pixel height of the bitmap


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



