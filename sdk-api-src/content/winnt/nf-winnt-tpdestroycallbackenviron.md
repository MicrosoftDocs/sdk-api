---
UID: NF:winnt.TpDestroyCallbackEnviron
title: TpDestroyCallbackEnviron function (winnt.h)
author: windows-sdk-content
description: Deletes the specified callback environment. Call this function when the callback environment is no longer needed for creating new thread pool objects.
old-location: base\tpdestroycallbackenviron.htm
tech.root: ProcThread
ms.assetid: B0925491-73FE-4342-9E66-E5F6344353FB
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TpDestroyCallbackEnviron, TpDestroyCallbackEnviron function, base.tpdestroycallbackenviron, winnt/TpDestroyCallbackEnviron
ms.topic: function
f1_keywords: ["winnt/TpDestroyCallbackEnviron"]
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
 - TpDestroyCallbackEnviron
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TpDestroyCallbackEnviron function


## -description


Deletes the specified callback environment. Call this function when the callback environment is no longer needed for creating new thread pool objects.


## -parameters




### -param CallbackEnviron [in]

A <b>TP_CALLBACK_ENVIRON</b> structure that defines the callback environment. The <a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpinitializecallbackenviron">TpInitializeCallbackEnviron</a> function returns this structure.


## -returns



This function does not return a value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpinitializecallbackenviron">TpInitializeCallbackEnviron</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbackactivationcontext">TpSetCallbackActivationContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbackcleanupgroup">TpSetCallbackCleanupGroup</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbackfinalizationcallback">TpSetCallbackFinalizationCallback</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbacklongfunction">TpSetCallbackLongFunction</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbacknoactivationcontext">TpSetCallbackNoActivationContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbackpersistent">TpSetCallbackPersistent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbackpriority">TpSetCallbackPriority</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbackracewithdll">TpSetCallbackRaceWithDll</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-tpsetcallbackthreadpool">TpSetCallbackThreadpool</a>
 

 

