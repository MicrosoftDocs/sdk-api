---
UID: NF:winnt.TpSetCallbackThreadpool
title: TpSetCallbackThreadpool function (winnt.h)
author: windows-sdk-content
description: Assigns a thread pool to a callback environment.
old-location: base\tpsetcallbackthreadpool.htm
tech.root: ProcThread
ms.assetid: A1BED20A-9DB5-4B5A-B1AD-60454176AB1D
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TpSetCallbackThreadpool, TpSetCallbackThreadpool function, base.tpsetcallbackthreadpool, winnt/TpSetCallbackThreadpool
ms.topic: function
f1_keywords: 
 - "winnt/TpSetCallbackThreadpool"
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
 - TpSetCallbackThreadpool
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TpSetCallbackThreadpool function


## -description


Assigns a thread pool to a callback environment.


## -parameters




### -param CallbackEnviron [in, out]

A <b>TP_CALLBACK_ENVIRON</b> structure that defines the callback environment. The <a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpinitializecallbackenviron">TpInitializeCallbackEnviron</a> function returns this structure.


### -param Pool [in]

A <b>TP_POOL</b> structure that defines a thread pool. The <a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpool">CreateThreadpool</a> function returns this structure.


## -returns



This function does not return a value.




## -remarks



If you do not specify a thread pool, the global thread pool is used.

This function is implemented as an inline function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpdestroycallbackenviron">TpDestroyCallbackEnviron</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpinitializecallbackenviron">TpInitializeCallbackEnviron</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbackactivationcontext">TpSetCallbackActivationContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbackcleanupgroup">TpSetCallbackCleanupGroup</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbackfinalizationcallback">TpSetCallbackFinalizationCallback</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbacklongfunction">TpSetCallbackLongFunction</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbacknoactivationcontext">TpSetCallbackNoActivationContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbackpersistent">TpSetCallbackPersistent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbackpriority">TpSetCallbackPriority</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbackracewithdll">TpSetCallbackRaceWithDll</a>
 

 

