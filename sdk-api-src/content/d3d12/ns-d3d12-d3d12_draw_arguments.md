---
UID: NS:d3d12.D3D12_DRAW_ARGUMENTS
title: D3D12_DRAW_ARGUMENTS
author: windows-sdk-content
description: Describes parameters for drawing instances.
old-location: direct3d12\d3d12_draw_arguments.htm
tech.root: direct3d12
ms.assetid: 300F3628-C8E8-44BF-BCEC-579E6DA80347
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D12_DRAW_ARGUMENTS, D3D12_DRAW_ARGUMENTS structure, d3d12/D3D12_DRAW_ARGUMENTS, direct3d12.d3d12_draw_arguments
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_DRAW_ARGUMENTS
product: Windows
targetos: Windows
req.typenames: D3D12_DRAW_ARGUMENTS
req.redist: 
---

# D3D12_DRAW_ARGUMENTS structure


## -description


Describes parameters for drawing instances.


## -struct-fields




### -field VertexCountPerInstance

Specifies the number of vertices to draw, per instance.


### -field InstanceCount

Specifies the number of instances.


### -field StartVertexLocation

Specifies an index to the first vertex to start drawing from.


### -field StartInstanceLocation

Specifies an index to the first instance to start drawing from.


## -remarks



The members of this structure serve the same purpose as the parameters of  <a href="https://msdn.microsoft.com/BB10C732-1F42-417D-ADDE-55E870AD5FE9">DrawInstanced</a>.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

