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

# tagLOCKTYPE enumeration


## -description



			The 
<b>LOCKTYPE</b> enumeration values indicate the type of locking requested for the specified range of bytes. The values are used in the 
<a href="https://msdn.microsoft.com/cea59e2a-99d8-472d-8e4f-2e2474789c20">ILockBytes::LockRegion</a> and 
<a href="https://msdn.microsoft.com/f2606833-05ed-4bd0-a762-7b8172fb14c8">IStream::LockRegion</a> methods.


## -enum-fields




### -field LOCK_WRITE

If this lock is granted, the specified range of bytes can be opened and read any number of times, but writing to the locked range is prohibited except for the owner that was granted this lock.


### -field LOCK_EXCLUSIVE

If this lock is granted, writing to the specified range of bytes is prohibited except by the owner that was granted this lock.


### -field LOCK_ONLYONCE

If this lock is granted, no other <b>LOCK_ONLYONCE</b> lock can be obtained on the range. Usually this lock type is an alias for some other lock type. Thus, specific implementations can have additional behavior associated with this lock type.

