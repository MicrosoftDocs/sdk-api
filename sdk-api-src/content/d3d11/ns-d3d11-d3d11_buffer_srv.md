---
UID: NS:d3d11.D3D11_BUFFER_SRV
title: D3D11_BUFFER_SRV (d3d11.h)
description: Specifies the elements in a buffer resource to use in a shader-resource view. (D3D11_BUFFER_SRV)
helpviewer_keywords: ["D3D11_BUFFER_SRV","D3D11_BUFFER_SRV structure [Direct3D 11]","d3d11/D3D11_BUFFER_SRV","direct3d11.d3d11_buffer_srv","f51a8ea2-ef96-9fea-a1b6-75c15fd9f42e"]
old-location: direct3d11\d3d11_buffer_srv.htm
tech.root: direct3d11
ms.assetid: 2ada8526-bef3-4998-8775-6e062f972a1c
ms.date: 12/05/2018
ms.keywords: D3D11_BUFFER_SRV, D3D11_BUFFER_SRV structure [Direct3D 11], d3d11/D3D11_BUFFER_SRV, direct3d11.d3d11_buffer_srv, f51a8ea2-ef96-9fea-a1b6-75c15fd9f42e
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
req.typenames: D3D11_BUFFER_SRV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_BUFFER_SRV
 - d3d11/D3D11_BUFFER_SRV
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
 - D3D11_BUFFER_SRV
---

# D3D11_BUFFER_SRV structure


## -description

Specifies the elements in a buffer resource to use in a shader-resource view.

## -struct-fields

### -field FirstElement

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index of the first element to access.

### -field ElementOffset

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The offset of the first element in the view to access, relative to element 0.

### -field NumElements

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The total number of elements in the view.

### -field ElementWidth

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The width of each element (in bytes).
              This can be determined from the format stored in the shader-resource-view description.

## -remarks

The <b>D3D11_BUFFER_SRV</b> structure is a member of the  <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc">D3D11_SHADER_RESOURCE_VIEW_DESC</a> structure, which represents a shader-resource view description. You can create a shader-resource view by calling the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createshaderresourceview">ID3D11Device::CreateShaderResourceView</a> method.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-structures">Resource Structures</a>
