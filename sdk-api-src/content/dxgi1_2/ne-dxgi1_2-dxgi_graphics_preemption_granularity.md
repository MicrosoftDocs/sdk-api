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

# DXGI_GRAPHICS_PREEMPTION_GRANULARITY enumeration


## -description


Identifies the granularity at which the graphics processing unit (GPU) can be preempted from performing its current graphics rendering task.


## -enum-fields




### -field DXGI_GRAPHICS_PREEMPTION_DMA_BUFFER_BOUNDARY

Indicates the preemption granularity as a DMA buffer.


### -field DXGI_GRAPHICS_PREEMPTION_PRIMITIVE_BOUNDARY

Indicates the preemption granularity as a graphics primitive. A primitive is a section in a DMA buffer and can be a group of triangles.


### -field DXGI_GRAPHICS_PREEMPTION_TRIANGLE_BOUNDARY

Indicates the preemption granularity as a triangle. A triangle is a part of a primitive.


### -field DXGI_GRAPHICS_PREEMPTION_PIXEL_BOUNDARY

Indicates the preemption granularity as a pixel. A pixel is a part of a triangle.


### -field DXGI_GRAPHICS_PREEMPTION_INSTRUCTION_BOUNDARY

Indicates the preemption granularity as a graphics instruction. A graphics instruction operates on a pixel.


## -remarks



You call the <a href="https://msdn.microsoft.com/DC1A054D-4092-4865-A6EF-B936891AA470">IDXGIAdapter2::GetDesc2</a> method to retrieve the granularity level at which the GPU can be preempted from performing its current graphics rendering task. The operating system specifies the graphics granularity level in the  <b>GraphicsPreemptionGranularity</b> member of the <a href="https://msdn.microsoft.com/AE34913A-84D8-49DB-A736-15AECA9989F9">DXGI_ADAPTER_DESC2</a> structure.

The following figure shows granularity of graphics rendering tasks.

<img alt="Graphics Rendering Granularity" src="images/Graphics_Preempt.png"/>



## -see-also




<a href="https://msdn.microsoft.com/c4574c89-dee2-4841-9318-5383cf417111">DXGI Enumerations</a>



<a href="https://msdn.microsoft.com/AE34913A-84D8-49DB-A736-15AECA9989F9">DXGI_ADAPTER_DESC2</a>
 

 

