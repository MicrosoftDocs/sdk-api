---
UID: NF:objidl.IRunnableObject.Run
title: IRunnableObject::Run
author: windows-driver-content
description: Forces an object to run.
old-location: com\irunnableobject_run.htm
old-project: com
ms.assetid: fb79e81c-0655-48ea-afb5-dab3529676d0
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IRunnableObject interface [COM],Run method, IRunnableObject.Run, IRunnableObject::Run, Run, Run method [COM], Run method [COM],IRunnableObject interface, _com_irunnableobject_run, com.irunnableobject_run, objidl/IRunnableObject::Run
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ObjIdl.h
api_name:
-	IRunnableObject.Run
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IRunnableObject::Run


## -description


Forces an object to run.


## -parameters




### -param pbc [in]

A pointer to the binding context of the run operation. See <a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>. This parameter can be <b>NULL</b>.


## -returns



This method can return the standard return values E_INVALIDARG, E_UNEXPECTED, and S_OK.




## -remarks



Containers call <b>IRunnableObject::Run</b> to force their objects to enter the running state. If the object is not already running, calling <b>Run</b> can be an expensive operation, on the order of many seconds. If the object is already running, then this method has no effect on the object.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
When called on a linked object that has been converted to a new class since the link was last activated, <b>IRunnableObject::Run</b> may return OLE_E_CLASSDIFF. In this case, the client should call <a href="https://msdn.microsoft.com/1fadd27d-cb2c-47fc-891a-16f82bdac0f6">IOleLink::BindToSource</a>.


<a href="https://msdn.microsoft.com/9035f996-b163-4855-aa9d-184b77072ead">OleRun</a> is a helper function that conveniently repackages the functionality offered by <b>IRunnableObject::Run</b>. With the release of OLE 2.01, the implementation of <b>OleRun</b> was changed so that it calls <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a>, asks for <a href="https://msdn.microsoft.com/c682447b-5b12-41d5-a81d-fe94a117f740">IRunnableObject</a>, and then calls <b>IRunnableObject::Run</b>. In other words, you can use the interface and the helper function interchangeably.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
The object should register in the running object table if it has a moniker assigned. The object should not hold any strong locks on itself; instead, it should remain in the unstable, unlocked state. The object should be locked when the first external connection is made to the object.

An embedded object must hold a lock on its embedding container while it is in the running state. The default handler provided by OLE 2 takes care of locking the embedding container on behalf of objects implemented by an EXE object application. Objects implemented by a DLL object application must explicitly put a lock on their embedding containers, which they do by first calling <a href="https://msdn.microsoft.com/8f0caf07-f059-4e0c-9c28-c7ad0cc149e3">IOleClientSite::GetContainer</a> to get a pointer to the container, then calling <a href="https://msdn.microsoft.com/31b9961a-29a2-48bf-9d39-d86718983682">IOleContainer::LockContainer</a> to actually place the lock. This lock must be released when <a href="https://msdn.microsoft.com/61ecd153-ed6b-4a2c-a862-54742c5769ee">IOleObject::Close</a> is called.




## -see-also




<a href="https://msdn.microsoft.com/c682447b-5b12-41d5-a81d-fe94a117f740">IRunnableObject</a>



<a href="https://msdn.microsoft.com/9035f996-b163-4855-aa9d-184b77072ead">OleRun</a>
 

 

