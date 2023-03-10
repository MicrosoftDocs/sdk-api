---
UID: NF:winbase.SetThreadpoolCallbackPriority
title: SetThreadpoolCallbackPriority function (winbase.h)
description: Specifies the priority of a callback function relative to other work items in the same thread pool. (SetThreadpoolCallbackPriority)
helpviewer_keywords: ["SetThreadpoolCallbackPriority","SetThreadpoolCallbackPriority function","TP_CALLBACK_PRIORITY_HIGH","TP_CALLBACK_PRIORITY_LOW","TP_CALLBACK_PRIORITY_NORMAL","base.setthreadpoolcallbackpriority","winbase/SetThreadpoolCallbackPriority"]
old-location: base\setthreadpoolcallbackpriority.htm
tech.root: backup
ms.assetid: c24d3e9b-5a4e-43e1-a903-b612d022aa97
ms.date: 12/05/2018
ms.keywords: SetThreadpoolCallbackPriority, SetThreadpoolCallbackPriority function, TP_CALLBACK_PRIORITY_HIGH, TP_CALLBACK_PRIORITY_LOW, TP_CALLBACK_PRIORITY_NORMAL, base.setthreadpoolcallbackpriority, winbase/SetThreadpoolCallbackPriority
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - SetThreadpoolCallbackPriority
 - winbase/SetThreadpoolCallbackPriority
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - SetThreadpoolCallbackPriority
---

# SetThreadpoolCallbackPriority function


## -description

Specifies the priority of a callback function relative to other work items in the same thread pool.

## -parameters

### -param pcbe [in, out]

A <b>TP_CALLBACK_ENVIRON</b> structure that defines the callback environment. The <a href="/windows/desktop/api/winbase/nf-winbase-initializethreadpoolenvironment">InitializeThreadpoolEnvironment</a> function returns this structure.

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

To compile an application that uses this function, set _WIN32_WINNT &gt;= _WIN32_WINNT_WIN7. For more information, see <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.
