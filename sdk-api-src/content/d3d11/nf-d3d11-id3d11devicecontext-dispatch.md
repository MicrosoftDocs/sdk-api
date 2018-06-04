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

# ID3D11DeviceContext::Dispatch


## -description


Execute a command list from a thread group.


## -parameters




### -param ThreadGroupCountX [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of groups dispatched in the x direction. <i>ThreadGroupCountX</i> must be less than or equal to D3D11_CS_DISPATCH_MAX_THREAD_GROUPS_PER_DIMENSION (65535).


### -param ThreadGroupCountY [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of groups dispatched in the y direction. <i>ThreadGroupCountY</i> must be less than or equal to D3D11_CS_DISPATCH_MAX_THREAD_GROUPS_PER_DIMENSION (65535).


### -param ThreadGroupCountZ [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of groups dispatched in the z direction.  <i>ThreadGroupCountZ</i> must be less than or equal to D3D11_CS_DISPATCH_MAX_THREAD_GROUPS_PER_DIMENSION (65535). 
        In feature level 10 the value for <i>ThreadGroupCountZ</i> must be 1.


## -returns



Returns nothing.




## -remarks



You call the <b>Dispatch</b> method to execute commands in a <a href="https://msdn.microsoft.com/02c1f98e-fdd6-49b0-b8b2-efbd472ab599">compute shader</a>. A compute shader can be run on many threads in parallel, within a thread group. Index a particular thread, within a thread group using a 3D vector 
      given by (x,y,z).

In the following illustration, assume a thread group with 50 threads where the size of the group is given by (5,5,2). A single thread is identified from a 
      thread group with 50 threads in it, using the vector (4,1,1).

<img alt="Illustration of a single thread within a thread group of 50 threads" src="images/d3d11_thread_group_1.png"/>

The following illustration shows the relationship between the parameters passed to <b>ID3D11DeviceContext::Dispatch</b>, Dispatch(5,3,2), the values specified in the <a href="https://msdn.microsoft.com/ec6b751c-d81c-4221-ae80-166d2a3707fe">numthreads</a> attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values 
(<a href="https://msdn.microsoft.com/e793be10-7c83-478c-859a-4b0a2c537570">SV_GroupIndex</a>,<a href="https://msdn.microsoft.com/bad697f6-26d9-47cd-93e5-127621a161e8">SV_DispatchThreadID</a>,<a href="https://msdn.microsoft.com/be944592-c4ea-43c9-88bc-98a9a190a437">SV_GroupThreadID</a>,<a href="https://msdn.microsoft.com/1b90ca74-a2b6-4a5f-aa4a-1ec879360593">SV_GroupID</a>).

<img alt="Illustration of the relationship between Dispatch, thread groups, and threads" src="images/ThreadGroupIDs.png"/>




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

