---
UID: NE:dxgi1_2.DXGI_COMPUTE_PREEMPTION_GRANULARITY
title: DXGI_COMPUTE_PREEMPTION_GRANULARITY (dxgi1_2.h)
description: Identifies the granularity at which the graphics processing unit (GPU) can be preempted from performing its current compute task.
helpviewer_keywords: ["DXGI_COMPUTE_PREEMPTION_DISPATCH_BOUNDARY","DXGI_COMPUTE_PREEMPTION_DMA_BUFFER_BOUNDARY","DXGI_COMPUTE_PREEMPTION_GRANULARITY","DXGI_COMPUTE_PREEMPTION_GRANULARITY enumeration [DXGI]","DXGI_COMPUTE_PREEMPTION_INSTRUCTION_BOUNDARY","DXGI_COMPUTE_PREEMPTION_THREAD_BOUNDARY","DXGI_COMPUTE_PREEMPTION_THREAD_GROUP_BOUNDARY","direct3ddxgi.dxgi_compute_preemption_granularity","dxgi1_2/DXGI_COMPUTE_PREEMPTION_DISPATCH_BOUNDARY","dxgi1_2/DXGI_COMPUTE_PREEMPTION_DMA_BUFFER_BOUNDARY","dxgi1_2/DXGI_COMPUTE_PREEMPTION_GRANULARITY","dxgi1_2/DXGI_COMPUTE_PREEMPTION_INSTRUCTION_BOUNDARY","dxgi1_2/DXGI_COMPUTE_PREEMPTION_THREAD_BOUNDARY","dxgi1_2/DXGI_COMPUTE_PREEMPTION_THREAD_GROUP_BOUNDARY"]
old-location: direct3ddxgi\dxgi_compute_preemption_granularity.htm
tech.root: direct3ddxgi
ms.assetid: DEE6E26D-B4BB-4832-9CFC-4167F399BC65
ms.date: 12/05/2018
ms.keywords: DXGI_COMPUTE_PREEMPTION_DISPATCH_BOUNDARY, DXGI_COMPUTE_PREEMPTION_DMA_BUFFER_BOUNDARY, DXGI_COMPUTE_PREEMPTION_GRANULARITY, DXGI_COMPUTE_PREEMPTION_GRANULARITY enumeration [DXGI], DXGI_COMPUTE_PREEMPTION_INSTRUCTION_BOUNDARY, DXGI_COMPUTE_PREEMPTION_THREAD_BOUNDARY, DXGI_COMPUTE_PREEMPTION_THREAD_GROUP_BOUNDARY, direct3ddxgi.dxgi_compute_preemption_granularity, dxgi1_2/DXGI_COMPUTE_PREEMPTION_DISPATCH_BOUNDARY, dxgi1_2/DXGI_COMPUTE_PREEMPTION_DMA_BUFFER_BOUNDARY, dxgi1_2/DXGI_COMPUTE_PREEMPTION_GRANULARITY, dxgi1_2/DXGI_COMPUTE_PREEMPTION_INSTRUCTION_BOUNDARY, dxgi1_2/DXGI_COMPUTE_PREEMPTION_THREAD_BOUNDARY, dxgi1_2/DXGI_COMPUTE_PREEMPTION_THREAD_GROUP_BOUNDARY
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DXGI_COMPUTE_PREEMPTION_GRANULARITY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_COMPUTE_PREEMPTION_GRANULARITY
 - dxgi1_2/DXGI_COMPUTE_PREEMPTION_GRANULARITY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGI1_2.h
api_name:
 - DXGI_COMPUTE_PREEMPTION_GRANULARITY
---

# DXGI_COMPUTE_PREEMPTION_GRANULARITY enumeration


## -description

Identifies the granularity at which the graphics processing unit (GPU) can be preempted from performing its current compute task.

## -enum-fields

### -field DXGI_COMPUTE_PREEMPTION_DMA_BUFFER_BOUNDARY:0

Indicates the preemption granularity as a compute packet.

### -field DXGI_COMPUTE_PREEMPTION_DISPATCH_BOUNDARY:1

Indicates the preemption granularity as a dispatch (for example, a call to the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch">ID3D11DeviceContext::Dispatch</a> method). A dispatch is a part of a compute packet.

### -field DXGI_COMPUTE_PREEMPTION_THREAD_GROUP_BOUNDARY:2

Indicates the preemption granularity as a thread group. A thread group is a part of a dispatch.

### -field DXGI_COMPUTE_PREEMPTION_THREAD_BOUNDARY:3

Indicates the preemption granularity as a thread in a thread group. A thread is a part of a thread group.

### -field DXGI_COMPUTE_PREEMPTION_INSTRUCTION_BOUNDARY:4

Indicates the preemption granularity as a compute instruction in a thread.

## -remarks

You call the <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiadapter2-getdesc2">IDXGIAdapter2::GetDesc2</a> method to retrieve the granularity level at which the GPU can be preempted from performing its current compute task. The operating system specifies the compute granularity level in the  <b>ComputePreemptionGranularity</b> member of the <a href="/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_adapter_desc2">DXGI_ADAPTER_DESC2</a> structure.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-enums">DXGI Enumerations</a>



<a href="/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_adapter_desc2">DXGI_ADAPTER_DESC2</a>
