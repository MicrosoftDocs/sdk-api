---
UID: NS:wincodec.WICBitmapPlaneDescription
title: WICBitmapPlaneDescription (wincodec.h)
description: Specifies the pixel format and size of a component plane.
helpviewer_keywords: ["PWICBitmapPlaneDescription","PWICBitmapPlaneDescription structure pointer [Windows Imaging Component]","WICBitmapPlaneDescription","WICBitmapPlaneDescription structure [Windows Imaging Component]","wic.wicbitmapplanedescription","wincodec/PWICBitmapPlaneDescription","wincodec/WICBitmapPlaneDescription"]
old-location: wic\wicbitmapplanedescription.htm
tech.root: wic
ms.assetid: A5685E9B-F2B9-4A1B-9CEA-044E5FA1CC6D
ms.date: 12/05/2018
ms.keywords: PWICBitmapPlaneDescription, PWICBitmapPlaneDescription structure pointer [Windows Imaging Component], WICBitmapPlaneDescription, WICBitmapPlaneDescription structure [Windows Imaging Component], wic.wicbitmapplanedescription, wincodec/PWICBitmapPlaneDescription, wincodec/WICBitmapPlaneDescription
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WICBitmapPlaneDescription
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICBitmapPlaneDescription
 - wincodec/WICBitmapPlaneDescription
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincodec.h
api_name:
 - WICBitmapPlaneDescription
---

# WICBitmapPlaneDescription structure


## -description

Specifies the pixel format and size of a component plane.

## -struct-fields

### -field Format

Describes the pixel format of the plane.

### -field Width

Component width of the plane.

### -field Height

Component height of the plane.

## -see-also

<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-copypixels">IWICPlanarBitmapSourceTransform::CopyPixels</a>



<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-doessupporttransform">IWICPlanarBitmapSourceTransform::DoesSupportTransform</a>