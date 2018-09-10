---
UID: NF:audioengineendpoint.IAudioDeviceEndpoint.SetBuffer
title: IAudioDeviceEndpoint::SetBuffer
author: windows-sdk-content
description: Initializes the endpoint and creates a buffer based on the format of the endpoint into which the audio data is streamed.
old-location: termserv\iaudiodeviceendpoint_setbuffer.htm
tech.root: termserv
ms.assetid: 345a172b-11af-4c98-9f9c-54bfa38c5077
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IAudioDeviceEndpoint interface [Remote Desktop Services],SetBuffer method, IAudioDeviceEndpoint.SetBuffer, IAudioDeviceEndpoint::SetBuffer, SetBuffer, SetBuffer method [Remote Desktop Services], SetBuffer method [Remote Desktop Services],IAudioDeviceEndpoint interface, audioengineendpoint/IAudioDeviceEndpoint::SetBuffer, termserv.iaudiodeviceendpoint_setbuffer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: audioengineendpoint.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
 - COM
api_location:
 - Audioengineendpoint.h
api_name:
 - IAudioDeviceEndpoint.SetBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

