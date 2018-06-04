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

# IRunnableObject::LockRunning


## -description


Locks an already running object into its running state or unlocks it from its running state.


## -parameters




### -param fLock [in]

<b>TRUE</b> locks the object into its running state. <b>FALSE</b> unlocks the object from its running state.


### -param fLastUnlockCloses [in]

<b>TRUE</b> specifies that if the connection being released is the last external lock on the object, the object should close. <b>FALSE</b> specifies that the object should remain open until closed by the user or another process.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



Most implementations of <b>IRunnableObject::LockRunning</b> call <a href="https://msdn.microsoft.com/36eb55f1-06de-49ad-8a8d-91693ca92e99">CoLockObjectExternal</a>.


<a href="https://msdn.microsoft.com/84941a59-6880-4824-b4b9-cd1b52d2bffb">OleLockRunning</a> is a helper function that conveniently repackages the functionality offered by <b>IRunnableObject::LockRunning</b>. With the release of OLE 2.01, the implementation of <b>OleLockRunning</b> was changed to call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a>, ask for <a href="https://msdn.microsoft.com/c682447b-5b12-41d5-a81d-fe94a117f740">IRunnableObject</a>, and then call <b>IRunnableObject::LockRunning</b>. In other words, you can use the interface and the helper function interchangeably.




## -see-also




<a href="https://msdn.microsoft.com/36eb55f1-06de-49ad-8a8d-91693ca92e99">CoLockObjectExternal</a>



<a href="https://msdn.microsoft.com/c682447b-5b12-41d5-a81d-fe94a117f740">IRunnableObject</a>



<a href="https://msdn.microsoft.com/84941a59-6880-4824-b4b9-cd1b52d2bffb">OleLockRunning</a>
 

 

