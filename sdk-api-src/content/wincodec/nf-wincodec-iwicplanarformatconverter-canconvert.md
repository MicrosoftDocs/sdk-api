---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

