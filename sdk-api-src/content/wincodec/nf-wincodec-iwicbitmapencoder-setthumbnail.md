---
UID: NF:wincodec.IWICBitmapEncoder.SetThumbnail
title: IWICBitmapEncoder::SetThumbnail
author: windows-sdk-content
description: Sets the global thumbnail for the image.
old-location: wic\_wic_codec_iwicbitmapencoder_setthumbnail.htm
tech.root: wic
ms.assetid: ecabfde8-0079-4059-8691-bbe3f0baa934
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IWICBitmapEncoder interface [Windows Imaging Component],SetThumbnail method, IWICBitmapEncoder.SetThumbnail, IWICBitmapEncoder::SetThumbnail, SetThumbnail, SetThumbnail method [Windows Imaging Component], SetThumbnail method [Windows Imaging Component],IWICBitmapEncoder interface, _wic_codec_iwicbitmapencoder_setthumbnail, wic._wic_codec_iwicbitmapencoder_setthumbnail, wincodec/IWICBitmapEncoder::SetThumbnail
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
 - IWICBitmapEncoder.SetThumbnail
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICBitmapEncoder::SetThumbnail


## -description


Sets the global thumbnail for the image.


## -parameters




### -param pIThumbnail [in]

Type: <b><a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a>*</b>

The <a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a> to set as the global thumbnail.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise.
            

Returns WINCODEC_ERR_UNSUPPORTEDOPERATION if the feature is not supported by the encoder.



