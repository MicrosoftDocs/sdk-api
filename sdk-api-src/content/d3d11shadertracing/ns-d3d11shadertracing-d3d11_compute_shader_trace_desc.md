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

# D3D11_COMPUTE_SHADER_TRACE_DESC structure


## -description


Describes an instance of a compute shader to trace.


## -struct-fields




### -field Invocation

The invocation number of the instance of the compute shader.


### -field ThreadIDInGroup


            The <a href="https://msdn.microsoft.com/be944592-c4ea-43c9-88bc-98a9a190a437">SV_GroupThreadID</a> to trace. This value identifies indexes of individual threads within a thread group that a compute shader executes in.
          


### -field ThreadGroupID


            The <a href="https://msdn.microsoft.com/1b90ca74-a2b6-4a5f-aa4a-1ec879360593">SV_GroupID</a> to trace. This value identifies indexes of a thread group that the compute shader executes in.
          


## -remarks




        This API requires the Windows Software Development Kit (SDK) for Windows 8.
      




## -see-also




<a href="https://msdn.microsoft.com/3b8ece5c-5065-4711-b12c-06cf7ea0e1ba">Shader Structures</a>
 

 

