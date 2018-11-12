---
UID: NS:d3d12.D3D12_DISPATCH_ARGUMENTS
title: D3D12_DISPATCH_ARGUMENTS
author: windows-sdk-content
description: Describes dispatch parameters, for use by the compute shader.
old-location: direct3d12\d3d12_dispatch_arguments.htm
tech.root: direct3d12
ms.assetid: E48E4D01-DED2-4FB0-AD5A-EE1496ACF025
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: D3D12_DISPATCH_ARGUMENTS, D3D12_DISPATCH_ARGUMENTS structure, d3d12/D3D12_DISPATCH_ARGUMENTS, direct3d12.d3d12_dispatch_arguments
ms.prod: windows
ms.technology: windows-sdk
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
 - D3D12_DISPATCH_ARGUMENTS
product: Windows
targetos: Windows
req.typenames: D3D12_DISPATCH_ARGUMENTS
req.redist: 
---

# D3D12_DISPATCH_ARGUMENTS structure


## -description


Describes dispatch parameters, for use by the compute shader.


## -struct-fields




### -field ThreadGroupCountX

The size, in thread groups, of the x-dimension of the thread-group grid. 


### -field ThreadGroupCountY

The size, in thread groups, of the y-dimension of the thread-group grid.


### -field ThreadGroupCountZ

The size, in thread groups, of the z-dimension of the thread-group grid.  


## -remarks



The members of this structure serve the same purpose as the parameters of <a href="https://msdn.microsoft.com/948EE430-6B34-473D-9B5F-1C78CECFBF6F">Dispatch</a>.

 A compiled compute shader defines the set of instructions to execute per thread and the number of threads to run per group. The thread-group parameters  indicate how many thread groups to execute. Each thread group contains the same number of threads, as defined by the compiled compute shader. The thread groups are organized in a three-dimensional grid. The total number of thread groups that the compiled compute shader executes is determined by the following calculation:

<pre class="syntax" xml:space="preserve"><code>ThreadGroupCountX * ThreadGroupCountY * ThreadGroupCountZ</code></pre>
In particular, if any of the values in the thread-group parameters are 0, nothing will happen. 


The maximum size of any dimension is 65535.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

