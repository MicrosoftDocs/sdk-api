---
UID: NF:winnt.TpSetCallbackLongFunction
title: TpSetCallbackLongFunction function (winnt.h)

description: Indicates that callbacks associated with this callback environment may not return quickly.
old-location: base\tpsetcallbacklongfunction.htm
tech.root: ProcThread
ms.assetid: 27E7F647-1005-4499-9787-F2CE6E8B6AFF

ms.date: 12/05/2018
ms.keywords: TpSetCallbackLongFunction, TpSetCallbackLongFunction function, base.tpsetcallbacklongfunction, winnt/TpSetCallbackLongFunction
ms.topic: function
f1_keywords: 
 - "winnt/TpSetCallbackLongFunction"
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
 - TpSetCallbackLongFunction
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TpSetCallbackLongFunction function


## -description


Indicates that callbacks associated with this callback environment may not return quickly.


## -parameters




### -param CallbackEnviron [in, out]

A <b>TP_CALLBACK_ENVIRON</b> structure that defines the callback environment. The <a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpinitializecallbackenviron">TpInitializeCallbackEnviron</a> function returns this structure.


## -returns



This function does not return a value.




## -remarks



The thread pool may use this information to better determine when a new thread should be created.

This function is implemented as an inline function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpdestroycallbackenviron">TpDestroyCallbackEnviron</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpinitializecallbackenviron">TpInitializeCallbackEnviron</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbackactivationcontext">TpSetCallbackActivationContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbackcleanupgroup">TpSetCallbackCleanupGroup</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbackfinalizationcallback">TpSetCallbackFinalizationCallback</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbacknoactivationcontext">TpSetCallbackNoActivationContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbackpersistent">TpSetCallbackPersistent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbackpriority">TpSetCallbackPriority</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbackracewithdll">TpSetCallbackRaceWithDll</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbackthreadpool">TpSetCallbackThreadpool</a>
 

 

