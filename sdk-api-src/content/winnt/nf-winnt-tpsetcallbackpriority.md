---
UID: NF:winnt.TpSetCallbackPriority
title: TpSetCallbackPriority function (winnt.h)
description: Specifies the priority of a callback function relative to other work items in the same thread pool. (TpSetCallbackPriority)
helpviewer_keywords: ["TP_CALLBACK_PRIORITY_HIGH","TP_CALLBACK_PRIORITY_LOW","TP_CALLBACK_PRIORITY_NORMAL","TpSetCallbackPriority","TpSetCallbackPriority function","base.tpsetcallbackpriority","winnt/TpSetCallbackPriority"]
old-location: base\tpsetcallbackpriority.htm
tech.root: backup
ms.assetid: 3A2DA8CA-D5F2-442A-B152-11AB28681B5B
ms.date: 12/05/2018
ms.keywords: TP_CALLBACK_PRIORITY_HIGH, TP_CALLBACK_PRIORITY_LOW, TP_CALLBACK_PRIORITY_NORMAL, TpSetCallbackPriority, TpSetCallbackPriority function, base.tpsetcallbackpriority, winnt/TpSetCallbackPriority
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
 - TpSetCallbackPriority
 - winnt/TpSetCallbackPriority
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
 - TpSetCallbackPriority
---

# TpSetCallbackPriority function


## -description

Specifies the priority of a callback function relative to other work items in the same thread pool.

## -parameters

### -param CallbackEnviron [in, out]

A <b>TP_CALLBACK_ENVIRON</b> structure that defines the callback environment. The <a href="/windows/desktop/api/winnt/nf-winnt-tpinitializecallbackenviron">TpInitializeCallbackEnviron</a> function returns this structure.

### -param Priority [in]

The priority for the callback relative to other callbacks in the same thread pool. This parameter can be one of the following <b>TP_CALLBACK_PRIORITY</b> enumeration values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TP_CALLBACK_PRIORITY_HIGH"></a><a id="tp_callback_priority_high"></a><dl>
<dt><b>TP_CALLBACK_PRIORITY_HIGH</b></dt>
</dl>
</td>
<td width="60%">
The callback should run at high priority. 

</td>
</tr>
<tr>
<td width="40%"><a id="TP_CALLBACK_PRIORITY_LOW"></a><a id="tp_callback_priority_low"></a><dl>
<dt><b>TP_CALLBACK_PRIORITY_LOW</b></dt>
</dl>
</td>
<td width="60%">
The callback should run at low priority.

</td>
</tr>
<tr>
<td width="40%"><a id="TP_CALLBACK_PRIORITY_NORMAL"></a><a id="tp_callback_priority_normal"></a><dl>
<dt><b>TP_CALLBACK_PRIORITY_NORMAL</b></dt>
</dl>
</td>
<td width="60%">
The callback should run at normal priority.

</td>
</tr>
</table>

## -remarks

Higher priority callbacks are guaranteed to be run first by the first available worker thread, but they are not guaranteed to finish before lower priority callbacks.

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



<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbackracewithdll">TpSetCallbackRaceWithDll</a>



<a href="/windows/desktop/api/winnt/nf-winnt-tpsetcallbackthreadpool">TpSetCallbackThreadpool</a>
