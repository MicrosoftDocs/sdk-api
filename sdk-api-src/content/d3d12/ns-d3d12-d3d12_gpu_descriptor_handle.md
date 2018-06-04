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

# D3D12_GPU_DESCRIPTOR_HANDLE structure


## -description



        Describes a GPU descriptor handle.
      


## -struct-fields




### -field ptr


            The address of the descriptor.
          


## -remarks




        This structure is returned by <a href="https://msdn.microsoft.com/63A031A1-EF53-4308-A8F9-179E21C7CE7B">ID3D12DescriptorHeap::GetGPUDescriptorHandleForHeapStart</a>.
      


        This structure is passed into the following methods:
        

<ul>
<li>
<a href="https://msdn.microsoft.com/6A19F429-D7B2-4A71-8904-31BFA1FD10C6">ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat</a>
</li>
<li>
<a href="https://msdn.microsoft.com/A048BF0C-9141-4DDF-91F9-B53464033A44">ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint</a>
</li>
<li>
<a href="https://msdn.microsoft.com/DC05D64A-39D0-4EF2-A9FE-956B499386F2">ID3D12GraphicsCommandList:SetComputeRootDescriptorTable</a>
</li>
<li>
<a href="https://msdn.microsoft.com/AF182E9D-6A85-42B2-ADE4-490756AEDCE7">ID3D12GraphicsCommandList::SetGraphicsRootDescriptorTable</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/6E405AD6-D370-4B87-849A-C52D64C79BF7">CD3DX12_GPU_DESCRIPTOR_HANDLE</a>



<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

