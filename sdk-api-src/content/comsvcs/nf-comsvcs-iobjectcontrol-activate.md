---
UID: NF:comsvcs.IObjectControl.Activate
title: IObjectControl::Activate (comsvcs.h)
description: Enables a COM+ object to perform context-specific initialization whenever it is activated. (IObjectControl.Activate)
helpviewer_keywords: ["Activate","Activate method [COM+]","Activate method [COM+]","IObjectControl interface","IObjectControl interface [COM+]","Activate method","IObjectControl.Activate","IObjectControl::Activate","_cos_IObjectControl_Activate","comsvcs/IObjectControl::Activate","cos.iobjectcontrol_activate"]
old-location: cos\iobjectcontrol_activate.htm
tech.root: cos
ms.assetid: 53bf55a2-0cfa-4612-bca7-c6693f84e18f
ms.date: 12/05/2018
ms.keywords: Activate, Activate method [COM+], Activate method [COM+],IObjectControl interface, IObjectControl interface [COM+],Activate method, IObjectControl.Activate, IObjectControl::Activate, _cos_IObjectControl_Activate, comsvcs/IObjectControl::Activate, cos.iobjectcontrol_activate
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
 - IObjectControl::Activate
 - comsvcs/IObjectControl::Activate
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
 - IObjectControl.Activate
---

# IObjectControl::Activate


## -description

Enables a COM+ object to perform context-specific initialization whenever it is activated. This method is called by the COM+ run-time environment before any other methods are called on the object.



## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

Whenever a client calls a COM+ object that isn't already active, the COM+ run-time environment automatically activates the object. This is called <a href="/windows/desktop/cossdk/com--just-in-time-activation">Just-in-Time Activation</a>. For components that support <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontrol">IObjectControl</a> as an interface, COM+ invokes the object's <b>Activate</b> method before passing the client's method call on to the object.

Any context-specific initialization procedures should be implemented in the <b>Activate</b> method for objects that expose <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontrol">IObjectControl</a>.

For example, you can use the <b>Activate</b> method to obtain a reference to an object's context and store it in a member variable. Then the object context is available to any method that requires it, and you do not have to acquire a new one every time you want to use it. After you have a reference to the object's context, you can use the <b>IObjectControl</b> methods to check whether security is enabled, whether the object is executing in a transaction, or whether the caller is in a particular role.

If you are enabling object recycling (by implementing the <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontrol-canbepooled">CanBePooled</a> method to query the object), the <b>Activate</b> method must be able to handle both newly created and recycled objects. When the <b>Activate</b> method returns, there should be no distinguishable difference between a new object and a recycled one.

COM+ expressly forbids calling into an object that exposes <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontrol">IObjectControl</a> before calling the <b>Activate</b> method (when it is in its constructor). Such a call would result in an RPC_E_DISCONNECTED error. For example, if an object passes out a reference to itself while in its constructor and then the reference calls back into that object prior to the call to <b>Activate</b>, the disconnected error is returned.



You can also use the <b>Activate</b> method to obtain a reference to the object's <a href="/windows/desktop/api/comsvcs/nn-comsvcs-isecurityproperty">ISecurityProperty</a> interface and check the security ID of the object's creator before any methods are called.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontrol">IObjectControl</a>
