---
UID: NS:dxva9typ._DXVACompBufferInfo
title: DXVACompBufferInfo (dxva9typ.h)
description: Specifies the requirements for compressed surfaces for DirectX Video Acceleration (DXVA).
helpviewer_keywords: ["DXVACompBufferInfo","DXVACompBufferInfo structure [Media Foundation]","_DXVACompBufferInfo","dxva9typ/DXVACompBufferInfo","mf.dxvacompbufferinfo"]
old-location: mf\dxvacompbufferinfo.htm
tech.root: mf
ms.assetid: dabef388-d883-48a6-9abc-218dc163ef63
ms.date: 12/05/2018
ms.keywords: DXVACompBufferInfo, DXVACompBufferInfo structure [Media Foundation], _DXVACompBufferInfo, dxva9typ/DXVACompBufferInfo, mf.dxvacompbufferinfo
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
req.typenames: DXVACompBufferInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVACompBufferInfo
 - dxva9typ/_DXVACompBufferInfo
 - DXVACompBufferInfo
 - dxva9typ/DXVACompBufferInfo
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
 - DXVACompBufferInfo
---

# DXVACompBufferInfo structure


## -description

Specifies the requirements for compressed surfaces for DirectX Video Acceleration (DXVA).

To get this information, call <a href="/windows/desktop/medfound/idirect3dvideodevice9-getdxvacompressedbufferinfo">IDirect3DVideoDevice9::GetDXVACompressedBufferInfo</a>. Each <b>DXVACompBufferInfo</b> structure gives the requirements for a specific  DXVA surface type. The surface type is defined implicitly by the index of the array that is passed into the <i>pBufferInfo</i>  parameter.

## -struct-fields

### -field NumCompBuffers

The number of surfaces of this type to create.

### -field WidthToCreate

The width of the surface, in pixels.

### -field HeightToCreate

The height of the surface, in pixels.

### -field BytesToAllocate

The size of the surface, in bytes.

### -field Usage

A bitwise <b>OR</b> of one or more <b>D3DUSAGE</b> constants.

### -field Pool

The memory pool in which to create the surface, specified as a <b>D3DPOOL</b> value.

### -field Format

The pixel format, specified as a <b>D3DFORMAT</b> value.

## -remarks

To create the compressed surfaces, call <a href="/windows/desktop/medfound/idirect3dvideodevice9-createsurface">IDirect3DVideoDevice9::CreateSurface</a>.

## -see-also

<a href="/windows/desktop/medfound/direct3d-video-structures">Direct3D Video Structures</a>



<a href="/windows/desktop/medfound/idirect3dvideodevice9-getdxvacompressedbufferinfo">IDirect3DVideoDevice9::GetDXVACompressedBufferInfo</a>