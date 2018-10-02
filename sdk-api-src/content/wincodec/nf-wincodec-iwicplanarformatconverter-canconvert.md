---
UID: NF:wincodec.IWICPlanarFormatConverter.CanConvert
title: IWICPlanarFormatConverter::CanConvert
author: windows-sdk-content
description: Query if the format converter can convert from one format to another.
old-location: wic\iwicplanarformatconverter_canconvert.htm
tech.root: wic
ms.assetid: 24E68425-3758-4E8E-B3F4-46EE8488E3E1
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: CanConvert, CanConvert method [Windows Imaging Component], CanConvert method [Windows Imaging Component],IWICPlanarFormatConverter interface, IWICPlanarFormatConverter interface [Windows Imaging Component],CanConvert method, IWICPlanarFormatConverter.CanConvert, IWICPlanarFormatConverter::CanConvert, wic.iwicplanarformatconverter_canconvert, wincodec/IWICPlanarFormatConverter::CanConvert
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWICPlanarFormatConverter.CanConvert
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICPlanarFormatConverter::CanConvert


## -description


Query if the format converter can convert from one format to another.


## -parameters




### -param pSrcPixelFormats [in]

An array of WIC pixel formats that represents source image planes.


### -param cSrcPlanes

The number of source pixel formats specified by the <i>pSrcFormats</i> parameter.


### -param dstPixelFormat [in]

The destination interleaved pixel format.


### -param pfCanConvert [out]

True if the conversion is supported.


## -returns



If the conversion is not supported, this method returns S_OK, but *<i>pfCanConvert</i> is set to FALSE.



If this method fails, the out parameter <i>pfCanConvert</i> is invalid.




## -remarks



To specify an interleaved input pixel format, provide a length 1 array to <i>pSrcPixelFormats</i>.




## -see-also




<a href="https://msdn.microsoft.com/07258A07-84AA-4DC2-B2E3-14A43AED5617">IWICPlanarFormatConverter</a>
 

 

