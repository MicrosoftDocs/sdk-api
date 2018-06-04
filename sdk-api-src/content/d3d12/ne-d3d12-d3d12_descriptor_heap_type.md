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

# D3D12_DESCRIPTOR_HEAP_TYPE enumeration


## -description



          Specifies a type of descriptor heap.
        


## -enum-fields




### -field D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV


            The descriptor heap for the combination of constant-buffer, shader-resource, and unordered-access views.
          


### -field D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER


            The descriptor heap for the sampler.
          


### -field D3D12_DESCRIPTOR_HEAP_TYPE_RTV


            The descriptor heap for the render-target view.
          


### -field D3D12_DESCRIPTOR_HEAP_TYPE_DSV


            The descriptor heap for the depth-stencil view.
          


### -field D3D12_DESCRIPTOR_HEAP_TYPE_NUM_TYPES


            The number of types of descriptor heaps.
          


## -remarks




        This enum is used by the <a href="https://msdn.microsoft.com/060ED49E-12B2-4DAE-A9DC-5BAB96B8E8ED">D3D12_DESCRIPTOR_HEAP_DESC</a> structure, and the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/F995EF34-74FF-4FCA-A018-E2F48DF92450">CopyDescriptors</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6DA1FCDA-042C-4727-9814-B8F57E14CD51">CopyDescriptorsSimple</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4593C153-913A-49DF-ADDC-6FB1E19D3D17">GetDescriptorHandleIncrementSize</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>



<a href="https://msdn.microsoft.com/58677023-692C-4BA4-90B7-D568F3DD3F73">Creating Descriptor Heaps</a>



<a href="https://msdn.microsoft.com/04D3FACF-21EC-45CA-AD9B-78FDCDDC7136">Descriptor Heaps</a>
 

 

