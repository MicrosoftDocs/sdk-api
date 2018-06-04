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

# D3D12_RESOURCE_BARRIER structure


## -description



          Describes a resource barrier (transition in resource use).
        


## -struct-fields




### -field Type


            A <a href="https://msdn.microsoft.com/B3364C92-777F-4207-9685-534B2F07B48F">D3D12_RESOURCE_BARRIER_TYPE</a>-typed value that specifies the type of resource barrier. 
            This member determines which type to use in the union below.
          


### -field Flags


            Specifies a <a href="https://msdn.microsoft.com/352DF566-2E30-49C6-9D1B-35F0AEEA3338">D3D12_RESOURCE_BARRIER_FLAGS</a> enumeration constant such as for "begin only" or "end only".
          


### -field Transition


              A <a href="https://msdn.microsoft.com/52C21198-827A-4E75-ADB8-DCA0204A4469">D3D12_RESOURCE_TRANSITION_BARRIER</a> structure that describes the transition of subresources between different usages.  
              Members specify the before and after usages of the subresources.
            


### -field Aliasing


              A 
              <a href="https://msdn.microsoft.com/9855D609-E863-4334-B6BA-B6777FDAB82B">D3D12_RESOURCE_ALIASING_BARRIER</a>
              structure that describes the transition between usages of two different resources that have mappings into the same heap.
            


### -field UAV


              A 
              <a href="https://msdn.microsoft.com/683F645F-9A90-4648-99EF-2F7444254B41">D3D12_RESOURCE_UAV_BARRIER</a>
              structure that describes a resource in which all UAV accesses (reads or writes) must complete before any future UAV accesses (read or write) can begin.
            


## -remarks




        This structure is used by the <a href="https://msdn.microsoft.com/AA788F94-122B-4132-BED5-162EAC683676">ID3D12GraphicsCommandList::ResourceBarrier</a> method.
      




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>



<a href="https://msdn.microsoft.com/3AB3BF34-433C-400B-921A-55B23CCDA44F">Using Resource Barriers to Synchronize Resource States in Direct3D 12</a>
 

 

