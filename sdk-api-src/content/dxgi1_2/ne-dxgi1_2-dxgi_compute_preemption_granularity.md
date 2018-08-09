---
UID: NE:dxgi1_2.DXGI_COMPUTE_PREEMPTION_GRANULARITY
title: DXGI_COMPUTE_PREEMPTION_GRANULARITY
author: windows-sdk-content
description: Identifies the granularity at which the graphics processing unit (GPU) can be preempted from performing its current compute task.
old-location: direct3ddxgi\dxgi_compute_preemption_granularity.htm
old-project: direct3ddxgi
ms.assetid: DEE6E26D-B4BB-4832-9CFC-4167F399BC65
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: DXGI_COMPUTE_PREEMPTION_DISPATCH_BOUNDARY, DXGI_COMPUTE_PREEMPTION_DMA_BUFFER_BOUNDARY, DXGI_COMPUTE_PREEMPTION_GRANULARITY, DXGI_COMPUTE_PREEMPTION_GRANULARITY enumeration [DXGI], DXGI_COMPUTE_PREEMPTION_INSTRUCTION_BOUNDARY, DXGI_COMPUTE_PREEMPTION_THREAD_BOUNDARY, DXGI_COMPUTE_PREEMPTION_THREAD_GROUP_BOUNDARY, direct3ddxgi.dxgi_compute_preemption_granularity, dxgi1_2/DXGI_COMPUTE_PREEMPTION_DISPATCH_BOUNDARY, dxgi1_2/DXGI_COMPUTE_PREEMPTION_DMA_BUFFER_BOUNDARY, dxgi1_2/DXGI_COMPUTE_PREEMPTION_GRANULARITY, dxgi1_2/DXGI_COMPUTE_PREEMPTION_INSTRUCTION_BOUNDARY, dxgi1_2/DXGI_COMPUTE_PREEMPTION_THREAD_BOUNDARY, dxgi1_2/DXGI_COMPUTE_PREEMPTION_THREAD_GROUP_BOUNDARY
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: DXGI_COMPUTE_PREEMPTION_GRANULARITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGI1_2.h
api_name:
 - DXGI_COMPUTE_PREEMPTION_GRANULARITY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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
 

 

