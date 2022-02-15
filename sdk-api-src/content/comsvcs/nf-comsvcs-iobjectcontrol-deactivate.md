---
UID: NF:comsvcs.IObjectControl.Deactivate
title: IObjectControl::Deactivate (comsvcs.h)
description: Enables a COM+ object to perform required cleanup before it is recycled or destroyed.
helpviewer_keywords: ["Deactivate","Deactivate method [COM+]","Deactivate method [COM+]","IObjectControl interface","IObjectControl interface [COM+]","Deactivate method","IObjectControl.Deactivate","IObjectControl::Deactivate","_cos_IObjectControl_Deactivate","comsvcs/IObjectControl::Deactivate","cos.iobjectcontrol_deactivate"]
old-location: cos\iobjectcontrol_deactivate.htm
tech.root: cos
ms.assetid: e076e7ce-867a-47ab-bd7e-9754b7d81e43
ms.date: 12/05/2018
ms.keywords: Deactivate, Deactivate method [COM+], Deactivate method [COM+],IObjectControl interface, IObjectControl interface [COM+],Deactivate method, IObjectControl.Deactivate, IObjectControl::Deactivate, _cos_IObjectControl_Deactivate, comsvcs/IObjectControl::Deactivate, cos.iobjectcontrol_deactivate
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IObjectControl::Deactivate
 - comsvcs/IObjectControl::Deactivate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IObjectControl.Deactivate
---

# IObjectControl::Deactivate


## -description

Enables a COM+ object to perform required cleanup before it is recycled or destroyed.

This method is called by the COM+ run-time environment whenever an object is deactivated. Do not make any method calls on objects in the same activity from this method.



## -remarks

The COM+ run-time environment calls the <b>Deactivate</b> method whenever an object that supports the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontrol">IObjectControl</a> interface is deactivated. An object is deactivated when it returns from a method in which the method called <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-setcomplete">SetComplete</a> or <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-setabort">SetAbort</a>, when the transaction in which it executed is committed or aborted, or when the last client to hold a reference on the object releases its reference.

If the component supports recycling (returns <b>TRUE</b> from the <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontrol-canbepooled">CanBePooled</a> method), you must use the <b>Deactivate</b> method to reset the object's state to the state in which the <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontrol-activate">Activate</a> method expects to find it. You can also use the <b>Deactivate</b> method to release the object's context or to do other context-specific cleanup. Even if an object supports recycling, it can be beneficial to release certain reusable resources in its <b>Deactivate</b> method. For example, ODBC provides its own connection pooling. It is more efficient to pool a database connection in a general connection pool where other objects can use it than it is to keep it tied to a specific object in an object pool.



COM+ expressly forbids calling into an object that exposes <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontrol">IObjectControl</a> after the deactivate method has returned (when it is in its destructor). Such a call would result in an RPC_E_DISCONNECTED error. For example, if an object has passed out a reference to itself and then calls back into the object after <b>Deactivate</b> has returned, a disconnected error results.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontrol">IObjectControl</a>
