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

# IAudioEndpointRT::GetCurrentPadding


## -description


The <b>GetCurrentPadding</b> method gets the amount, in 100-nanosecond units, of data that is queued up in the endpoint.


## -parameters




### -param pPadding [out]

Receives the number of frames available in the endpoint buffer.


### -param pAeCurrentPosition [out]

Receives information about the position of the  current frame in the endpoint buffer in an <a href="https://msdn.microsoft.com/2e239114-1af7-455a-a60f-2054b05e1414">AE_CURRENT_POSITION</a> structure specified by the caller.


## -returns



This method does not return a value.




## -remarks



The audio engine uses this information to calculate the amount of data that requires processing.
    This calculation depends on the implementation.
    The  value of the <i>pPadding</i> parameter specifies the number of audio frames that are queued up to play in the endpoint buffer. Before writing to the endpoint buffer, the audio engine can calculate the amount of available space in the buffer by subtracting the padding value from the buffer length. For a CaptureStream endpoint, the padding value reported by the <b>GetCurrentPadding</b> method specifies the number of frames of capture data that are available in the next packet in the endpoint buffer and that might be ready for the audio engine to read from the buffer.

This method can be called from a real-time processing thread. The
    implementation of this method must not block, access
    paged memory, or call any blocking system routines.

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.




## -see-also




<a href="https://msdn.microsoft.com/3fb05ce4-a3be-4c84-8e03-71213f453f74">IAudioEndpointRT</a>
 

 

