---
UID: NF:comsvcs.ObjectControl.Activate
title: ObjectControl::Activate
author: windows-sdk-content
description: Enables a COM+ object to perform context-specific initialization whenever it is activated.
old-location: cos\objectcontrol_activate.htm
old-project: cossdk
ms.assetid: 70b260e7-a51d-4ddc-b395-5478e368e776
ms.author: windowssdkdev
ms.date: 06/18/2018
ms.keywords: Activate, Activate method [COM+], Activate method [COM+],ObjectControl interface, ObjectControl interface [COM+],Activate method, ObjectControl.Activate, ObjectControl::Activate, _cos_ObjectControl_Activate, comsvcs/ObjectControl::Activate, cos.objectcontrol_activate
ms.prod: windows
ms.technology: windows-sdk
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
 - ObjectControl.Activate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ObjectControl::Activate


## -description


Enables a COM+ object to perform context-specific initialization whenever it is activated.

This method is called by the COM+ run-time environment before any other methods are called on the object.



## -parameters






## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



Whenever a client calls a COM+ object that isn't already active, the COM+ run-time environment automatically activates the object. This is called <a href="https://msdn.microsoft.com/47b23cae-d5fc-4788-ab1c-93d6d8ee3f01">Just-in-Time Activation</a>. For components that support <a href="https://msdn.microsoft.com/3ca939de-31ce-4ce6-84cd-4b4191a0753c">ObjectControl</a> as an interface, COM+ invokes the object's <b>Activate</b> method before passing the client's method call on to the object.

Any context-specific initialization procedures should be implemented in the <b>Activate</b> method for objects that expose <a href="https://msdn.microsoft.com/3ca939de-31ce-4ce6-84cd-4b4191a0753c">ObjectControl</a>.

For example, you can use the <b>Activate</b> method to obtain a reference to an object's context and store it in a member variable. Then the object context is available to any method that requires it, and you do not have to acquire a new one every time you want to use it. After you have a reference to the object's context, you can use the <a href="https://msdn.microsoft.com/09a17e57-7224-43bc-93c7-16ab95ca2517">ObjectContext</a> methods to check whether security is enabled, whether the object is executing in a transaction, or whether the caller is in a particular role.

If you are enabling object recycling (by implementing the <a href="https://msdn.microsoft.com/1bca2892-4b9a-4135-b009-37181a028130">CanBePooled</a> method to query the object), the <b>Activate</b> method must be able to handle newly created objects as well as recycled objects. When the <b>Activate</b> method returns, there should be no distinguishable difference between a new object and a recycled one.

COM+ expressly forbids calling into an object that exposes <a href="https://msdn.microsoft.com/3ca939de-31ce-4ce6-84cd-4b4191a0753c">ObjectControl</a> before calling the <b>Activate</b> method (when it is in its constructor). Such a call would result in an RPC_E_DISCONNECTED error. For example, if an object passes out a reference to itself while in its constructor and then the reference calls back into that object prior to the call to <b>Activate</b>, the disconnected error is returned.




## -see-also




<a href="https://msdn.microsoft.com/3ca939de-31ce-4ce6-84cd-4b4191a0753c">ObjectControl</a>
 

 

