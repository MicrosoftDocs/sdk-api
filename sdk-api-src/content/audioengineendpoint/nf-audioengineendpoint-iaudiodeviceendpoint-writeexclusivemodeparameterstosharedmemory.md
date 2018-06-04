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

# IAudioDeviceEndpoint::WriteExclusiveModeParametersToSharedMemory


## -description


The 
   <b>WriteExclusiveModeParametersToSharedMemory</b> 
   method creates and writes the exclusive-mode parameters to shared memory.


## -parameters




### -param hTargetProcess [in]

The handle of the process for which the handles
    will be duplicated.


### -param hnsPeriod [in]

The periodicity, in 100-nanosecond units, of the device. This value must fall within the range of the 
      minimum and maximum periodicity of the device represented by the endpoint.


### -param hnsBufferDuration [in]

The buffer duration, in 100-nanosecond units, requested by the client.


### -param u32LatencyCoefficient [in]

The latency coefficient of the audio endpoint. A client can obtain the actual latency of the endpoint by 
      calling the <a href="https://msdn.microsoft.com/9afca6b7-2e0e-40a1-bb4a-932dad21b9eb">IAudioEndpoint::GetLatency</a> 
      method.


### -param pu32SharedMemorySize [out]

Receives the size of the memory area shared by the service and the process.


### -param phSharedMemory [out]

Receives a handle to the memory area shared by the service and the process.


## -returns



If the method succeeds, it returns <b>S_OK</b>.




## -remarks



This method is used to provide handles and parameters of the audio service of the endpoint to the client 
    process for use in exclusive mode. This method fails if the endpoint object is fully initialized through the 
    <a href="https://msdn.microsoft.com/345a172b-11af-4c98-9f9c-54bfa38c5077">IAudioDeviceEndpoint::SetBuffer</a> 
    method call.

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client 
    applications.




## -see-also




<a href="https://msdn.microsoft.com/3112bc7e-e138-4b42-8f82-61fdf19f7e94">IAudioDeviceEndpoint</a>
 

 

