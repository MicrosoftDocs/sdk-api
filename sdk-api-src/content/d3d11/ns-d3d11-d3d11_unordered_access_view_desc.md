---
UID: NS:d3d11.D3D11_UNORDERED_ACCESS_VIEW_DESC
title: D3D11_UNORDERED_ACCESS_VIEW_DESC
author: windows-sdk-content
description: Specifies the subresources from a resource that are accessible using an unordered-access view.
old-location: direct3d11\d3d11_unordered_access_view_desc.htm
old-project: direct3d11
ms.assetid: 884b5498-7f10-4a44-a947-bc7d93fa0cbf
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: 66d569bb-5ee1-ef49-184c-1e392e6a777a, D3D11_UNORDERED_ACCESS_VIEW_DESC, D3D11_UNORDERED_ACCESS_VIEW_DESC structure [Direct3D 11], d3d11/D3D11_UNORDERED_ACCESS_VIEW_DESC, direct3d11.d3d11_unordered_access_view_desc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: D3D11_UNORDERED_ACCESS_VIEW_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_UNORDERED_ACCESS_VIEW_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_UNORDERED_ACCESS_VIEW_DESC structure


## -description


Specifies the subresources from a resource that are accessible using an unordered-access view.


## -struct-fields




### -field Format

Type: <b><a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a></b>

The data format (see <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a>).


### -field ViewDimension

Type: <b><a href="https://msdn.microsoft.com/c9a2bcd1-9cfb-4cac-87eb-4747af745fdd">D3D11_UAV_DIMENSION</a></b>

The resource type (see <a href="https://msdn.microsoft.com/c9a2bcd1-9cfb-4cac-87eb-4747af745fdd">D3D11_UAV_DIMENSION</a>), which specifies how the resource will be accessed.


### -field Buffer

Type: <b><a href="https://msdn.microsoft.com/8dcd2281-1875-474e-8c86-a6920ab2b515">D3D11_BUFFER_UAV</a></b>

Specifies which buffer elements can be accessed (see <a href="https://msdn.microsoft.com/8dcd2281-1875-474e-8c86-a6920ab2b515">D3D11_BUFFER_UAV</a>).


### -field Texture1D

Type: <b><a href="https://msdn.microsoft.com/946047de-2b29-4f58-999d-4d4eaa27bb2c">D3D11_TEX1D_UAV</a></b>

Specifies the subresources in a 1D texture that can be accessed (see <a href="https://msdn.microsoft.com/946047de-2b29-4f58-999d-4d4eaa27bb2c">D3D11_TEX1D_UAV</a>).


### -field Texture1DArray

Type: <b><a href="https://msdn.microsoft.com/8a637d5f-b9cb-486b-8f43-4925cee9ccf7">D3D11_TEX1D_ARRAY_UAV</a></b>

Specifies the subresources in a 1D texture array that can be accessed (see <a href="https://msdn.microsoft.com/8a637d5f-b9cb-486b-8f43-4925cee9ccf7">D3D11_TEX1D_ARRAY_UAV</a>).


### -field Texture2D

Type: <b><a href="https://msdn.microsoft.com/2b090290-5250-4c92-9e1d-5e8a33dc2c4d">D3D11_TEX2D_UAV</a></b>

Specifies the subresources in a 2D texture that can be accessed (see <a href="https://msdn.microsoft.com/2b090290-5250-4c92-9e1d-5e8a33dc2c4d">D3D11_TEX2D_UAV</a>).


### -field Texture2DArray

Type: <b><a href="https://msdn.microsoft.com/94f47a6c-538e-484d-ac7d-b6b6a3080370">D3D11_TEX2D_ARRAY_UAV</a></b>

Specifies the subresources in a 2D texture array that can be accessed (see <a href="https://msdn.microsoft.com/94f47a6c-538e-484d-ac7d-b6b6a3080370">D3D11_TEX2D_ARRAY_UAV</a>).


### -field Texture3D

Type: <b><a href="https://msdn.microsoft.com/5668c7be-73d1-4407-ace6-8970d723fc44">D3D11_TEX3D_UAV</a></b>

Specifies subresources in a 3D texture that can be accessed (see <a href="https://msdn.microsoft.com/5668c7be-73d1-4407-ace6-8970d723fc44">D3D11_TEX3D_UAV</a>).


## -remarks



An unordered-access-view description is passed into <a href="https://msdn.microsoft.com/85b85114-4e3f-407e-879c-ef4c120cb3c1">ID3D11Device::CreateUnorderedAccessView</a> to create a view.




## -see-also




<a href="https://msdn.microsoft.com/a29e01ac-8aa1-4a40-ad4d-3b738e129436">Resource Structures</a>
 

 

