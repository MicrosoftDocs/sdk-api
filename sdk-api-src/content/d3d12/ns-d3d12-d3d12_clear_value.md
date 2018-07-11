---
UID: NS:d3d12.D3D12_CLEAR_VALUE
title: D3D12_CLEAR_VALUE
author: windows-sdk-content
description: Describes a value used to optimize clear operations for a particular resource.
old-location: direct3d12\d3d12_clear_value.htm
old-project: direct3d12
ms.assetid: 03B67F91-C150-4719-8C43-D04F51DC9C06
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: D3D12_CLEAR_VALUE, D3D12_CLEAR_VALUE structure, d3d12/D3D12_CLEAR_VALUE, direct3d12.d3d12_clear_value
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D12_CLEAR_VALUE
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
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_CLEAR_VALUE structure


## -description


Describes a value used to optimize clear operations for a particular resource.


## -struct-fields




### -field Format

Specifies one member of the <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a> enum.

The format of the commonly cleared color follows the same validation rules as a view/ descriptor creation. In general, the format of the clear color can be any format in the same typeless group that the resource format belongs to.

This <i>Format</i> must match the format of the view used during the clear operation. It indicates whether the <i>Color</i> or the <i>DepthStencil</i> member is valid and how to convert the values for usage with the resource.


### -field Color

Specifies a 4-entry array of float values (each value in the range 0.0 to 1.0), determining the RGBA value. The order of RGBA matches the order used with <a href="https://msdn.microsoft.com/5AB13E36-A189-41B4-AEF8-B5C5831655DB">ClearRenderTargetView</a>.


### -field DepthStencil

Specifies one member of <a href="https://msdn.microsoft.com/9C37A002-F65A-4943-AA15-C62D7DD25A74">D3D12_DEPTH_STENCIL_VALUE</a>. These values match the semantics of <i>Depth</i> and <i>Stencil</i> in <a href="https://msdn.microsoft.com/EF56EA6C-00DB-4231-B67D-B99811F51246">ClearDepthStencilView</a>.


## -remarks




          This structure is optionally passed into the following methods:
        

<ul>
<li>
<a href="https://msdn.microsoft.com/FF9E8F11-F2C5-4A96-8E25-140870D15DA9">ID3D12Device::CreateCommittedResource</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4581A82D-D2B6-4CAE-A336-07B8CF90A0BA">ID3D12Device::CreatePlacedResource</a>
</li>
<li>
<a href="https://msdn.microsoft.com/37E74129-1B5C-4997-A584-D7E9F92342EA">ID3D12Device::CreateReservedResource</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/C3E2FAF4-79C4-49CA-B7D3-1FED69C8F7A7">CD3DX12_CLEAR_VALUE</a>



<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

