---
UID: NE:d3d12.D3D12_RESOLVE_MODE
title: D3D12_RESOLVE_MODE (d3d12.h)
author: windows-sdk-content
description: Specifies a resolve operation.
old-location: direct3d12\d3d12_resolve_mode.htm
tech.root: direct3d12
ms.assetid: 1E14F62A-E6B9-4C88-AC28-2322C4662E1F
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D12_RESOLVE_MODE, D3D12_RESOLVE_MODE enumeration, D3D12_RESOLVE_MODE_AVERAGE, D3D12_RESOLVE_MODE_DECOMPRESS, D3D12_RESOLVE_MODE_MAX, D3D12_RESOLVE_MODE_MIN, d3d12/D3D12_RESOLVE_MODE, d3d12/D3D12_RESOLVE_MODE_AVERAGE, d3d12/D3D12_RESOLVE_MODE_DECOMPRESS, d3d12/D3D12_RESOLVE_MODE_MAX, d3d12/D3D12_RESOLVE_MODE_MIN, direct3d12.d3d12_resolve_mode
ms.topic: enum
req.header: d3d12.h
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
 - d3d12.h
api_name:
 - D3D12_RESOLVE_MODE
product: Windows
targetos: Windows
req.typenames: D3D12_RESOLVE_MODE
req.redist: 
---

# D3D12_RESOLVE_MODE enumeration


## -description


Specifies a resolve operation.


## -enum-fields




### -field D3D12_RESOLVE_MODE_DECOMPRESS

Resolves compressed source samples to their uncompressed values. When using this operation, the source and destination resources must have the same sample count, unlike the min, max, and average operations that require the destination to have a sample count of 1.


### -field D3D12_RESOLVE_MODE_MIN

Resolves the source samples to their minimum value. It can be used with any render target or depth stencil format.


### -field D3D12_RESOLVE_MODE_MAX

Resolves the source samples to their maximum value. It can be used with any render target or depth stencil format.


### -field D3D12_RESOLVE_MODE_AVERAGE

Resolves the source samples to their average value. It can be used with any non-integer render target format, including the depth plane. It can't be used with integer render target formats, including the stencil plane.


## -remarks



This enum is used by the <a href="https://msdn.microsoft.com/8CF3809C-0EC7-4FBB-AEEF-E74FCD9B836D">ID3D12GraphicsCommandList1::ResolveSubresourceRegion</a> function.




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

