---
UID: NF:comsvcs.ObjectControl.Deactivate
title: ObjectControl::Deactivate
author: windows-sdk-content
description: Enables a COM+ object to perform cleanup required before it is recycled or destroyed.
old-location: cos\objectcontrol_deactivate.htm
old-project: cossdk
ms.assetid: 86ab7f50-6f2e-4c6c-ba4d-fd302cccf97d
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: Deactivate, Deactivate method [COM+], Deactivate method [COM+],ObjectControl interface, ObjectControl interface [COM+],Deactivate method, ObjectControl.Deactivate, ObjectControl::Deactivate, _cos_ObjectControl_Deactivate, comsvcs/ObjectControl::Deactivate, cos.objectcontrol_deactivate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ObjectControl.Deactivate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ObjectControl::Deactivate


## -description


Enables a COM+ object to perform cleanup required before it is recycled or destroyed.

This method is called by the COM+ run-time environment whenever an object is deactivated. Do not make any method calls on objects in the same activity from this method.


## -parameters






## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



The COM+ run-time environment calls the <b>Deactivate</b> method whenever an object that supports the <a href="https://msdn.microsoft.com/3ca939de-31ce-4ce6-84cd-4b4191a0753c">ObjectControl</a> interface is deactivated. An object is deactivated when it returns from a method in which the method called <a href="https://msdn.microsoft.com/3bf3bbc2-9b4f-4dba-89ef-62c58640710b">SetComplete</a> or <a href="https://msdn.microsoft.com/709c1752-f2fb-463e-a95e-a082cd28b110">SetAbort</a>, when the transaction in which it executed is committed or aborted, or when the last client to hold a reference on the object releases its reference.

If the component supports recycling (returns <b>TRUE</b> from the <a href="https://msdn.microsoft.com/1bca2892-4b9a-4135-b009-37181a028130">CanBePooled</a> method), you must use the <b>Deactivate</b> method to reset the object's state to the state in which the <a href="https://msdn.microsoft.com/70b260e7-a51d-4ddc-b395-5478e368e776">Activate</a> method expects to find it. You can also use the <b>Deactivate</b> method to release the object's context or to do other context-specific cleanup. Even if an object supports recycling, it can be beneficial to release certain reusable resources in its <b>Deactivate</b> method. For example, ODBC provides its own connection pooling. It is more efficient to pool a database connection in a general connection pool where other objects can use it than it is to keep it tied to a specific object in an object pool.

COM+ expressly forbids calling into an object that exposes <a href="https://msdn.microsoft.com/3ca939de-31ce-4ce6-84cd-4b4191a0753c">ObjectControl</a> after the <b>Deactivate</b> method has returned (when it is in its destructor). Such a call would result in an RPC_E_DISCONNECTED error. For example, if an object has passed out a reference to itself and then calls back into the object after <b>Deactivate</b> has returned, a disconnected error results.




## -see-also




<a href="https://msdn.microsoft.com/3ca939de-31ce-4ce6-84cd-4b4191a0753c">ObjectControl</a>
 

 

