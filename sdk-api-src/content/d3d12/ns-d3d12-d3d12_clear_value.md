---
UID: NS:d3d12.D3D12_CLEAR_VALUE
title: D3D12_CLEAR_VALUE
author: windows-sdk-content
description: Describes a value used to optimize clear operations for a particular resource.
old-location: direct3d12\d3d12_clear_value.htm
tech.root: direct3d12
ms.assetid: 03B67F91-C150-4719-8C43-D04F51DC9C06
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D12_CLEAR_VALUE, D3D12_CLEAR_VALUE structure, d3d12/D3D12_CLEAR_VALUE, direct3d12.d3d12_clear_value
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
 - D3D12.h
api_name:
 - D3D12_CLEAR_VALUE
product: Windows
targetos: Windows
req.typenames: D3D12_CLEAR_VALUE
req.redist: 
---

# D3D12_CLEAR_VALUE structure


## -description


Describes a value used to optimize clear operations for a particular resource.


## -struct-fields




### -field Format

Specifies one member of the <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a> enum.

The format of the commonly cleared color follows the same validation rules as a view/ descriptor creation. In general, the format of the clear color can be any format in the same typeless group that the resource format belongs to.

This <i>Format</i> must match the format of the view used during the clear operation. It indicates whether the <i>Color</i> or the <i>DepthStencil</i> member is valid and how to convert the values for usage with the resource.


### -field Color

Specifies a 4-entry array of float values (each value in the range 0.0 to 1.0), determining the RGBA value. The order of RGBA matches the order used with <a href="https://msdn.microsoft.com/en-us/library/Dn903842(v=VS.85).aspx">ClearRenderTargetView</a>.


### -field DepthStencil

Specifies one member of <a href="https://msdn.microsoft.com/en-us/library/Dn903799(v=VS.85).aspx">D3D12_DEPTH_STENCIL_VALUE</a>. These values match the semantics of <i>Depth</i> and <i>Stencil</i> in <a href="https://msdn.microsoft.com/en-us/library/Dn903840(v=VS.85).aspx">ClearDepthStencilView</a>.


## -remarks



This structure is optionally passed into the following methods:
        

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn899178(v=VS.85).aspx">ID3D12Device::CreateCommittedResource</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn899180(v=VS.85).aspx">ID3D12Device::CreatePlacedResource</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn899181(v=VS.85).aspx">ID3D12Device::CreateReservedResource</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt186564(v=VS.85).aspx">CD3DX12_CLEAR_VALUE</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn770459(v=VS.85).aspx">Core Structures</a>
 

 

