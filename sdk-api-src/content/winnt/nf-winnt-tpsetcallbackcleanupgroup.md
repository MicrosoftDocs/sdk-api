---
UID: NF:winnt.TpSetCallbackCleanupGroup
title: TpSetCallbackCleanupGroup function (winnt.h)
description: Associates the specified cleanup group with the specified callback environment. (TpSetCallbackCleanupGroup)
helpviewer_keywords: ["TpSetCallbackCleanupGroup","TpSetCallbackCleanupGroup function","base.tpsetcallbackcleanupgroup","winnt/TpSetCallbackCleanupGroup"]
old-location: base\tpsetcallbackcleanupgroup.htm
tech.root: backup
ms.assetid: B14084F5-2686-4522-8024-71A07541CFE2
ms.date: 12/05/2018
ms.keywords: TpSetCallbackCleanupGroup, TpSetCallbackCleanupGroup function, base.tpsetcallbackcleanupgroup, winnt/TpSetCallbackCleanupGroup
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
 - TpSetCallbackCleanupGroup
 - winnt/TpSetCallbackCleanupGroup
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
 - TpSetCallbackCleanupGroup
---

# TpSetCallbackCleanupGroup function


## -description

Associates the specified cleanup group with the specified callback environment.

## -parameters

### -param CallbackEnviron [in, out]

A <b>TP_CALLBACK_ENVIRON</b> structure that defines the callback environment. The <a href="/windows/desktop/api/winnt/nf-winnt-tpinitializecallbackenviron">TpInitializeCallbackEnviron</a> function returns this structure.

### -param CleanupGroup [in]

A <b>TP_CLEANUP_GROUP</b> structure that defines the cleanup group. The <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolcleanupgroup">CreateThreadpoolCleanupGroup</a> function returns this structure.

### -param CleanupGroupCancelCallback [in, optional]

The cleanup callback to be called if the cleanup group is canceled before the associated object is released. The function is called when you call <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolcleanupgroupmembers">CloseThreadpoolCleanupGroupMembers</a>.

## -remarks

This function is implemented as an inline function.

## -see-also

<a href="/windows/desktop/api/winnt/nf-winnt-tpdestroycallbackenviron">TpDestroyCallbackEnviron</a>



<a href="/windows/desktop/api/winnt/nf-winnt-tpinitializecallbackenviron">TpInitializeCallbackEnviron</a>



<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbackactivationcontext">TpSetCallbackActivationContext</a>



<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbackfinalizationcallback">TpSetCallbackFinalizationCallback</a>



<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbacklongfunction">TpSetCallbackLongFunction</a>



<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbacknoactivationcontext">TpSetCallbackNoActivationContext</a>



<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbackpersistent">TpSetCallbackPersistent</a>



<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbackpriority">TpSetCallbackPriority</a>



<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbackracewithdll">TpSetCallbackRaceWithDll</a>



<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbackthreadpool">TpSetCallbackThreadpool</a>
