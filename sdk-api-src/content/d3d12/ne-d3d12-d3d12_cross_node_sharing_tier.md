---
UID: NE:d3d12.D3D12_CROSS_NODE_SHARING_TIER
title: D3D12_CROSS_NODE_SHARING_TIER
author: windows-sdk-content
description: Specifies the level of sharing across nodes of an adapter, such as Tier 1 Emulated, Tier 1, or Tier 2.
old-location: direct3d12\d3d12_cross_node_sharing_tier.htm
old-project: direct3d12
ms.assetid: 49DAC69D-8134-4D1E-94B6-443978C24073
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: D3D12_CROSS_NODE_SHARING_TIER, D3D12_CROSS_NODE_SHARING_TIER enumeration, D3D12_CROSS_NODE_SHARING_TIER_1, D3D12_CROSS_NODE_SHARING_TIER_1_EMULATED, D3D12_CROSS_NODE_SHARING_TIER_2, D3D12_CROSS_NODE_SHARING_TIER_NOT_SUPPORTED, d3d12/D3D12_CROSS_NODE_SHARING_TIER, d3d12/D3D12_CROSS_NODE_SHARING_TIER_1, d3d12/D3D12_CROSS_NODE_SHARING_TIER_1_EMULATED, d3d12/D3D12_CROSS_NODE_SHARING_TIER_2, d3d12/D3D12_CROSS_NODE_SHARING_TIER_NOT_SUPPORTED, direct3d12.d3d12_cross_node_sharing_tier
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D12_CROSS_NODE_SHARING_TIER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_CROSS_NODE_SHARING_TIER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_CROSS_NODE_SHARING_TIER enumeration


## -description



          Specifies the level of sharing across nodes of an adapter, such as Tier 1 Emulated, Tier 1, or Tier 2.
        


## -enum-fields




### -field D3D12_CROSS_NODE_SHARING_TIER_NOT_SUPPORTED


              If an adapter only has 1 node, then cross-node sharing doesn't apply, so
              the <b>CrossNodeSharingTier</b> member of the <a href="https://msdn.microsoft.com/3193E3CC-C6CA-43D4-8D8C-41B7FCEE2BDF">D3D12_FEATURE_DATA_D3D12_OPTIONS</a> structure
              is set to D3D12_CROSS_NODE_SHARING_NOT_SUPPORTED.
            


### -field D3D12_CROSS_NODE_SHARING_TIER_1_EMULATED


            Tier 1 Emulated.
            Devices that set
            the <b>CrossNodeSharingTier</b> member of the <a href="https://msdn.microsoft.com/3193E3CC-C6CA-43D4-8D8C-41B7FCEE2BDF">D3D12_FEATURE_DATA_D3D12_OPTIONS</a> structure
            to D3D12_CROSS_NODE_SHARING_TIER_1_EMULATED have Tier 1 support.
            However, drivers stage these copy operations through a driver-internal system memory allocation.
            This will cause these copy operations to consume time on the destination GPU as well as the source.
          


### -field D3D12_CROSS_NODE_SHARING_TIER_1


            Tier 1.
            Devices that set
            the <b>CrossNodeSharingTier</b> member of the <a href="https://msdn.microsoft.com/3193E3CC-C6CA-43D4-8D8C-41B7FCEE2BDF">D3D12_FEATURE_DATA_D3D12_OPTIONS</a> structure
            to D3D12_CROSS_NODE_SHARING_TIER_1 only support the following cross-node copy operations:
            

<ul>
<li>
<a href="https://msdn.microsoft.com/46F89B85-EDAA-4095-B6C6-4CC47F972F09">ID3D12CommandList::CopyBufferRegion</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2EAFC6B9-376C-4801-8E53-BF0DB08943AA">ID3D12CommandList::CopyTextureRegion</a>
</li>
<li>
<a href="https://msdn.microsoft.com/EFC305CF-FBA9-4192-999B-6C6BFCDFF51F">ID3D12CommandList::CopyResource</a>
</li>
</ul>

            Additionally, the cross-node resource must be the destination of the copy operation.
          


### -field D3D12_CROSS_NODE_SHARING_TIER_2


            Tier 2.
            Devices that set
            the <b>CrossNodeSharingTier</b> member of the <a href="https://msdn.microsoft.com/3193E3CC-C6CA-43D4-8D8C-41B7FCEE2BDF">D3D12_FEATURE_DATA_D3D12_OPTIONS</a> structure
            to D3D12_CROSS_NODE_SHARING_TIER_2 support all operations across nodes, except for the following:
            

<ul>
<li>
                Render target views.
              </li>
<li>
                Depth stencil views.
              </li>
<li>
                UAV atomic operations.
                Similar to CPU/GPU interop, shaders may perform UAV atomic operations; however, no atomicity across adapters is guaranteed.
              </li>
</ul>

            Applications can retrieve the node where a resource/heap exists from the <a href="https://msdn.microsoft.com/3A473476-F37E-4F01-B121-87E998EE9411">D3D12_HEAP_DESC</a> structure.
            These values are retrievable for opened resources.
            The runtime performs the appropriate re-mapping in case the 2 devices are using different UMD-specified node re-mappings.
          


### -field D3D12_CROSS_NODE_SHARING_TIER_3




## -remarks




          This enum is used by
          the <b>CrossNodeSharingTier</b> member of the <a href="https://msdn.microsoft.com/3193E3CC-C6CA-43D4-8D8C-41B7FCEE2BDF">D3D12_FEATURE_DATA_D3D12_OPTIONS</a> structure.
        




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

