---
UID: NF:wincodec.IWICPlanarFormatConverter.Initialize
title: IWICPlanarFormatConverter::Initialize (wincodec.h)
author: windows-sdk-content
description: Initializes a format converter with a planar source, and specifies the interleaved output pixel format.
old-location: wic\iwicplanarformatconverter_initialize.htm
tech.root: wic
ms.assetid: 0EEF6940-627A-4615-90C0-196AAB36843E
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWICPlanarFormatConverter interface [Windows Imaging Component],Initialize method, IWICPlanarFormatConverter.Initialize, IWICPlanarFormatConverter::Initialize, Initialize, Initialize method [Windows Imaging Component], Initialize method [Windows Imaging Component],IWICPlanarFormatConverter interface, wic.iwicplanarformatconverter_initialize, wincodec/IWICPlanarFormatConverter::Initialize
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - IWICPlanarFormatConverter.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICPlanarFormatConverter::Initialize


## -description


Initializes a format converter with a planar source, and specifies the interleaved output pixel format.


## -parameters




### -param ppPlanes [in]

Type: <b><a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a>**</b>

An array of <a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a> that represents image planes.


### -param cPlanes

Type: <b>UINT</b>

The number of component planes specified by the planes parameter.


### -param dstFormat

Type: <b>REFWICPixelFormatGUID </b>

The destination interleaved pixel format.


### -param dither

Type: <b><a href="https://msdn.microsoft.com/e3fd8f37-8ea9-4cdb-853b-d5119b7afdc9">WICBitmapDitherType</a></b>

The <a href="https://msdn.microsoft.com/e3fd8f37-8ea9-4cdb-853b-d5119b7afdc9">WICBitmapDitherType</a> used for conversion.


### -param pIPalette

Type: <b><a href="https://msdn.microsoft.com/cb0e4f92-4aff-48c7-af62-5f7154539289">IWICPalette</a>*</b>

The palette to use for conversion.


### -param alphaThresholdPercent

Type: <b>double</b>

The alpha threshold to use for conversion.


### -param paletteTranslate

Type: <b><a href="https://msdn.microsoft.com/a8192905-2bae-4760-bf2d-64640c46e168">WICBitmapPaletteType</a></b>

The palette translation type to use for conversion.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0EEF6940-627A-4615-90C0-196AAB36843E">IWICFormatConverter::Initialize</a>



<a href="https://msdn.microsoft.com/07258A07-84AA-4DC2-B2E3-14A43AED5617">IWICPlanarFormatConverter</a>
 

 

