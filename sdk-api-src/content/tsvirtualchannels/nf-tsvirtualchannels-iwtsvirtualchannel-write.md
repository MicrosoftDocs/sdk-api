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

# IWTSVirtualChannel::Write


## -description


Starts a write request on the channel. All writes are considered asynchronous. Calling this method copies the contents of <i>pBuffer</i> and returns immediately, so  the buffer can be reclaimed. Because of the memory copy, too many <b>Write()</b> calls may result in allocating too much memory by the client.

A <a href="https://msdn.microsoft.com/b900789d-c7da-4974-8c46-72ea8ffd6892">Close()</a> call on this channel will cancel any pending writes.


## -parameters




### -param cbSize [in]

The size, in bytes, of the buffer to which to write.


### -param pBuffer [in]

A pointer to a buffer on the channel to which to write the data. You can reuse this buffer as soon as the call returns.


### -param pReserved [in, optional]

Reserved for future use. The value must be <b>NULL</b>.


## -returns



Returns <b>S_OK</b> if successful.




## -see-also




<a href="https://msdn.microsoft.com/8a5b093f-5756-400f-9442-b95d6010ee46">IWTSVirtualChannel</a>
 

 

