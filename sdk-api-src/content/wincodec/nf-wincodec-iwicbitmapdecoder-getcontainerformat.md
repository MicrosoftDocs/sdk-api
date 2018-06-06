---
UID: NF:wincodec.IWICBitmapDecoder.GetContainerFormat
title: IWICBitmapDecoder::GetContainerFormat
author: windows-sdk-content
description: Retrieves the image's container format.
old-location: wic\_wic_codec_iwicbitmapdecoder_getcontainerformat.htm
old-project: wic
ms.assetid: ba7b64cf-28de-40d9-80f1-f4b5b1909b77
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetContainerFormat, GetContainerFormat method [Windows Imaging Component], GetContainerFormat method [Windows Imaging Component],IWICBitmapDecoder interface, IWICBitmapDecoder interface [Windows Imaging Component],GetContainerFormat method, IWICBitmapDecoder.GetContainerFormat, IWICBitmapDecoder::GetContainerFormat, _wic_codec_iwicbitmapdecoder_getcontainerformat, wic._wic_codec_iwicbitmapdecoder_getcontainerformat, wincodec/IWICBitmapDecoder::GetContainerFormat
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
 - IWICBitmapDecoder.GetContainerFormat
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICBitmapDecoder::GetContainerFormat


## -description


Retrieves the image's container format.


## -parameters




### -param pguidContainerFormat [out]

Type: <b>GUID*</b>

A pointer that receives the image's container format GUID.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/91dafd5e-e4fb-4691-a3d0-ca8b6ff0aaf7">IWICBitmapDecoder</a>



<a href="https://msdn.microsoft.com/2be5cfeb-2dd3-4486-b639-35ee28a7dd7b">WIC GUIDs and CLSIDs</a>
 

 

