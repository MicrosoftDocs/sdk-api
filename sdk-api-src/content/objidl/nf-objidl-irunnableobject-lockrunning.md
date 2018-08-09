---
UID: NF:objidl.IRunnableObject.LockRunning
title: IRunnableObject::LockRunning
author: windows-sdk-content
description: Locks an already running object into its running state or unlocks it from its running state.
old-location: com\irunnableobject_lockrunning.htm
old-project: com
ms.assetid: ce501785-16ad-4120-abea-41e2d6ca67df
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IRunnableObject interface [COM],LockRunning method, IRunnableObject.LockRunning, IRunnableObject::LockRunning, LockRunning, LockRunning method [COM], LockRunning method [COM],IRunnableObject interface, _com_irunnableobject_lockrunning, com.irunnableobject_lockrunning, objidl/IRunnableObject::LockRunning
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IRunnableObject.LockRunning
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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
 

 

