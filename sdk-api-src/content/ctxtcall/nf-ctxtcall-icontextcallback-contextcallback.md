---
UID: NF:ctxtcall.IContextCallback.ContextCallback
title: IContextCallback::ContextCallback method
author: windows-driver-content
description: Enters the object context, executes the specified function, and returns.
old-location: com\icontextcallback_contextcallback.htm
old-project: com
ms.assetid: 7446792e-7f29-4ad4-8245-b86f63f2df18
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: ContextCallback method [COM], ContextCallback method [COM], IContextCallback interface, ContextCallback,IContextCallback.ContextCallback, IContextCallback, IContextCallback interface [COM], ContextCallback method, IContextCallback::ContextCallback, _com_icontextcallback_contextcallback, com.icontextcallback_contextcallback, ctxtcall/IContextCallback::ContextCallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ctxtcall.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctxtcall.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TF_LBBALLOONINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Ctxtcall.h
api_name:
-	IContextCallback.ContextCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IContextCallback::ContextCallback method


## -description


Enters the object context, executes the specified function, and returns.


## -parameters




### -param pfnCallback [in]

The function to be called inside the object context.


### -param pParam [in]

The data to be passed to the function when it is called in the context.


### -param riid [in]

The IID of the call that is being simulated. See Remarks for more information.


### -param iMethod [in]

The method number of the call that is being simulated. See Remarks for more information.


### -param pUnk [in]

This parameter is reserved and must be <b>NULL</b>.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and E_FAIL. If none of these failures occur, the return value of this function is the <b>HRESULT</b> value returned by the <i>pfnCallback</i> function.




## -remarks



This method simulates a method call on an object inside the context. It is intended for low-level operations, such as cleanup/lazy marshaling, that respect the application's reentrancy expectations. 

To give the infrastructure information, an interface and method number must be specified. The parameter <i>riid</i> must not be IID_IUnknown, and the method number must not be less than 3.

If <i>riid</i> is set to IID_IEnterActivityWithNoLock, the function is executed without an activity lock.

If <i>riid</i> is set to IID_ICallbackWithNoReentrancyToApplicationSTA, the function does not reenter an ASTA arbitrarily. Most apps should set <i>riid</i> to this values for general purpose use.




## -see-also




<a href="https://msdn.microsoft.com/47af7b80-3419-4a40-8932-a5a27f297dc9">IContextCallback</a>
 

 

