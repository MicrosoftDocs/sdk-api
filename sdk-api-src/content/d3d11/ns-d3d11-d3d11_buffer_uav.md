---
UID: NS:d3d11.D3D11_BUFFER_UAV
title: D3D11_BUFFER_UAV (d3d11.h)
description: Describes the elements in a buffer to use in a unordered-access view. (D3D11_BUFFER_UAV)
helpviewer_keywords: ["D3D11_BUFFER_UAV","D3D11_BUFFER_UAV structure [Direct3D 11]","c8071050-410d-09ba-35f3-6d7c40e44eb6","d3d11/D3D11_BUFFER_UAV","direct3d11.d3d11_buffer_uav"]
old-location: direct3d11\d3d11_buffer_uav.htm
tech.root: direct3d11
ms.assetid: 8dcd2281-1875-474e-8c86-a6920ab2b515
ms.date: 12/05/2018
ms.keywords: D3D11_BUFFER_UAV, D3D11_BUFFER_UAV structure [Direct3D 11], c8071050-410d-09ba-35f3-6d7c40e44eb6, d3d11/D3D11_BUFFER_UAV, direct3d11.d3d11_buffer_uav
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
req.typenames: D3D11_BUFFER_UAV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_BUFFER_UAV
 - d3d11/D3D11_BUFFER_UAV
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
 - D3D11_BUFFER_UAV
---

# D3D11_BUFFER_UAV structure


## -description

Describes the elements in a buffer to use in a unordered-access view.

## -struct-fields

### -field FirstElement

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The zero-based index of the first element to be accessed.

### -field NumElements

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of elements in the resource. For structured buffers, this is the number of structures in the buffer.

### -field Flags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

View options for the resource (see <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag">D3D11_BUFFER_UAV_FLAG</a>).

## -remarks

This structure is used by a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_unordered_access_view_desc">D3D11_UNORDERED_ACCESS_VIEW_DESC</a>.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-structures">Resource Structures</a>
