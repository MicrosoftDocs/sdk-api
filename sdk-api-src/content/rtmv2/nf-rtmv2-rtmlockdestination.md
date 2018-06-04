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

# RtmLockDestination function


## -description


The 
<b>RtmLockDestination</b> function locks or unlocks a destination in the routing table. Use this function to protect a destination while changing opaque pointers.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


### -param DestHandle [in]

Handle to the destination to lock.


### -param Exclusive [in]

Specifies whether to lock or unlock the destination in an exclusive (<b>TRUE</b>) or shared (<b>FALSE</b>) mode.


### -param LockDest [in]

Specifies whether to lock or unlock the destination. Specify <b>TRUE</b> to lock the destination; specify <b>FALSE</b> to unlock it.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The calling client does not own this destination.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle is invalid.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



This function also locks the associated routes. Avoid locking destinations for long periods of time, because no other client can access the destination and associated routes until the lock is released.

A client can also use this function when reading information for a destination, while preventing changes during the client's read operation. In this case, consider using 
<a href="https://msdn.microsoft.com/bf6525ea-5f32-41d3-b436-920e7369b926">RtmGetDestInfo</a> instead.

For sample code using this function, see 
<a href="https://msdn.microsoft.com/3598a28f-8ade-4b3f-9d31-4f2c84df2dd6">Update a Route In Place Using RtmUpdateAndUnlockRoute</a>.




## -see-also




<a href="https://msdn.microsoft.com/7ad948fa-cd00-4496-bd62-433d7faa0f85">RtmGetOpaqueInformationPointer</a>
 

 

