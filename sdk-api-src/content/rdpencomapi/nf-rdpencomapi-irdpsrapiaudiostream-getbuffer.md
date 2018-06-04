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

# IRDPSRAPIAudioStream::GetBuffer


## -description


Gets audio data from the buffer.   
   This method locks an internal buffer and returns a pointer to a specific location in that buffer. It does not  allocate a copy of the buffer for the caller.  To release the buffer after the last call to this method,   call  the <a href="https://msdn.microsoft.com/03926ABF-D5D0-4D13-B081-0085EC698E9F">FreeBuffer</a> method.


## -parameters




### -param ppbData [out]

A pointer to the current location in the buffer.


### -param pcbData [out]

The size in bytes of the available data in the buffer.


### -param pTimestamp [out]

The time-based location of the location pointer.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.




## -see-also




<a href="https://msdn.microsoft.com/03926ABF-D5D0-4D13-B081-0085EC698E9F">FreeBuffer</a>



<a href="https://msdn.microsoft.com/B2BC04A1-DE22-4543-9F10-33B0B99E0F92">IRDPSRAPIAudioStream</a>
 

 

