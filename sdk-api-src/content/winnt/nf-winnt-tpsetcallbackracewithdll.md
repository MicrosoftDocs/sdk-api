---
UID: NF:winnt.TpSetCallbackRaceWithDll
title: TpSetCallbackRaceWithDll function (winnt.h)
description: Ensures that the specified DLL remains loaded as long as there are outstanding callbacks. (TpSetCallbackRaceWithDll)
helpviewer_keywords: ["TpSetCallbackRaceWithDll","TpSetCallbackRaceWithDll function","base.tpsetcallbackracewithdll","winnt/TpSetCallbackRaceWithDll"]
old-location: base\tpsetcallbackracewithdll.htm
tech.root: backup
ms.assetid: 14519064-450C-409E-AA2D-B4EF4D43C180
ms.date: 12/05/2018
ms.keywords: TpSetCallbackRaceWithDll, TpSetCallbackRaceWithDll function, base.tpsetcallbackracewithdll, winnt/TpSetCallbackRaceWithDll
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TpSetCallbackRaceWithDll
 - winnt/TpSetCallbackRaceWithDll
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winnt.h
api_name:
 - TpSetCallbackRaceWithDll
---

# TpSetCallbackRaceWithDll function


## -description

Ensures that the specified DLL remains loaded as long as there are outstanding callbacks.

## -parameters

### -param CallbackEnviron [in, out]

A <b>TP_CALLBACK_ENVIRON</b> structure that defines the callback environment. The <a href="/windows/desktop/api/winbase/nf-winbase-initializethreadpoolenvironment">InitializeThreadpoolEnvironment</a> function returns this structure.

### -param DllHandle [in]

A handle to the DLL.

## -remarks

You should call this function if a callback might acquire the loader lock. This prevents a deadlock from occurring when one thread in DllMain is waiting for the callback to end, and another thread that is executing the callback attempts to acquire the loader lock.

If the DLL containing the callback might be unloaded, the cleanup code in DllMain must cancel outstanding callbacks before releasing the object.

Managing callbacks created with a TP_CALLBACK_ENVIRON that specifies a callback library is somewhat processing-intensive.  You should consider other options for ensuring that the library is not unloaded while callbacks are executing, or to guarantee that callbacks which may be executing do not acquire the loader lock.

This function is implemented as an inline function.

## -see-also

<a href="/windows/desktop/api/winnt/nf-winnt-tpdestroycallbackenviron">TpDestroyCallbackEnviron</a>



<a href="/windows/desktop/api/winnt/nf-winnt-tpinitializecallbackenviron">TpInitializeCallbackEnviron</a>



<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbackactivationcontext">TpSetCallbackActivationContext</a>



<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbackcleanupgroup">TpSetCallbackCleanupGroup</a>



<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbackfinalizationcallback">TpSetCallbackFinalizationCallback</a>



<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbacklongfunction">TpSetCallbackLongFunction</a>



<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbacknoactivationcontext">TpSetCallbackNoActivationContext</a>



<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbackpersistent">TpSetCallbackPersistent</a>



<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbackpriority">TpSetCallbackPriority</a>



<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbackthreadpool">TpSetCallbackThreadpool</a>
