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

# IAudioDeviceEndpoint::SetBuffer


## -description


The <b>SetBuffer</b> method initializes the endpoint and creates a buffer based on the format of the endpoint into which the audio data is streamed.


## -parameters




### -param MaxPeriod [in]

The processing time, in 
    100-nanosecond units, of the audio endpoint.


### -param u32LatencyCoefficient [in]

The latency coefficient for the audio          device. This value is used to calculate the latency. Latency = <i>u32LatencyCoefficient</i> * <i>MaxPeriod</i>.

<div class="alert"><b>Note</b>  The device that the endpoint represents has a minimum latency
    value. If the value of this parameter is less than the minimum latency of the device or is zero, the
     endpoint object applies the minimum latency.  The audio engine can obtain the
    actual latency of the endpoint by calling the <a href="https://msdn.microsoft.com/9afca6b7-2e0e-40a1-bb4a-932dad21b9eb">IAudioEndpoint::GetLatency</a> method.</div>
<div> </div>

## -returns



If the method succeeds, it returns <b>S_OK</b>.

If it fails, possible return codes include, but are not limited to, the following.




## -remarks



The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.




## -see-also




<a href="https://msdn.microsoft.com/3112bc7e-e138-4b42-8f82-61fdf19f7e94">IAudioDeviceEndpoint</a>
 

 

