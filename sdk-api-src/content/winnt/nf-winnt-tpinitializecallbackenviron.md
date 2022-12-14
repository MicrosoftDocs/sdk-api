---
UID: NF:winnt.TpInitializeCallbackEnviron
title: TpInitializeCallbackEnviron function (winnt.h)
description: Initializes a callback environment for the thread pool.
helpviewer_keywords: ["TpInitializeCallbackEnviron","TpInitializeCallbackEnviron function","base.tpinitializecallbackenviron","winnt/TpInitializeCallbackEnviron"]
old-location: base\tpinitializecallbackenviron.htm
tech.root: backup
ms.assetid: 4602CB19-D8C0-460E-A853-8DDECE643A76
ms.date: 12/05/2018
ms.keywords: TpInitializeCallbackEnviron, TpInitializeCallbackEnviron function, base.tpinitializecallbackenviron, winnt/TpInitializeCallbackEnviron
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
 - TpInitializeCallbackEnviron
 - winnt/TpInitializeCallbackEnviron
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
 - TpInitializeCallbackEnviron
---

# TpInitializeCallbackEnviron function


## -description

Initializes a callback environment for the thread pool.

## -parameters

### -param CallbackEnviron [out]

A <b>TP_CALLBACK_ENVIRON</b> structure that defines the callback environment. Allocate space for this structure and initialize it using this function.

## -remarks

The thread pool callback environment is subject to default behaviors that can be changed. For example, callbacks execute in the global pool by default, but a different thread pool can be specified using <a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbackthreadpool">TpSetCallbackThreadpool</a>. Thread pool callback environment behavior can be changed with the following functions:

<ul>
<li>
<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbackactivationcontext">TpSetCallbackActivationContext</a>
</li>
<li>
<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbackcleanupgroup">TpSetCallbackCleanupGroup</a>
</li>
<li>
<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbackfinalizationcallback">TpSetCallbackFinalizationCallback</a>
</li>
<li>
<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbacklongfunction">TpSetCallbackLongFunction</a>
</li>
<li>
<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbacknoactivationcontext">TpSetCallbackNoActivationContext</a>
</li>
<li>
<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbackpersistent">TpSetCallbackPersistent</a>
</li>
<li>
<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbackpriority">TpSetCallbackPriority</a>
</li>
<li>
<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbackracewithdll">TpSetCallbackRaceWithDll</a>
</li>
<li>
<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbackthreadpool">TpSetCallbackThreadpool</a>
</li>
</ul>
Call
<b>TpInitializeCallbackEnviron</b> to create a callback environment that can be modified. Call <a href="/windows/desktop/api/winnt/nf-winnt-tpdestroycallbackenviron">TpDestroyCallbackEnviron</a> to destroy the callback environment.

This function is implemented as an inline function.