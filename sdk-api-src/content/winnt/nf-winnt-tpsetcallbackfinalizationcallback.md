---
UID: NF:winnt.TpSetCallbackFinalizationCallback
title: TpSetCallbackFinalizationCallback function (winnt.h)
description: Indicates a function to call when the callback environment is finalized.
helpviewer_keywords: ["TpSetCallbackFinalizationCallback","TpSetCallbackFinalizationCallback function","base.tpsetcallbackfinalizationcallback","winnt/TpSetCallbackFinalizationCallback"]
old-location: base\tpsetcallbackfinalizationcallback.htm
tech.root: backup
ms.assetid: 425898A7-5E98-490A-912A-A409D1E2DFDE
ms.date: 12/05/2018
ms.keywords: TpSetCallbackFinalizationCallback, TpSetCallbackFinalizationCallback function, base.tpsetcallbackfinalizationcallback, winnt/TpSetCallbackFinalizationCallback
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
 - TpSetCallbackFinalizationCallback
 - winnt/TpSetCallbackFinalizationCallback
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
 - TpSetCallbackFinalizationCallback
---

# TpSetCallbackFinalizationCallback function


## -description

Indicates a function to call when the callback environment is finalized.

## -parameters

### -param CallbackEnviron [in, out]

A <b>TP_CALLBACK_ENVIRON</b> structure that defines the callback environment. The <a href="/windows/desktop/api/winnt/nf-winnt-tpinitializecallbackenviron">TpInitializeCallbackEnviron</a> function returns this structure.

### -param FinalizationCallback [in]

Pointer to a <b>TP_SIMPLE_CALLBACK</b> structure indicating a function to call when the callback environment is finalized.

## -remarks

This function is implemented as an inline function.

## -see-also

<a href="/windows/desktop/api/winnt/nf-winnt-tpdestroycallbackenviron">TpDestroyCallbackEnviron</a>



<a href="/windows/desktop/api/winnt/nf-winnt-tpinitializecallbackenviron">TpInitializeCallbackEnviron</a>



<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbackactivationcontext">TpSetCallbackActivationContext</a>



<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbackcleanupgroup">TpSetCallbackCleanupGroup</a>



<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbacklongfunction">TpSetCallbackLongFunction</a>



<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbacknoactivationcontext">TpSetCallbackNoActivationContext</a>



<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbackpersistent">TpSetCallbackPersistent</a>



<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbackpriority">TpSetCallbackPriority</a>



<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbackracewithdll">TpSetCallbackRaceWithDll</a>



<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbackthreadpool">TpSetCallbackThreadpool</a>