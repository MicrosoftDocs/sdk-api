---
UID: NF:wincodec.IWICImagingFactory.CreateBitmapFromMemory
title: IWICImagingFactory::CreateBitmapFromMemory (wincodec.h)
author: windows-sdk-content
description: Creates an IWICBitmap from a memory block.
old-location: wic\_wic_codec_iwicimagingfactory_createbitmapfrommemory.htm
tech.root: wic
ms.assetid: d0fa8f55-2752-4494-8aac-6c47e0ba6e26
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateBitmapFromMemory, CreateBitmapFromMemory method [Windows Imaging Component], CreateBitmapFromMemory method [Windows Imaging Component],IWICImagingFactory interface, IWICImagingFactory interface [Windows Imaging Component],CreateBitmapFromMemory method, IWICImagingFactory.CreateBitmapFromMemory, IWICImagingFactory::CreateBitmapFromMemory, _wic_codec_iwicimagingfactory_createbitmapfrommemory, wic._wic_codec_iwicimagingfactory_createbitmapfrommemory, wincodec/IWICImagingFactory::CreateBitmapFromMemory
ms.topic: method
f1_keywords: ["wincodec/IWICImagingFactory.CreateBitmapFromMemory"]
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
 - IWICImagingFactory.CreateBitmapFromMemory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICImagingFactory::CreateBitmapFromMemory


## -description


Creates an <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmap">IWICBitmap</a> from a memory block.


## -parameters




### -param uiWidth [in]

Type: <b>UINT</b>

The width of the new bitmap.


### -param uiHeight [in]

Type: <b>UINT</b>

The height of the new bitmap.


### -param pixelFormat [in]

Type: <b>REFWICPixelFormatGUID</b>

The pixel format of the new bitmap.  For valid pixel formats, see <a href="https://docs.microsoft.com/windows/desktop/wic/-wic-codec-native-pixel-formats">Native Pixel Formats</a>.


### -param cbStride [in]

Type: <b>UINT</b>

The number of bytes between successive scanlines in <i>pbBuffer</i>.


### -param cbBufferSize [in]

Type: <b>UINT</b>

The size of <i>pbBuffer</i>.


### -param pbBuffer [in]

Type: <b>BYTE*</b>

The buffer used to create the bitmap.


### -param ppIBitmap [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmap">IWICBitmap</a>**</b>

A pointer that receives a pointer to the new bitmap.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The size of the <a href="https://docs.microsoft.com/windows/desktop/wic/-wic-imp-iwicbitmapdecoder">IWICBitmap</a> to be created must be smaller than or equal to the size of the image in <i>pbBuffer</i>.

The <a href="https://docs.microsoft.com/">stride</a> of the destination bitmap will equal the <i>stride</i> of the source data, regardless of the width and height specified.

The <i>pixelFormat</i> parameter defines the pixel format for both the input data and the output bitmap.



