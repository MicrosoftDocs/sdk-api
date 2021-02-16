---
UID: NF:ctxtcall.IContextCallback.ContextCallback
title: IContextCallback::ContextCallback (ctxtcall.h)
description: Enters the object context, executes the specified function, and returns.
helpviewer_keywords: ["ContextCallback","ContextCallback method [COM]","ContextCallback method [COM]","IContextCallback interface","IContextCallback interface [COM]","ContextCallback method","IContextCallback.ContextCallback","IContextCallback::ContextCallback","_com_icontextcallback_contextcallback","com.icontextcallback_contextcallback","ctxtcall/IContextCallback::ContextCallback"]
old-location: com\icontextcallback_contextcallback.htm
tech.root: com
ms.assetid: 7446792e-7f29-4ad4-8245-b86f63f2df18
ms.date: 12/05/2018
ms.keywords: ContextCallback, ContextCallback method [COM], ContextCallback method [COM],IContextCallback interface, IContextCallback interface [COM],ContextCallback method, IContextCallback.ContextCallback, IContextCallback::ContextCallback, _com_icontextcallback_contextcallback, com.icontextcallback_contextcallback, ctxtcall/IContextCallback::ContextCallback
req.header: ctxtcall.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctxtcall.idl
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
 - IContextCallback::ContextCallback
 - ctxtcall/IContextCallback::ContextCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ctxtcall.h
api_name:
 - IContextCallback.ContextCallback
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

<a href="/windows/desktop/api/ctxtcall/nn-ctxtcall-icontextcallback">IContextCallback</a>