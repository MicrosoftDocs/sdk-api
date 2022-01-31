---
UID: NE:wincodec.WICDdsDimension
title: WICDdsDimension (wincodec.h)
description: Specifies the dimension type of the data contained in DDS image.
helpviewer_keywords: ["WICDdsDimension","WICDdsDimension enumeration [Windows Imaging Component]","WICDdsTexture1D","WICDdsTexture2D","WICDdsTexture3D","WICDdsTextureCube","wic.wicddsdimension","wincodec/WICDdsDimension","wincodec/WICDdsTexture1D","wincodec/WICDdsTexture2D","wincodec/WICDdsTexture3D","wincodec/WICDdsTextureCube"]
old-location: wic\wicddsdimension.htm
tech.root: wic
ms.assetid: 76CEBFD7-EE7D-48C4-9F88-9AD82C9FED55
ms.date: 12/05/2018
ms.keywords: WICDdsDimension, WICDdsDimension enumeration [Windows Imaging Component], WICDdsTexture1D, WICDdsTexture2D, WICDdsTexture3D, WICDdsTextureCube, wic.wicddsdimension, wincodec/WICDdsDimension, wincodec/WICDdsTexture1D, wincodec/WICDdsTexture2D, wincodec/WICDdsTexture3D, wincodec/WICDdsTextureCube
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
req.typenames: WICDdsDimension
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICDdsDimension
 - wincodec/WICDdsDimension
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
 - WICDdsDimension
---

# WICDdsDimension enumeration


## -description

Specifies the dimension type of the data contained in DDS image.

## -enum-fields

### -field WICDdsTexture1D:0

DDS image contains a 1-dimensional texture .

### -field WICDdsTexture2D:0x1

DDS image contains a 2-dimensional texture .

### -field WICDdsTexture3D:0x2

DDS image contains a 3-dimensional texture .

### -field WICDdsTextureCube:0x3

The DDS image contains a cube texture represented as an array of 6 faces.

### -field WICDDSTEXTURE_FORCE_DWORD:0x7fffffff

## -remarks

Both <b>WICDdsTexture2d</b> and <b>WICDdsTextureCube</b> correspond to <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_dimension">D3D11_RESOURCE_DIMENSION_TEXTURE2D</a>. When using <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createtexture2d">ID3D11Device::CreateTexture2D</a>, they are distinguished by the flag <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag">D3D11_RESOURCE_MISC_TEXTURECUBE</a> in the structure <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_texture2d_desc">D3D11_TEXTURE2D_DESC</a>.

## -see-also

<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicddsdecoder-getparameters">IWICDdsDecoder::GetParameters</a>



<a href="/windows/desktop/api/wincodec/ns-wincodec-wicddsparameters">WICDdsParameters</a>
