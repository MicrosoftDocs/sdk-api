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

# IContextCallback::ContextCallback


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
 

 

