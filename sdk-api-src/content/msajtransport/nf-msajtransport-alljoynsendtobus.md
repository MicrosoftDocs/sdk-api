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

# AllJoynSendToBus function


## -description


Sends data to the bus via named pipe. The caller of this API is responsible to check if the <i>bytesTransferred</i> is less than the   
requested bytes and call this API again to resend the rest of the data.

When the named pipe <i>outBufferSize</i> is less than the <i>bytesToWrite</i>, writing to named pipe is returning TRUE and <i>bytesTransferred == 0</i>, rather than returning TRUE
	   and transferring as much as possible.


## -parameters




### -param connectedBusHandle [in]

Pipe handle.


### -param buffer [in]

Input data buffer.


### -param bytesToWrite [in]

Number of bytes to send.


### -param bytesTransferred [out, optional]

Number of bytes written.


### -param reserved [in, out]

May be used in a future version as OVERLAPPED address. Currently must be NULL.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.



