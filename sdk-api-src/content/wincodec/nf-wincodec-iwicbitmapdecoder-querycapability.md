---
UID: NF:wincodec.IWICBitmapDecoder.QueryCapability
title: IWICBitmapDecoder::QueryCapability
author: windows-sdk-content
description: Retrieves the capabilities of the decoder based on the specified stream.
old-location: wic\_wic_codec_iwicbitmapdecoder_querycapability.htm
tech.root: wic
ms.assetid: eeff3d5d-ed7f-41f7-b529-aeeeb8503a50
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWICBitmapDecoder interface [Windows Imaging Component],QueryCapability method, IWICBitmapDecoder.QueryCapability, IWICBitmapDecoder::QueryCapability, QueryCapability, QueryCapability method [Windows Imaging Component], QueryCapability method [Windows Imaging Component],IWICBitmapDecoder interface, _wic_codec_iwicbitmapdecoder_querycapability, wic._wic_codec_iwicbitmapdecoder_querycapability, wincodec/IWICBitmapDecoder::QueryCapability
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
 - IWICBitmapDecoder.QueryCapability
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICBitmapDecoder::QueryCapability


## -description


Retrieves the capabilities of the decoder based on the specified stream.


## -parameters




### -param pIStream [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

The stream to retrieve the decoder capabilities from.


### -param pdwCapability [out]

Type: <b>DWORD*</b>

The <a href="https://msdn.microsoft.com/e501b8f7-3c99-461d-be92-dca80f5657c5">WICBitmapDecoderCapabilities</a> of the decoder.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Custom decoder implementations should save the current position of the specified <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>, read whatever information is necessary in order to determine which capabilities it can provide for the supplied stream, and restore the stream position.



