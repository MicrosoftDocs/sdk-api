---
UID: NF:comsvcs.ObjectControl.Activate
title: ObjectControl::Activate (comsvcs.h)
description: Enables a COM+ object to perform context-specific initialization whenever it is activated. (ObjectControl.Activate)
helpviewer_keywords: ["Activate","Activate method [COM+]","Activate method [COM+]","ObjectControl interface","ObjectControl interface [COM+]","Activate method","ObjectControl.Activate","ObjectControl::Activate","_cos_ObjectControl_Activate","comsvcs/ObjectControl::Activate","cos.objectcontrol_activate"]
old-location: cos\objectcontrol_activate.htm
tech.root: cos
ms.assetid: 70b260e7-a51d-4ddc-b395-5478e368e776
ms.date: 12/05/2018
ms.keywords: Activate, Activate method [COM+], Activate method [COM+],ObjectControl interface, ObjectControl interface [COM+],Activate method, ObjectControl.Activate, ObjectControl::Activate, _cos_ObjectControl_Activate, comsvcs/ObjectControl::Activate, cos.objectcontrol_activate
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
 - ObjectControl::Activate
 - comsvcs/ObjectControl::Activate
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
 - ObjectControl.Activate
---

# ObjectControl::Activate


## -description

Enables a COM+ object to perform context-specific initialization whenever it is activated.

This method is called by the COM+ run-time environment before any other methods are called on the object.



## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

Whenever a client calls a COM+ object that isn't already active, the COM+ run-time environment automatically activates the object. This is called <a href="/windows/desktop/cossdk/com--just-in-time-activation">Just-in-Time Activation</a>. For components that support <a href="/windows/desktop/api/comsvcs/nn-comsvcs-objectcontrol">ObjectControl</a> as an interface, COM+ invokes the object's <b>Activate</b> method before passing the client's method call on to the object.

Any context-specific initialization procedures should be implemented in the <b>Activate</b> method for objects that expose <a href="/windows/desktop/api/comsvcs/nn-comsvcs-objectcontrol">ObjectControl</a>.

For example, you can use the <b>Activate</b> method to obtain a reference to an object's context and store it in a member variable. Then the object context is available to any method that requires it, and you do not have to acquire a new one every time you want to use it. After you have a reference to the object's context, you can use the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-objectcontext">ObjectContext</a> methods to check whether security is enabled, whether the object is executing in a transaction, or whether the caller is in a particular role.

If you are enabling object recycling (by implementing the <a href="/windows/desktop/api/comsvcs/nf-comsvcs-objectcontrol-canbepooled">CanBePooled</a> method to query the object), the <b>Activate</b> method must be able to handle newly created objects as well as recycled objects. When the <b>Activate</b> method returns, there should be no distinguishable difference between a new object and a recycled one.

COM+ expressly forbids calling into an object that exposes <a href="/windows/desktop/api/comsvcs/nn-comsvcs-objectcontrol">ObjectControl</a> before calling the <b>Activate</b> method (when it is in its constructor). Such a call would result in an RPC_E_DISCONNECTED error. For example, if an object passes out a reference to itself while in its constructor and then the reference calls back into that object prior to the call to <b>Activate</b>, the disconnected error is returned.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-objectcontrol">ObjectControl</a>
