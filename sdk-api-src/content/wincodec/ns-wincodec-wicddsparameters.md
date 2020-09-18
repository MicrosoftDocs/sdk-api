---
UID: NS:wincodec.WICDdsParameters
title: WICDdsParameters (wincodec.h)
description: Specifies the DDS image dimension, DXGI_FORMAT and alpha mode of contained data.
helpviewer_keywords: ["PWICDdsParameters","PWICDdsParameters structure pointer [Windows Imaging Component]","WICDdsParameters","WICDdsParameters structure [Windows Imaging Component]","wic.wicddsparameters","wincodec/PWICDdsParameters","wincodec/WICDdsParameters"]
old-location: wic\wicddsparameters.htm
tech.root: wic
ms.assetid: 2E5755B4-E8DC-40B2-8DA1-B053A261079B
ms.date: 12/05/2018
ms.keywords: PWICDdsParameters, PWICDdsParameters structure pointer [Windows Imaging Component], WICDdsParameters, WICDdsParameters structure [Windows Imaging Component], wic.wicddsparameters, wincodec/PWICDdsParameters, wincodec/WICDdsParameters
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
req.typenames: WICDdsParameters
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICDdsParameters
 - wincodec/WICDdsParameters
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
 - WICDdsParameters
---

# WICDdsParameters structure


## -description

Specifies the DDS image dimension, <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> and alpha mode of contained data.

## -struct-fields

### -field Width

Type: <b>UINT</b>

The width, in pixels, of the texture at the largest mip size (mip level 0).

### -field Height

Type: <b>UINT</b>

The height, in pixels, of the texture at the largest mip size (mip level 0). When the DDS image contains a 1-dimensional texture, this value is equal to 1.

### -field Depth

Type: <b>UINT</b>

The number of slices in the 3D texture. This is equivalent to the depth, in pixels, of the 3D texture at the largest mip size (mip level 0). When the DDS image contains a 1- or 2-dimensional texture, this value is equal to 1.

### -field MipLevels

Type: <b>UINT</b>

The number of mip levels contained in the DDS image.

### -field ArraySize

Type: <b>UINT</b>

The number of textures in the array in the DDS image.

### -field DxgiFormat

Type: <b><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a></b>

The <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> of the DDS pixel data.

### -field Dimension

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicddsdimension">WICDdsDimension</a></b>

Specifies the dimension type of the data contained in DDS image (1D, 2D, 3D or cube texture).

### -field AlphaMode

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicddsalphamode">WICDdsAlphaMode</a></b>

Specifies the alpha behavior of the DDS image.

## -see-also

<a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>



<a href="/windows/desktop/api/wincodec/ne-wincodec-wicddsalphamode">WICDdsAlphaMode</a>



<a href="/windows/desktop/api/wincodec/ne-wincodec-wicddsdimension">WICDdsDimension</a>