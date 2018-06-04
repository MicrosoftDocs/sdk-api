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

# IStream::UnlockRegion


## -description



			The <b>UnlockRegion</b> method removes the access restriction on a range of bytes previously restricted with 
<a href="https://msdn.microsoft.com/f2606833-05ed-4bd0-a762-7b8172fb14c8">IStream::LockRegion</a>.


## -parameters




### -param libOffset [in]

Specifies the byte offset for the beginning of the range.


### -param cb [in]

Specifies, in bytes, the length of the range to be restricted.


### -param dwLockType [in]

Specifies the access restrictions previously placed on the range.


## -returns



This method can return one of these values.




## -remarks



<b>IStream::UnlockRegion</b> unlocks a region previously locked with the 
<a href="https://msdn.microsoft.com/f2606833-05ed-4bd0-a762-7b8172fb14c8">IStream::LockRegion</a> method. Locked regions must later be explicitly unlocked by calling <b>IStream::UnlockRegion</b> with exactly the same values for the <i>libOffset</i>, <i>cb</i>, and <i>dwLockType</i> parameters. The region must be unlocked before the stream is released. Two adjacent regions cannot be locked separately and then unlocked with a single unlock call.




## -see-also




<a href="https://msdn.microsoft.com/52474e37-0e14-4dcc-8e04-4442cfd26eb3">IStream - Compound File Implementation</a>



<a href="https://msdn.microsoft.com/f2606833-05ed-4bd0-a762-7b8172fb14c8">IStream::LockRegion</a>



<a href="https://msdn.microsoft.com/5d84fb08-aa4f-4918-a0de-550b02cb5287">LOCKTYPE</a>
 

 

