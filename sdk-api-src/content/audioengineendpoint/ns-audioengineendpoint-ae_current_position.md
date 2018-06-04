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

# AE_CURRENT_POSITION structure


## -description


Reports the current frame position from the device to the clients.


## -struct-fields




### -field u64DevicePosition

The device position, in frames.


### -field u64StreamPosition

The stream position, in frames, used to determine the starting point for audio capture and the render device position relative to the stream.


### -field u64PaddingFrames

The amount of padding, in frames, between the current position and the stream fill point.


### -field hnsQPCPosition

A translated quality performance counter (QPC) timer value taken at the time that the <b>u64DevicePosition</b> member was checked.


### -field f32FramesPerSecond

The calculated data rate at the point at the time the  position was set.


### -field Flag

A value of the <a href="https://msdn.microsoft.com/09edc9ae-923c-4f57-9479-c0331588dd92">AE_POSITION_FLAGS</a> enumeration that indicates the validity of the position information.


## -remarks



The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.




## -see-also




<a href="https://msdn.microsoft.com/f61497c8-35da-4fbf-af83-1f15d5fe94f7">IAudioEndpointRT::GetCurrentPadding</a>



<a href="https://msdn.microsoft.com/1da81a49-d421-4643-9be6-b13d45d678f0">IAudioInputEndpointRT::GetInputDataPointer</a>



<a href="https://msdn.microsoft.com/14d69520-3d0c-42ee-8986-9d83b5cff62e">IAudioOutputEndpointRT::GetOutputDataPointer</a>
 

 

