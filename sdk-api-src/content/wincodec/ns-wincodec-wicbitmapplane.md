---
UID: NS:wincodec.WICBitmapPlane
title: WICBitmapPlane (wincodec.h)
description: Specifies the pixel format, buffer, stride and size of a component plane for a planar pixel format.
helpviewer_keywords: ["PWICBitmapPlane","PWICBitmapPlane structure pointer [Windows Imaging Component]","WICBitmapPlane","WICBitmapPlane structure [Windows Imaging Component]","wic.wicbitmapplane","wincodec/PWICBitmapPlane","wincodec/WICBitmapPlane"]
old-location: wic\wicbitmapplane.htm
tech.root: wic
ms.assetid: 4E988284-DE71-48B2-BF77-D616FAA2A3B1
ms.date: 12/05/2018
ms.keywords: PWICBitmapPlane, PWICBitmapPlane structure pointer [Windows Imaging Component], WICBitmapPlane, WICBitmapPlane structure [Windows Imaging Component], wic.wicbitmapplane, wincodec/PWICBitmapPlane, wincodec/WICBitmapPlane
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
req.typenames: WICBitmapPlane
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICBitmapPlane
 - wincodec/WICBitmapPlane
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
 - WICBitmapPlane
---

# WICBitmapPlane structure


## -description

Specifies the pixel format, buffer, stride and size of a component plane for a planar pixel format.

## -struct-fields

### -field Format

Type: <b>WICPixelFormatGUID</b>

Describes the pixel format of the plane.

### -field pbBuffer

Type: <b>BYTE*</b>

Pointer to the buffer that holds the plane’s pixel components.

### -field cbStride

Type: <b>UINT</b>

The stride of the buffer pointed to by <i>pbData</i>.  Stride indicates the total number of bytes to go from the beginning of one scanline to the beginning of the next scanline.

### -field cbBufferSize

Type: <b>UINT</b>

The total size of the buffer pointed to by <i>pbBuffer</i>.

## -see-also

<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-copypixels">IWICPlanarBitmapSourceTransform::CopyPixels</a>



<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-doessupporttransform">IWICPlanarBitmapSourceTransform::DoesSupportTransform</a>