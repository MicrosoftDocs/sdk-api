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

# ILockBytes::UnlockRegion


## -description


The <b>UnlockRegion</b> method removes the access restriction on a previously locked range of bytes.


## -parameters




### -param libOffset [in]

Specifies the byte offset for the beginning of the range.


### -param cb [in]

Specifies, in bytes, the length of the range that is restricted.


### -param dwLockType [in]

Specifies the type of access restrictions previously placed on the range. This parameter uses a value from the 
<a href="https://msdn.microsoft.com/5d84fb08-aa4f-4918-a0de-550b02cb5287">LOCKTYPE</a> enumeration.


## -returns



This method can return one of these values.




## -remarks



<b>ILockBytes::UnlockRegion</b> unlocks a region previously locked with a call to 
<a href="https://msdn.microsoft.com/cea59e2a-99d8-472d-8e4f-2e2474789c20">ILockBytes::LockRegion</a>. Each region locked must be explicitly unlocked, using the same values for the <i>libOffset</i>, <i>cb</i>, and <i>dwLockType</i> parameters as in the matching calls to <b>ILockBytes::LockRegion</b>. Two adjacent regions cannot be locked separately and then unlocked with a single unlock call.




## -see-also




<a href="https://msdn.microsoft.com/700b6a3c-1046-4c21-8887-16f344c23510">ILockBytes - File-Based Implementation</a>



<a href="https://msdn.microsoft.com/6ab019b0-34d7-4b6e-ba77-6b6881fabd29">ILockBytes - Global Memory Implementation</a>



<a href="https://msdn.microsoft.com/cea59e2a-99d8-472d-8e4f-2e2474789c20">ILockBytes::LockRegion</a>



<a href="https://msdn.microsoft.com/5d84fb08-aa4f-4918-a0de-550b02cb5287">LOCKTYPE</a>
 

 

