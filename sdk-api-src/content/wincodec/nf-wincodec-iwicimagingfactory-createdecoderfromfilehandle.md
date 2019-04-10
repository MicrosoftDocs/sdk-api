---
UID: NF:wincodec.IWICImagingFactory.CreateDecoderFromFileHandle
title: IWICImagingFactory::CreateDecoderFromFileHandle (wincodec.h)
author: windows-sdk-content
description: Creates a new instance of the IWICBitmapDecoder based on the given file handle.
old-location: wic\_wic_codec_iwicimagingfactory_createdecoderfromfilehandle.htm
tech.root: wic
ms.assetid: 94cf408c-bcea-419a-bf87-fac1e15e0a12
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateDecoderFromFileHandle, CreateDecoderFromFileHandle method [Windows Imaging Component], CreateDecoderFromFileHandle method [Windows Imaging Component],IWICImagingFactory interface, IWICImagingFactory interface [Windows Imaging Component],CreateDecoderFromFileHandle method, IWICImagingFactory.CreateDecoderFromFileHandle, IWICImagingFactory::CreateDecoderFromFileHandle, _wic_codec_iwicimagingfactory_createdecoderfromfilehandle, wic._wic_codec_iwicimagingfactory_createdecoderfromfilehandle, wincodec/IWICImagingFactory::CreateDecoderFromFileHandle
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
 - IWICImagingFactory.CreateDecoderFromFileHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICImagingFactory::CreateDecoderFromFileHandle


## -description


Creates a new instance of the <a href="https://msdn.microsoft.com/91dafd5e-e4fb-4691-a3d0-ca8b6ff0aaf7">IWICBitmapDecoder</a> based on the given file handle.


## -parameters




### -param hFile [in]

Type: <b>ULONG_PTR</b>

The file handle to create the decoder from.


### -param pguidVendor [in]

Type: <b>const GUID*</b>

The GUID for the preferred decoder vendor. Use <b>NULL</b> if no preferred vendor.


### -param metadataOptions [in]

Type: <b><a href="https://msdn.microsoft.com/27b9d6e1-e171-4c7f-8f96-fa5a93923e35">WICDecodeOptions</a></b>

The <a href="https://msdn.microsoft.com/27b9d6e1-e171-4c7f-8f96-fa5a93923e35">WICDecodeOptions</a> to use when creating the decoder.


### -param ppIDecoder [out, retval]

Type: <b><a href="https://msdn.microsoft.com/91dafd5e-e4fb-4691-a3d0-ca8b6ff0aaf7">IWICBitmapDecoder</a>**</b>

A pointer that receives a pointer to a new <a href="https://msdn.microsoft.com/91dafd5e-e4fb-4691-a3d0-ca8b6ff0aaf7">IWICBitmapDecoder</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When a decoder is created using this method, the file handle must remain alive during the lifetime of the decoder.




## -see-also




<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/30d155b1-a46c-46c4-9f8f-fb56dc6bf0a9">IWICImagingFactory</a>
 

 

