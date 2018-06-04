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

# D3D12_RESOURCE_HEAP_TIER enumeration


## -description



          Specifies which resource heap tier the hardware and driver support.
        


## -enum-fields




### -field D3D12_RESOURCE_HEAP_TIER_1


            Indicates that heaps can only support resources from a single resource category.
            For the list of resource categories, see Remarks.
            In tier 1, these resource categories are mutually exclusive and cannot be used with the same heap.
            The resource category must be declared when creating a heap, using the correct <a href="https://msdn.microsoft.com/C3C1B611-714C-49DB-8034-9C9B7D6772E4">D3D12_HEAP_FLAGS</a> enumeration constant.
            Applications cannot create heaps with flags that allow all three categories.
          


### -field D3D12_RESOURCE_HEAP_TIER_2


            Indicates that heaps can support resources from all three categories.
            For the list of resource categories, see Remarks.
            In tier 2, these resource categories can be mixed within the same heap.
            Applications may create heaps with flags that allow all three categories; but are not required to do so.
            Applications may be written to support tier 1 and seamlessly run on tier 2.
          


## -remarks




          This enum is used by the <b>ResourceHeapTier</b> member of the <a href="https://msdn.microsoft.com/3193E3CC-C6CA-43D4-8D8C-41B7FCEE2BDF">D3D12_FEATURE_DATA_D3D12_OPTIONS</a> structure.
        


          This enum specifies which resource heap tier the hardware and driver support.
          Lower tiers require more heap attribution than greater tiers.
        


          Resources can be categorized into the following types:
        

<ul>
<li>Buffers</li>
<li>Non-render target &amp; non-depth stencil textures</li>
<li>Render target or depth stencil textures</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

