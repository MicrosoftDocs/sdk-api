---
UID: NS:d3d11.D3D11_BUFFEREX_SRV
title: D3D11_BUFFEREX_SRV (d3d11.h)
description: Describes the elements in a raw buffer resource to use in a shader-resource view.
helpviewer_keywords: ["6e2b4acb-42c7-1258-4812-425166fea83e","D3D11_BUFFEREX_SRV","D3D11_BUFFEREX_SRV structure [Direct3D 11]","d3d11/D3D11_BUFFEREX_SRV","direct3d11.d3d11_bufferex_srv"]
old-location: direct3d11\d3d11_bufferex_srv.htm
tech.root: direct3d11
ms.assetid: 55714c3b-ef21-43c1-94a1-60b63f3fedac
ms.date: 12/05/2018
ms.keywords: 6e2b4acb-42c7-1258-4812-425166fea83e, D3D11_BUFFEREX_SRV, D3D11_BUFFEREX_SRV structure [Direct3D 11], d3d11/D3D11_BUFFEREX_SRV, direct3d11.d3d11_bufferex_srv
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
req.typenames: D3D11_BUFFEREX_SRV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_BUFFEREX_SRV
 - d3d11/D3D11_BUFFEREX_SRV
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
 - D3D11_BUFFEREX_SRV
---

# D3D11_BUFFEREX_SRV structure


## -description

Describes the elements in a raw buffer resource to use in a shader-resource view.

## -struct-fields

### -field FirstElement

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The index of the first element to be accessed by the view.

### -field NumElements

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of elements in the resource.

### -field Flags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_bufferex_srv_flag">D3D11_BUFFEREX_SRV_FLAG</a>-typed value that identifies view options for the buffer. Currently, the only option is to identify a raw view of the buffer. For more info about raw viewing of buffers, see <a href="/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro">Raw Views of Buffers</a>.

## -remarks

This structure is used by <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc">D3D11_SHADER_RESOURCE_VIEW_DESC</a> to create a raw view of a buffer.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-structures">Resource Structures</a>