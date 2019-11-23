---
UID: NF:wincodec.IWICBitmapEncoder.GetContainerFormat
title: IWICBitmapEncoder::GetContainerFormat (wincodec.h)

description: Retrieves the encoder's container format.
old-location: wic\_wic_codec_iwicbitmapencoder_getcontainerformat.htm
tech.root: wic
ms.assetid: 2d197321-0a89-49fd-b243-1d870c178b57

ms.date: 12/05/2018
ms.keywords: GetContainerFormat, GetContainerFormat method [Windows Imaging Component], GetContainerFormat method [Windows Imaging Component],IWICBitmapEncoder interface, IWICBitmapEncoder interface [Windows Imaging Component],GetContainerFormat method, IWICBitmapEncoder.GetContainerFormat, IWICBitmapEncoder::GetContainerFormat, _wic_codec_iwicbitmapencoder_getcontainerformat, wic._wic_codec_iwicbitmapencoder_getcontainerformat, wincodec/IWICBitmapEncoder::GetContainerFormat
ms.topic: method
f1_keywords: 
 - "wincodec/IWICBitmapEncoder.GetContainerFormat"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder">IWICBitmapEncoder</a>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-guids-clsids">WIC GUIDs and CLSIDs</a>
 

 

