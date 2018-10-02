---
UID: NF:wincodec.IWICBitmapEncoder.GetContainerFormat
title: IWICBitmapEncoder::GetContainerFormat
author: windows-sdk-content
description: Retrieves the encoder's container format.
old-location: wic\_wic_codec_iwicbitmapencoder_getcontainerformat.htm
tech.root: wic
ms.assetid: 2d197321-0a89-49fd-b243-1d870c178b57
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetContainerFormat, GetContainerFormat method [Windows Imaging Component], GetContainerFormat method [Windows Imaging Component],IWICBitmapEncoder interface, IWICBitmapEncoder interface [Windows Imaging Component],GetContainerFormat method, IWICBitmapEncoder.GetContainerFormat, IWICBitmapEncoder::GetContainerFormat, _wic_codec_iwicbitmapencoder_getcontainerformat, wic._wic_codec_iwicbitmapencoder_getcontainerformat, wincodec/IWICBitmapEncoder::GetContainerFormat
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
 - IWICBitmapEncoder.GetContainerFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICBitmapEncoder::GetContainerFormat


## -description


Retrieves the encoder's container format.


## -parameters




### -param pguidContainerFormat [out]

Type: <b>GUID*</b>

A pointer that receives the encoder's container format GUID.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/fe87c9ae-dedf-4ec2-ac11-0ea5fc6aa3ad">IWICBitmapEncoder</a>



<a href="https://msdn.microsoft.com/2be5cfeb-2dd3-4486-b639-35ee28a7dd7b">WIC GUIDs and CLSIDs</a>
 

 

