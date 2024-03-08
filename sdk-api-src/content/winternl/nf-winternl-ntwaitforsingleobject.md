---
UID: NF:winternl.NtWaitForSingleObject
title: NtWaitForSingleObject function (winternl.h)
description: Deprecated. Waits until the specified object attains a state of signaled. NtWaitForSingleObject is superseded by WaitForSingleObject.
helpviewer_keywords: ["NtWaitForSingleObject","FALSE","NtWaitForSingleObject","NtWaitForSingleObject function [Windows API]","TRUE","winprog.ntwaitforsingleobject","winternl/NtWaitForSingleObject","winui.ntwaitforsingleobject"]
old-location: winprog\ntwaitforsingleobject.htm
tech.root: winprog
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\misc\ntwaitforsingleobject.htm
ms.date: 12/05/2018
ms.keywords: "'NtWaitForSingleObject, FALSE, NtWaitForSingleObject, NtWaitForSingleObject function [Windows API], TRUE, winprog.ntwaitforsingleobject, winternl/NtWaitForSingleObject, winui.ntwaitforsingleobject"
req.header: winternl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ntdll.lib
req.dll: ntdll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NtWaitForSingleObject
 - winternl/NtWaitForSingleObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdll.dll
api_name:
 - NtWaitForSingleObject
---

# NtWaitForSingleObject function


## -description

Deprecated. Waits until the specified object attains a state of
    <code>signaled</code>. <b>NtWaitForSingleObject</b> is superseded by <a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject">WaitForSingleObject</a>.

## -parameters

### -param Handle [in]

The handle to the wait object.

### -param Alertable [in]

Specifies whether an alert can be delivered when the object is waiting.



#### TRUE

The alert can be delivered.



#### FALSE

The alert cannot be delivered.

### -param Timeout [in]

A pointer to an absolute or relative time over
        which the wait is to occur. Can be null. If a timeout is specified, and
    the object has not attained a state of <code>signaled</code> when the timeout
    expires, then the wait is automatically satisfied.  If an explicit
    timeout value of zero is specified, then no wait occurs if the
    wait cannot be satisfied immediately.

## -returns

The wait completion status. The various NTSTATUS values are defined in NTSTATUS.H, which is distributed with the Windows DDK.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The specified
    object satisfied the wait. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
A
    timeout occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_ALERTED</b></dt>
</dl>
</td>
<td width="60%">
The
    wait was aborted to deliver an alert to the current thread.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_USER_APC</b></dt>
</dl>
</td>
<td width="60%">
The wait was aborted to deliver a user <a href="/windows/desktop/Sync/asynchronous-procedure-calls">Asynchronous Procedure Call (APC)</a> to the current thread.

</td>
</tr>
</table>

## -remarks

Because there is no import library for this function, you must use <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>.