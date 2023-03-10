---
UID: NS:d3d11.D3D11_TEX2D_ARRAY_VPOV
title: D3D11_TEX2D_ARRAY_VPOV (d3d11.h)
description: Identifies a texture resource for a video processor output view. (D3D11_TEX2D_ARRAY_VPOV)
helpviewer_keywords: ["D3D11_TEX2D_ARRAY_VPOV","D3D11_TEX2D_ARRAY_VPOV structure [Media Foundation]","d3d11/D3D11_TEX2D_ARRAY_VPOV","mf.d3d11_tex2d_array_vpov"]
old-location: mf\d3d11_tex2d_array_vpov.htm
tech.root: mf
ms.assetid: DF059392-3E4B-45D2-A3CD-A0C61C8D628F
ms.date: 12/05/2018
ms.keywords: D3D11_TEX2D_ARRAY_VPOV, D3D11_TEX2D_ARRAY_VPOV structure [Media Foundation], d3d11/D3D11_TEX2D_ARRAY_VPOV, mf.d3d11_tex2d_array_vpov
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D3D11_TEX2D_ARRAY_VPOV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_TEX2D_ARRAY_VPOV
 - d3d11/D3D11_TEX2D_ARRAY_VPOV
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_TEX2D_ARRAY_VPOV
---

# D3D11_TEX2D_ARRAY_VPOV structure


## -description

Identifies a texture resource for a video  processor output view.

## -struct-fields

### -field MipSlice

The zero-based index into the array of subtextures.

### -field FirstArraySlice

The index of the first texture to use.

### -field ArraySize

The number of textures in the array.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-structures">Direct3D 11 Video Structures</a>



<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessoroutputview">ID3D11VideoDevice::CreateVideoProcessorOutputView</a>
