---
UID: NF:wincodec.IWICBitmapDecoder.GetThumbnail
title: IWICBitmapDecoder::GetThumbnail
author: windows-sdk-content
description: Retrieves a bitmap thumbnail of the image, if one exists
old-location: wic\_wic_codec_iwicbitmapdecoder_getthumbnail.htm
old-project: wic
ms.assetid: dbfe61d9-50ca-4d44-a8a3-2acae3413985
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetThumbnail, GetThumbnail method [Windows Imaging Component], GetThumbnail method [Windows Imaging Component],IWICBitmapDecoder interface, IWICBitmapDecoder interface [Windows Imaging Component],GetThumbnail method, IWICBitmapDecoder.GetThumbnail, IWICBitmapDecoder::GetThumbnail, _wic_codec_iwicbitmapdecoder_getthumbnail, wic._wic_codec_iwicbitmapdecoder_getthumbnail, wincodec/IWICBitmapDecoder::GetThumbnail
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
 - IWICBitmapDecoder.GetThumbnail
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICBitmapDecoder::GetThumbnail


## -description


Retrieves a bitmap thumbnail of the image, if one exists


## -parameters




### -param ppIThumbnail [out]

Type: <b><a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a>**</b>

Receives a pointer to the <a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a> of the thumbnail.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The returned thumbnail can be of any size, so the caller should scale the thumbnail to the desired size. The only Windows provided image formats that support thumbnails are JPEG, TIFF, and JPEG-XR. If the thumbnail is not available, this will return <a href="https://msdn.microsoft.com/1ded909c-311b-49e3-ba23-b22cd7a77bc6">WINCODEC_ERR_CODECNOTHUMBNAIL</a>.



