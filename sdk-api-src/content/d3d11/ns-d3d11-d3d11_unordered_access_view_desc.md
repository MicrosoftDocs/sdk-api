---
UID: NS:d3d11.D3D11_UNORDERED_ACCESS_VIEW_DESC
title: D3D11_UNORDERED_ACCESS_VIEW_DESC
author: windows-sdk-content
description: Specifies the subresources from a resource that are accessible using an unordered-access view.
old-location: direct3d11\d3d11_unordered_access_view_desc.htm
tech.root: direct3d11
ms.assetid: 884b5498-7f10-4a44-a947-bc7d93fa0cbf
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 66d569bb-5ee1-ef49-184c-1e392e6a777a, D3D11_UNORDERED_ACCESS_VIEW_DESC, D3D11_UNORDERED_ACCESS_VIEW_DESC structure [Direct3D 11], d3d11/D3D11_UNORDERED_ACCESS_VIEW_DESC, direct3d11.d3d11_unordered_access_view_desc
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: D3D11_UNORDERED_ACCESS_VIEW_DESC
req.redist: 
---

# D3D11_UNORDERED_ACCESS_VIEW_DESC structure


## -description


Specifies the subresources from a resource that are accessible using an unordered-access view.


## -struct-fields




### -field Format

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a></b>

The data format (see <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a>).


### -field ViewDimension

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476257(v=VS.85).aspx">D3D11_UAV_DIMENSION</a></b>

The resource type (see <a href="https://msdn.microsoft.com/en-us/library/Ff476257(v=VS.85).aspx">D3D11_UAV_DIMENSION</a>), which specifies how the resource will be accessed.


### -field Buffer

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476095(v=VS.85).aspx">D3D11_BUFFER_UAV</a></b>

Specifies which buffer elements can be accessed (see <a href="https://msdn.microsoft.com/en-us/library/Ff476095(v=VS.85).aspx">D3D11_BUFFER_UAV</a>).


### -field Texture1D

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476232(v=VS.85).aspx">D3D11_TEX1D_UAV</a></b>

Specifies the subresources in a 1D texture that can be accessed (see <a href="https://msdn.microsoft.com/en-us/library/Ff476232(v=VS.85).aspx">D3D11_TEX1D_UAV</a>).


### -field Texture1DArray

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476228(v=VS.85).aspx">D3D11_TEX1D_ARRAY_UAV</a></b>

Specifies the subresources in a 1D texture array that can be accessed (see <a href="https://msdn.microsoft.com/en-us/library/Ff476228(v=VS.85).aspx">D3D11_TEX1D_ARRAY_UAV</a>).


### -field Texture2D

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476246(v=VS.85).aspx">D3D11_TEX2D_UAV</a></b>

Specifies the subresources in a 2D texture that can be accessed (see <a href="https://msdn.microsoft.com/en-us/library/Ff476246(v=VS.85).aspx">D3D11_TEX2D_UAV</a>).


### -field Texture2DArray

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476242(v=VS.85).aspx">D3D11_TEX2D_ARRAY_UAV</a></b>

Specifies the subresources in a 2D texture array that can be accessed (see <a href="https://msdn.microsoft.com/en-us/library/Ff476242(v=VS.85).aspx">D3D11_TEX2D_ARRAY_UAV</a>).


### -field Texture3D

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476249(v=VS.85).aspx">D3D11_TEX3D_UAV</a></b>

Specifies subresources in a 3D texture that can be accessed (see <a href="https://msdn.microsoft.com/en-us/library/Ff476249(v=VS.85).aspx">D3D11_TEX3D_UAV</a>).


## -remarks



An unordered-access-view description is passed into <a href="https://msdn.microsoft.com/en-us/library/Ff476523(v=VS.85).aspx">ID3D11Device::CreateUnorderedAccessView</a> to create a view.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476173(v=VS.85).aspx">Resource Structures</a>
 

 

