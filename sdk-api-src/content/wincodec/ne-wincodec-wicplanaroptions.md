---
UID: NE:wincodec.WICPlanarOptions
title: WICPlanarOptions
author: windows-sdk-content
description: Specifies additional options to an IWICPlanarBitmapSourceTransform implementation.
old-location: wic\wicplanaroptions.htm
old-project: wic
ms.assetid: 8B7F34AA-77A0-428D-800E-31AB43067102
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: WICPlanarOptions, WICPlanarOptions enumeration [Windows Imaging Component], WICPlanarOptionsDefault, WICPlanarOptionsPreserveSubsampling, wic.wicplanaroptions, wincodec/WICPlanarOptions, wincodec/WICPlanarOptionsDefault, wincodec/WICPlanarOptionsPreserveSubsampling
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps | UWP apps]
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
req.typenames: WICPlanarOptions
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincodec.h
api_name:
 - WICPlanarOptions
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

