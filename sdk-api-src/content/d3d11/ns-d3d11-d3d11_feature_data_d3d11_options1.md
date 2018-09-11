---
UID: NS:d3d11.D3D11_FEATURE_DATA_D3D11_OPTIONS1
title: D3D11_FEATURE_DATA_D3D11_OPTIONS1
author: windows-sdk-content
description: Describes Direct3D 11.2 feature options in the current graphics driver.
old-location: direct3d11\d3d11_feature_data_d3d11_options1.htm
tech.root: direct3d11
ms.assetid: 940381BB-E8E6-416D-8F36-CC3591E70702
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: D3D11_FEATURE_DATA_D3D11_OPTIONS1, D3D11_FEATURE_DATA_D3D11_OPTIONS1 structure [Direct3D 11], d3d11/D3D11_FEATURE_DATA_D3D11_OPTIONS1, direct3d11.d3d11_feature_data_d3d11_options1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - D3D11_FEATURE_DATA_D3D11_OPTIONS1
product: Windows
targetos: Windows
req.typenames: D3D11_FEATURE_DATA_D3D11_OPTIONS1
req.redist: 
---

# D3D11_FEATURE_DATA_D3D11_OPTIONS1 structure


## -description


<div class="alert"><b>Note</b>  This structure is supported by the Direct3D 11.2 runtime, which is available on Windows 8.1 and later operating systems.
      </div><div> </div>Describes Direct3D 11.2 feature options in the current graphics driver.


## -struct-fields




### -field TiledResourcesTier

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn280435(v=VS.85).aspx">D3D11_TILED_RESOURCES_TIER</a></b>

Specifies whether the hardware and driver support tiled resources. The runtime sets this member to a <a href="https://msdn.microsoft.com/en-us/library/Dn280435(v=VS.85).aspx">D3D11_TILED_RESOURCES_TIER</a>-typed value that indicates if the hardware and driver support tiled resources and at what tier level.
          


### -field MinMaxFiltering

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">BOOL</a></b>

Specifies whether the hardware and driver support the filtering options (<a href="https://msdn.microsoft.com/en-us/library/Ff476132(v=VS.85).aspx">D3D11_FILTER</a>) of comparing the result to the minimum or maximum value during texture sampling. The runtime sets this member to <b>TRUE</b> if the hardware and driver support these filtering options.
          


### -field ClearViewAlsoSupportsDepthOnlyFormats

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">BOOL</a></b>

Specifies whether the hardware and driver also support the <a href="https://msdn.microsoft.com/en-us/library/Hh404601(v=VS.85).aspx">ID3D11DeviceContext1::ClearView</a> method on depth formats. For info about valid depth formats, see <a href="https://msdn.microsoft.com/en-us/library/Ff476112(v=VS.85).aspx">D3D11_DEPTH_STENCIL_VIEW_DESC</a>.
          


### -field MapOnDefaultBuffers

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">BOOL</a></b>

Specifies support for creating <a href="https://msdn.microsoft.com/en-us/library/Ff476351(v=VS.85).aspx">ID3D11Buffer</a> resources that can be passed to the <a href="https://msdn.microsoft.com/en-us/library/Ff476457(v=VS.85).aspx">ID3D11DeviceContext::Map</a> and <a href="https://msdn.microsoft.com/en-us/library/Ff476485(v=VS.85).aspx">ID3D11DeviceContext::Unmap</a> methods. This means that the <b>CPUAccessFlags</b> member of the <a href="https://msdn.microsoft.com/en-us/library/Ff476092(v=VS.85).aspx">D3D11_BUFFER_DESC</a> structure may be set with the desired <a href="https://msdn.microsoft.com/en-us/library/Ff476106(v=VS.85).aspx">D3D11_CPU_ACCESS_FLAG</a> elements when the <b>Usage</b> member of <b>D3D11_BUFFER_DESC</b> is set to <b>D3D11_USAGE_DEFAULT</b>. The runtime sets this member to <b>TRUE</b> if the hardware is capable of at least <b>D3D_FEATURE_LEVEL_11_0</b> and the graphics device driver supports mappable default buffers.
          


## -remarks



If the Direct3D API is the Direct3D 11.2 runtime and can support 11.2 features, <a href="https://msdn.microsoft.com/en-us/library/Ff476497(v=VS.85).aspx">ID3D11Device::CheckFeatureSupport</a> for <b>D3D11_FEATURE_D3D11_OPTIONS1</b> will return a SUCCESS code when valid parameters are passed. The members of <b>D3D11_FEATURE_DATA_D3D11_OPTIONS1</b> will be set appropriately based on the system's graphics hardware and graphics driver.
      

<h3><a id="Mappable_default_buffers"></a><a id="mappable_default_buffers"></a><a id="MAPPABLE_DEFAULT_BUFFERS"></a>Mappable default buffers</h3>
When creating a default buffer with <a href="https://msdn.microsoft.com/en-us/library/Ff476106(v=VS.85).aspx">D3D11_CPU_ACCESS_FLAG</a>, only the <b>D3D11_BIND_SHADER_RESOURCE</b> and <b>D3D11_BIND_UNORDERED_ACCESS</b> <a href="https://msdn.microsoft.com/en-us/library/Ff476085(v=VS.85).aspx">bind flags</a> may be used.

The <a href="https://msdn.microsoft.com/en-us/library/Ff476203(v=VS.85).aspx">D3D11_RESOURCE_MISC_FLAG</a> cannot be used when creating resources with <b>D3D11_CPU_ACCESS</b> flags.
          

On non-unified memory architecture systems (discrete GPUs), apps should not use mappable default buffers if the compute shader code accesses the same byte in a default buffer more than once - sending the data across the bus multiple times eliminates the performance gained by mapping the default buffer instead of copying it.
          




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476155(v=VS.85).aspx">Core Structures</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476124(v=VS.85).aspx">D3D11_FEATURE</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=316897">DirectX Mappable Default Buffers SDK Sample</a>
 

 

