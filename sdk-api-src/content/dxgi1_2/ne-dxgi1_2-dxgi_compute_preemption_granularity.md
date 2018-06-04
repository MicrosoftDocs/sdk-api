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

# DXGI_COMPUTE_PREEMPTION_GRANULARITY enumeration


## -description


Identifies the granularity at which the graphics processing unit (GPU) can be preempted from performing its current compute task.


## -enum-fields




### -field DXGI_COMPUTE_PREEMPTION_DMA_BUFFER_BOUNDARY

Indicates the preemption granularity as a compute packet.


### -field DXGI_COMPUTE_PREEMPTION_DISPATCH_BOUNDARY

Indicates the preemption granularity as a dispatch (for example, a call to the <a href="https://msdn.microsoft.com/7d3401bb-521f-4ab0-8833-e5caf712d0c9">ID3D11DeviceContext::Dispatch</a> method). A dispatch is a part of a compute packet.


### -field DXGI_COMPUTE_PREEMPTION_THREAD_GROUP_BOUNDARY

Indicates the preemption granularity as a thread group. A thread group is a part of a dispatch.


### -field DXGI_COMPUTE_PREEMPTION_THREAD_BOUNDARY

Indicates the preemption granularity as a thread in a thread group. A thread is a part of a thread group.


### -field DXGI_COMPUTE_PREEMPTION_INSTRUCTION_BOUNDARY

Indicates the preemption granularity as a compute instruction in a thread.


## -remarks



You call the <a href="https://msdn.microsoft.com/DC1A054D-4092-4865-A6EF-B936891AA470">IDXGIAdapter2::GetDesc2</a> method to retrieve the granularity level at which the GPU can be preempted from performing its current compute task. The operating system specifies the compute granularity level in the  <b>ComputePreemptionGranularity</b> member of the <a href="https://msdn.microsoft.com/AE34913A-84D8-49DB-A736-15AECA9989F9">DXGI_ADAPTER_DESC2</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/c4574c89-dee2-4841-9318-5383cf417111">DXGI Enumerations</a>



<a href="https://msdn.microsoft.com/AE34913A-84D8-49DB-A736-15AECA9989F9">DXGI_ADAPTER_DESC2</a>
 

 

