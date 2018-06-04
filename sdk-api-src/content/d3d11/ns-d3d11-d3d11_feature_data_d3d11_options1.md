---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# D3D11_FEATURE_DATA_D3D11_OPTIONS1 structure


## -description


<div class="alert"><b>Note</b>  
        This structure is supported by the Direct3D 11.2 runtime, which is available on Windows 8.1 and later operating systems.
      </div><div> </div>Describes Direct3D 11.2 feature options in the current graphics driver.


## -struct-fields




### -field TiledResourcesTier

Type: <b><a href="https://msdn.microsoft.com/F2E58CDC-4E65-4166-976A-E58B6DC7B1E8">D3D11_TILED_RESOURCES_TIER</a></b>


            Specifies whether the hardware and driver support tiled resources. The runtime sets this member to a <a href="https://msdn.microsoft.com/F2E58CDC-4E65-4166-976A-E58B6DC7B1E8">D3D11_TILED_RESOURCES_TIER</a>-typed value that indicates if the hardware and driver support tiled resources and at what tier level.
          


### -field MinMaxFiltering

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>


            Specifies whether the hardware and driver support the filtering options (<a href="https://msdn.microsoft.com/873b7910-4686-4f0c-a674-2aa3585a9b36">D3D11_FILTER</a>) of comparing the result to the minimum or maximum value during texture sampling. The runtime sets this member to <b>TRUE</b> if the hardware and driver support these filtering options.
          


### -field ClearViewAlsoSupportsDepthOnlyFormats

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>


            Specifies whether the hardware and driver also support the <a href="https://msdn.microsoft.com/7CC8DEB6-075C-40EB-822D-8A627E285FA2">ID3D11DeviceContext1::ClearView</a> method on depth formats. For info about valid depth formats, see <a href="https://msdn.microsoft.com/f073a798-edd5-4e6a-a8a7-1592721ce35d">D3D11_DEPTH_STENCIL_VIEW_DESC</a>.
          


### -field MapOnDefaultBuffers

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>


            Specifies support for creating <a href="https://msdn.microsoft.com/7224de57-75cb-4d68-9d70-f5dd2f92b1fd">ID3D11Buffer</a> resources that can be passed to the <a href="https://msdn.microsoft.com/c9d57873-1faa-42fa-855c-26f565e3b27c">ID3D11DeviceContext::Map</a> and <a href="https://msdn.microsoft.com/67797b77-c0a5-47b4-ba54-4282b6aa5b13">ID3D11DeviceContext::Unmap</a> methods. This means that the <b>CPUAccessFlags</b> member of the <a href="https://msdn.microsoft.com/a5e470bb-011b-4a2a-96d6-cbf76fe12638">D3D11_BUFFER_DESC</a> structure may be set with the desired <a href="https://msdn.microsoft.com/0a19c2a7-2570-40e2-8328-cbf5d7263605">D3D11_CPU_ACCESS_FLAG</a> elements when the <b>Usage</b> member of <b>D3D11_BUFFER_DESC</b> is set to <b>D3D11_USAGE_DEFAULT</b>. The runtime sets this member to <b>TRUE</b> if the hardware is capable of at least <b>D3D_FEATURE_LEVEL_11_0</b> and the graphics device driver supports mappable default buffers.
          


## -remarks




        If the Direct3D API is the Direct3D 11.2 runtime and can support 11.2 features, <a href="https://msdn.microsoft.com/7edf2ffd-908a-4cf8-9ac6-8fd14d7a0ea1">ID3D11Device::CheckFeatureSupport</a> for <b>D3D11_FEATURE_D3D11_OPTIONS1</b> will return a SUCCESS code when valid parameters are passed. The members of <b>D3D11_FEATURE_DATA_D3D11_OPTIONS1</b> will be set appropriately based on the system's graphics hardware and graphics driver.
      

<h3><a id="Mappable_default_buffers"></a><a id="mappable_default_buffers"></a><a id="MAPPABLE_DEFAULT_BUFFERS"></a>Mappable default buffers</h3>
When creating a default buffer with <a href="https://msdn.microsoft.com/0a19c2a7-2570-40e2-8328-cbf5d7263605">D3D11_CPU_ACCESS_FLAG</a>, only the <b>D3D11_BIND_SHADER_RESOURCE</b> and <b>D3D11_BIND_UNORDERED_ACCESS</b> <a href="https://msdn.microsoft.com/4ffa1714-bd85-4d5a-930d-20526f46e4b9">bind flags</a> may be used.


            The <a href="https://msdn.microsoft.com/2a324055-21b0-4dad-a8e0-781905329dc2">D3D11_RESOURCE_MISC_FLAG</a> cannot be used when creating resources with <b>D3D11_CPU_ACCESS</b> flags.
          


            On non-unified memory architecture systems (discrete GPUs), apps should not use mappable default buffers if the compute shader code accesses the same byte in a default buffer more than once - sending the data across the bus multiple times eliminates the performance gained by mapping the default buffer instead of copying it.
          




## -see-also




<a href="https://msdn.microsoft.com/2a45182a-7114-4075-b8b8-147f52fe7aa9">Core Structures</a>



<a href="https://msdn.microsoft.com/48c3bf65-f077-45e6-a306-03d5760eeccb">D3D11_FEATURE</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=316897">DirectX Mappable Default Buffers SDK Sample</a>
 

 

