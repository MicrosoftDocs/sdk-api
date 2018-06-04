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

# IClassFactory::LockServer


## -description


Locks an object application open in memory. This enables instances to be created more quickly.


## -parameters




### -param fLock [in]

If <b>TRUE</b>, increments the lock count; if <b>FALSE</b>, decrements the lock count.


## -returns



This method can return the standard return values E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



<b>IClassFactory::LockServer</b> controls whether an object's server is kept in memory. Keeping the application alive in memory allows instances to be created more quickly.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Most clients do not need to call this method. It is provided only for those clients that require special performance in creating multiple instances of their objects.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If the lock count is zero, there are no more objects in use, and the application is not under user control, the server can be closed. One way to implement <b>LockServer</b> is to call the <a href="https://msdn.microsoft.com/36eb55f1-06de-49ad-8a8d-91693ca92e99">CoLockObjectExternal</a> function.

The process that locks the object application is responsible for unlocking it. After the class object is released, there is no mechanism that guarantees the caller connection to the same class later (as in the case where a class object is registered as single-use). It is important to count all calls, not just the last one, to <b>LockServer</b>, because calls must be balanced before attempting to release the pointer to the <a href="https://msdn.microsoft.com/f624f833-2b69-43bc-92cd-c4ecbe6051c5">IClassFactory</a> interface on the class object or an error results. For every call to <b>LockServer</b> with <i>fLock</i> set to <b>TRUE</b>, there must be a call to <b>LockServer</b> with <i>fLock</i> set to <b>FALSE</b>. When the lock count and the class object reference count are both zero, the class object can be freed.




## -see-also




<a href="https://msdn.microsoft.com/36eb55f1-06de-49ad-8a8d-91693ca92e99">CoLockObjectExternal</a>



<a href="https://msdn.microsoft.com/f624f833-2b69-43bc-92cd-c4ecbe6051c5">IClassFactory</a>
 

 

