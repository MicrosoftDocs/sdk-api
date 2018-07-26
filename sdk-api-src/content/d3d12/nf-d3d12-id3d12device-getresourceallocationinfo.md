---
UID: NF:d3d12.ID3D12Device.GetResourceAllocationInfo
title: ID3D12Device::GetResourceAllocationInfo
author: windows-sdk-content
description: Gets the size and alignment of memory required for a collection of resources on this adapter.
old-location: direct3d12\id3d12device_getresourceallocationinfo.htm
old-project: direct3d12
ms.assetid: 43467E09-835B-4DB9-B0A4-F75868DE4609
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: GetResourceAllocationInfo, GetResourceAllocationInfo method, GetResourceAllocationInfo method,ID3D12Device interface, ID3D12Device interface,GetResourceAllocationInfo method, ID3D12Device.GetResourceAllocationInfo, ID3D12Device::GetResourceAllocationInfo, d3d12/ID3D12Device::GetResourceAllocationInfo, direct3d12.id3d12device_getresourceallocationinfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: D3D_SHADER_MODEL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12Device.GetResourceAllocationInfo
product: Windows
targetos: Windows
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
---

# ID3D12Device::GetResourceAllocationInfo


## -description


Gets the size and alignment of memory required for a collection of resources on this adapter.
        


## -parameters




### -param visibleMask [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

For single GPU operation, set this to zero. 
            If there are multiple GPU nodes, set bits to identify the nodes (the  device's physical adapters).
            Each bit in the mask corresponds to a single node.
            Refer to <a href="https://msdn.microsoft.com/CC4C6594-D48F-40C1-93EE-9F98532BC038">Multi-Adapter</a>.


### -param numResourceDescs [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of resource descriptors in the <i>pResourceDescs</i> array.
          


### -param pResourceDescs [in]

Type: <b>const <a href="https://msdn.microsoft.com/908BCB65-A7C6-473D-81AB-CCCA029AB6F9">D3D12_RESOURCE_DESC</a>*</b>

An array of <a href="https://msdn.microsoft.com/908BCB65-A7C6-473D-81AB-CCCA029AB6F9">D3D12_RESOURCE_DESC</a> structures that described the resources to get info about.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/ADBF5402-C1B5-4A10-92DF-E9F5706F52A1">D3D12_RESOURCE_ALLOCATION_INFO</a></b>

Returns a <a href="https://msdn.microsoft.com/ADBF5402-C1B5-4A10-92DF-E9F5706F52A1">D3D12_RESOURCE_ALLOCATION_INFO</a> structure that provides info about video memory allocated for the specified array of resources.
          




## -remarks



When using <a href="https://msdn.microsoft.com/4581A82D-D2B6-4CAE-A336-07B8CF90A0BA">CreatePlacedResource</a>, the application must use this method to understand the size and alignment characteristics of texture resources. 
          The results of this method vary depending on the particular adapter, and must be treated as unique to this adapter and driver version.
        

Applications cannot use the output of <b>GetResourceAllocationInfo</b> to understand packed mip properties of textures.
          To understand packed mip properties of textures, applications must use <a href="https://msdn.microsoft.com/32574750-92D3-4CAF-90C6-BA0DEF1E5464">GetResourceTiling</a>. 
          Texture resource sizes significantly differ from the information returned by <b>GetResourceTiling</b>, because some adapter architectures allocate extra memory for textures to reduce the effective bandwidth during common rendering scenarios. 
          This even includes textures that have constraints on their texture layouts or have standardized texture layouts. 
          That extra memory cannot be sparsely mapped or remapped by an application using <a href="https://msdn.microsoft.com/37E74129-1B5C-4997-A584-D7E9F92342EA">CreateReservedResource</a> and 
          <a href="https://msdn.microsoft.com/8A8017E5-AB55-4660-855B-D6F93F69CB52">UpdateTileMappings</a>, so it isn't reported in <b>GetResourceTiling</b>.
        

Applications can forgo using <b>GetResourceAllocationInfo</b> for buffer resources (<a href="https://msdn.microsoft.com/E04F3124-01FB-4EE7-BDF8-4821F2F1FCEB">D3D12_RESOURCE_DIMENSION</a>_BUFFER). 
          Buffers have the same size on all adapters, which is merely the smallest multiple of 64KB which is greater or equal to <a href="https://msdn.microsoft.com/908BCB65-A7C6-473D-81AB-CCCA029AB6F9">D3D12_RESOURCE_DESC</a>::<b>Width</b>.
        

When multiple resource descriptions are passed in, the C++ algorithm for calculating a structure size and alignment are used. 
          For example, a three-element array with two tiny 64KB-aligned resources and a tiny 4MB-aligned resource reports differing sizes based on the order of the array. 
          If the 4MB aligned resource is in the middle, the resulting <b>Size</b> is 12MB. 
          Otherwise, the resulting <b>Size</b> is 8MB. 
          The <b>Alignment</b> returned would always be 4MB, as it is the superset of all alignments in the resource array.
        




## -see-also




<a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a>
 

 

