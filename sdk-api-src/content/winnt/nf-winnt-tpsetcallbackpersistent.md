---
UID: NF:winnt.TpSetCallbackPersistent
title: TpSetCallbackPersistent function (winnt.h)
description: Specifies that the callback should run on a persistent thread. (TpSetCallbackPersistent)
helpviewer_keywords: ["TpSetCallbackPersistent","TpSetCallbackPersistent function","base.tpsetcallbackpersistent","winnt/TpSetCallbackPersistent"]
old-location: base\tpsetcallbackpersistent.htm
tech.root: backup
ms.assetid: FE2CB959-25BC-4420-A921-2A65016B25CF
ms.date: 12/05/2018
ms.keywords: TpSetCallbackPersistent, TpSetCallbackPersistent function, base.tpsetcallbackpersistent, winnt/TpSetCallbackPersistent
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
 - TpSetCallbackPersistent
 - winnt/TpSetCallbackPersistent
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
 - TpSetCallbackPersistent
---

# TpSetCallbackPersistent function


## -description

Specifies that the callback should run on a persistent thread.

## -parameters

### -param CallbackEnviron [in, out]

A <b>TP_CALLBACK_ENVIRON</b> structure that defines the callback environment. The <a href="/windows/desktop/api/winnt/nf-winnt-tpinitializecallbackenviron">TpInitializeCallbackEnviron</a> function returns this structure.

## -remarks

This function is implemented as an inline function.

## -see-also

<a href="/windows/desktop/api/winnt/nf-winnt-tpdestroycallbackenviron">TpDestroyCallbackEnviron</a>



<a href="/windows/desktop/api/winnt/nf-winnt-tpinitializecallbackenviron">TpInitializeCallbackEnviron</a>



<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbackactivationcontext">TpSetCallbackActivationContext</a>



<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbackcleanupgroup">TpSetCallbackCleanupGroup</a>



<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbackfinalizationcallback">TpSetCallbackFinalizationCallback</a>



<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbacklongfunction">TpSetCallbackLongFunction</a>



<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbacknoactivationcontext">TpSetCallbackNoActivationContext</a>



<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbackpriority">TpSetCallbackPriority</a>



<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbackracewithdll">TpSetCallbackRaceWithDll</a>



<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbackthreadpool">TpSetCallbackThreadpool</a>
