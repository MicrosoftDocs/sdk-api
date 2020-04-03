---
UID: NF:winnt.TpSetCallbackActivationContext
title: TpSetCallbackActivationContext function (winnt.h)
description: Assigns an activation context to the callback environment.
old-location: base\tpsetcallbackactivationcontext.htm
tech.root: ProcThread
ms.assetid: C4715789-0DF7-436B-881F-4360A7528246
ms.date: 12/05/2018
ms.keywords: TpSetCallbackActivationContext, TpSetCallbackActivationContext function, base.tpsetcallbackactivationcontext, winnt/TpSetCallbackActivationContext
f1_keywords:
- winnt/TpSetCallbackActivationContext
dev_langs:
- c++
req.header: winnt.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- winnt.h
api_name:
- TpSetCallbackActivationContext
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TpSetCallbackActivationContext function


## -description


Assigns an activation context to the callback environment.


## -parameters




### -param CallbackEnviron [in, out]

A <b>TP_CALLBACK_ENVIRON</b> structure that defines the callback environment. The <a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpinitializecallbackenviron">TpInitializeCallbackEnviron</a> function returns this structure.


### -param ActivationContext [in, optional]

Pointer to an <b>_ACTIVATION_CONTEXT</b> structure.


## -remarks



This function is implemented as an inline function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpdestroycallbackenviron">TpDestroyCallbackEnviron</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpinitializecallbackenviron">TpInitializeCallbackEnviron</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbackcleanupgroup">TpSetCallbackCleanupGroup</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbackfinalizationcallback">TpSetCallbackFinalizationCallback</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbacklongfunction">TpSetCallbackLongFunction</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbacknoactivationcontext">TpSetCallbackNoActivationContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbackpersistent">TpSetCallbackPersistent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbackpriority">TpSetCallbackPriority</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbackracewithdll">TpSetCallbackRaceWithDll</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbackthreadpool">TpSetCallbackThreadpool</a>
 

 

