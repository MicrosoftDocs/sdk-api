---
UID: NF:winnt.TpSetCallbackPersistent
title: TpSetCallbackPersistent function (winnt.h)

description: Specifies that the callback should run on a persistent thread.
old-location: base\tpsetcallbackpersistent.htm
tech.root: ProcThread
ms.assetid: FE2CB959-25BC-4420-A921-2A65016B25CF

ms.date: 12/05/2018
ms.keywords: TpSetCallbackPersistent, TpSetCallbackPersistent function, base.tpsetcallbackpersistent, winnt/TpSetCallbackPersistent
ms.topic: function
f1_keywords: 
 - "winnt/TpSetCallbackPersistent"
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
 - TpSetCallbackPersistent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TpSetCallbackPersistent function


## -description


Specifies that the callback should run on a persistent thread.


## -parameters




### -param CallbackEnviron [in, out]

A <b>TP_CALLBACK_ENVIRON</b> structure that defines the callback environment. The <a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpinitializecallbackenviron">TpInitializeCallbackEnviron</a> function returns this structure.


## -returns



This function does not return a value.




## -remarks



This function is implemented as an inline function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpdestroycallbackenviron">TpDestroyCallbackEnviron</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpinitializecallbackenviron">TpInitializeCallbackEnviron</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbackactivationcontext">TpSetCallbackActivationContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbackcleanupgroup">TpSetCallbackCleanupGroup</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbackfinalizationcallback">TpSetCallbackFinalizationCallback</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbacklongfunction">TpSetCallbackLongFunction</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbacknoactivationcontext">TpSetCallbackNoActivationContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbackpriority">TpSetCallbackPriority</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbackracewithdll">TpSetCallbackRaceWithDll</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbackthreadpool">TpSetCallbackThreadpool</a>
 

 

