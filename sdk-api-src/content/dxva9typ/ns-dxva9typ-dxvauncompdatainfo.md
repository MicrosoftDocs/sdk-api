---
UID: NS:dxva9typ._DXVAUncompDataInfo
title: DXVAUncompDataInfo (dxva9typ.h)
description: Specifies the dimensions and pixel format of the uncompressed surfaces for DirectX Video Acceleration (DXVA) video decoding.
helpviewer_keywords: ["DXVAUncompDataInfo","DXVAUncompDataInfo structure [Media Foundation]","_DXVAUncompDataInfo","dxva9typ/DXVAUncompDataInfo","mf.dxvauncompdatainfo"]
old-location: mf\dxvauncompdatainfo.htm
tech.root: mf
ms.assetid: bd19d9a8-7d69-4aea-9638-84c3f1a1e810
ms.date: 12/05/2018
ms.keywords: DXVAUncompDataInfo, DXVAUncompDataInfo structure [Media Foundation], _DXVAUncompDataInfo, dxva9typ/DXVAUncompDataInfo, mf.dxvauncompdatainfo
req.header: dxva9typ.h
req.include-header: Dxva.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: DXVAUncompDataInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVAUncompDataInfo
 - dxva9typ/_DXVAUncompDataInfo
 - DXVAUncompDataInfo
 - dxva9typ/DXVAUncompDataInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxva9typ.h
api_name:
 - DXVAUncompDataInfo
---

# DXVAUncompDataInfo structure


## -description

Specifies the dimensions and pixel format of the uncompressed surfaces for DirectX Video Acceleration (DXVA) video decoding.

## -struct-fields

### -field UncompWidth

The width of the uncompressed data, in pixels.

### -field UncompHeight

The height of the uncompressed data, in pixels.

### -field UncompFormat

The pixel format of the uncompressed data, specified as a <b>D3DFORMAT</b> value.

## -see-also

<a href="/windows/desktop/medfound/direct3d-video-structures">Direct3D Video Structures</a>



<a href="/windows/desktop/medfound/idirect3dvideodevice9">IDirect3DVideoDevice9</a>