---
UID: NE:d3d11.D3D11_MAP_FLAG
title: D3D11_MAP_FLAG (d3d11.h)
description: Specifies how the CPU should respond when an application calls the ID3D11DeviceContext::Map method on a resource that is being used by the GPU.
helpviewer_keywords: ["629d7d2f-642f-963f-2dce-b5f72d629978","D3D11_MAP_FLAG","D3D11_MAP_FLAG enumeration [Direct3D 11]","D3D11_MAP_FLAG_DO_NOT_WAIT","d3d11/D3D11_MAP_FLAG","d3d11/D3D11_MAP_FLAG_DO_NOT_WAIT","direct3d11.d3d11_map_flag"]
old-location: direct3d11\d3d11_map_flag.htm
tech.root: direct3d11
ms.assetid: 986400c4-2a81-4d43-9564-d26eeaf7bd28
ms.date: 12/05/2018
ms.keywords: 629d7d2f-642f-963f-2dce-b5f72d629978, D3D11_MAP_FLAG, D3D11_MAP_FLAG enumeration [Direct3D 11], D3D11_MAP_FLAG_DO_NOT_WAIT, d3d11/D3D11_MAP_FLAG, d3d11/D3D11_MAP_FLAG_DO_NOT_WAIT, direct3d11.d3d11_map_flag
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D3D11_MAP_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_MAP_FLAG
 - d3d11/D3D11_MAP_FLAG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_MAP_FLAG
---

# D3D11_MAP_FLAG enumeration


## -description

Specifies how the CPU should respond when an application calls the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-map">ID3D11DeviceContext::Map</a> method on a resource that is being used by the GPU.

## -enum-fields

### -field D3D11_MAP_FLAG_DO_NOT_WAIT:0x100000L

Specifies that <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-map">ID3D11DeviceContext::Map</a> should return DXGI_ERROR_WAS_STILL_DRAWING when the GPU blocks the CPU from accessing a resource. For more information about this error code, see <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.

## -remarks

This enumeration is used by <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-map">ID3D11DeviceContext::Map</a>.

D3D11_MAP_FLAG_DO_NOT_WAIT cannot be used with <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_map">D3D11_MAP_WRITE_DISCARD</a> or <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_map">D3D11_MAP_WRITE_NOOVERWRITE</a>.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-enums">Resource Enumerations</a>
