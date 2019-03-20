---
UID: NF:comsvcs.IObjectControl.Deactivate
title: IObjectControl::Deactivate (comsvcs.h)
author: windows-sdk-content
description: Enables a COM+ object to perform required cleanup before it is recycled or destroyed.
old-location: cos\iobjectcontrol_deactivate.htm
tech.root: cossdk
ms.assetid: e076e7ce-867a-47ab-bd7e-9754b7d81e43
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Deactivate, Deactivate method [COM+], Deactivate method [COM+],IObjectControl interface, IObjectControl interface [COM+],Deactivate method, IObjectControl.Deactivate, IObjectControl::Deactivate, _cos_IObjectControl_Deactivate, comsvcs/IObjectControl::Deactivate, cos.iobjectcontrol_deactivate
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IObjectControl.Deactivate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IObjectControl::Deactivate


## -description


Enables a COM+ object to perform required cleanup before it is recycled or destroyed.

This method is called by the COM+ run-time environment whenever an object is deactivated. Do not make any method calls on objects in the same activity from this method.



## -parameters






## -returns



This method does not return a value.




## -remarks



The COM+ run-time environment calls the <b>Deactivate</b> method whenever an object that supports the <a href="https://msdn.microsoft.com/cbc63f97-dfc7-4e1f-97f9-2043f8bea1d4">IObjectControl</a> interface is deactivated. An object is deactivated when it returns from a method in which the method called <a href="https://msdn.microsoft.com/8ff25b68-fcb3-4e11-9c74-b49b31806796">SetComplete</a> or <a href="https://msdn.microsoft.com/c254305f-1fc5-417e-b93b-d5e2b36e9e39">SetAbort</a>, when the transaction in which it executed is committed or aborted, or when the last client to hold a reference on the object releases its reference.

If the component supports recycling (returns <b>TRUE</b> from the <a href="https://msdn.microsoft.com/97f585f1-e9c2-4122-a5e9-0a10b874b06e">CanBePooled</a> method), you must use the <b>Deactivate</b> method to reset the object's state to the state in which the <a href="https://msdn.microsoft.com/53bf55a2-0cfa-4612-bca7-c6693f84e18f">Activate</a> method expects to find it. You can also use the <b>Deactivate</b> method to release the object's context or to do other context-specific cleanup. Even if an object supports recycling, it can be beneficial to release certain reusable resources in its <b>Deactivate</b> method. For example, ODBC provides its own connection pooling. It is more efficient to pool a database connection in a general connection pool where other objects can use it than it is to keep it tied to a specific object in an object pool.



COM+ expressly forbids calling into an object that exposes <a href="https://msdn.microsoft.com/cbc63f97-dfc7-4e1f-97f9-2043f8bea1d4">IObjectControl</a> after the deactivate method has returned (when it is in its destructor). Such a call would result in an RPC_E_DISCONNECTED error. For example, if an object has passed out a reference to itself and then calls back into the object after <b>Deactivate</b> has returned, a disconnected error results.





## -see-also




<a href="https://msdn.microsoft.com/cbc63f97-dfc7-4e1f-97f9-2043f8bea1d4">IObjectControl</a>
 

 

