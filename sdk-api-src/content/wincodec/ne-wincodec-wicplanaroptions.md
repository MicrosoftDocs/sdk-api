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

# WICPlanarOptions enumeration


## -description


Specifies additional options to an <a href="https://msdn.microsoft.com/AA47F10A-C90A-4DAF-973F-2669D7364CB9">IWICPlanarBitmapSourceTransform</a> implementation.  


## -enum-fields




### -field WICPlanarOptionsDefault

No options specified.  



WIC JPEG Decoder:  The default behavior for iDCT scaling is to preserve quality when downscaling by downscaling only the Y plane in some cases, and the image may change to 4:4:4 chroma subsampling.



### -field WICPlanarOptionsPreserveSubsampling

Asks the source to preserve the size ratio between planes when scaling.

WIC JPEG Decoder:  Specifying this option causes the JPEG decoder to scale luma and chroma planes by the same amount, so a 4:2:0 chroma subsampled image outputs 4:2:0 data when downscaling by 2x, 4x, or 8x.  



### -field WICPLANAROPTIONS_FORCE_DWORD




## -see-also




<a href="https://msdn.microsoft.com/0D6FB12B-B5C5-4A36-93FC-AF96BF03ED01">IWICPlanarBitmapSourceTransform::CopyPixels</a>



<a href="https://msdn.microsoft.com/CB601454-591B-4292-A8BF-EA9D1F060AB3">IWICPlanarBitmapSourceTransform::DoesSupportTransform</a>
 

 

