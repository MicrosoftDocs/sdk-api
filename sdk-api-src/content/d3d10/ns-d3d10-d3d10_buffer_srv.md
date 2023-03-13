---
UID: NS:d3d10.D3D10_BUFFER_SRV
title: D3D10_BUFFER_SRV (d3d10.h)
description: Specifies the elements in a buffer resource to use in a shader-resource view. (D3D10_BUFFER_SRV)
helpviewer_keywords: ["2f5305b7-1dcd-3d82-23b3-875654ce7066","D3D10_BUFFER_SRV","D3D10_BUFFER_SRV structure [Direct3D 10]","d3d10/D3D10_BUFFER_SRV","direct3d10.d3d10_buffer_srv"]
old-location: direct3d10\d3d10_buffer_srv.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_buffer_srv.htm
ms.date: 12/05/2018
ms.keywords: 2f5305b7-1dcd-3d82-23b3-875654ce7066, D3D10_BUFFER_SRV, D3D10_BUFFER_SRV structure [Direct3D 10], d3d10/D3D10_BUFFER_SRV, direct3d10.d3d10_buffer_srv
req.header: d3d10.h
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
req.typenames: D3D10_BUFFER_SRV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_BUFFER_SRV
 - d3d10/D3D10_BUFFER_SRV
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_BUFFER_SRV
---

# D3D10_BUFFER_SRV structure


## -description

Specifies the elements in a <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">buffer</a> resource to use in a shader-resource view.

## -struct-fields

### -field FirstElement

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of bytes between the beginning of the buffer and the first element to access.

### -field ElementOffset

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The offset of the first element in the view to access, relative to element 0.

### -field NumElements

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The total number of elements in the view.

### -field ElementWidth

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The width of each element (in bytes). This can be determined from the format stored in the shader-resource-view description.

## -remarks

The <b>D3D10_BUFFER_SRV</b> structure is a member of the  <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_shader_resource_view_desc">D3D10_SHADER_RESOURCE_VIEW_DESC</a> structure, which represents a shader-resource view description. You can create a shader-resource view by calling the <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createshaderresourceview">ID3D10Device::CreateShaderResourceView</a> method.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures">Resource Structures</a>
