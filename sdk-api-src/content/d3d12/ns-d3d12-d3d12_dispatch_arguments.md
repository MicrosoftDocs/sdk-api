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
 

 

