---
UID: NF:winbase.DequeueUmsCompletionListItems
title: DequeueUmsCompletionListItems function (winbase.h)
description: Retrieves user-mode scheduling (UMS) worker threads from the specified UMS completion list.
helpviewer_keywords: ["DequeueUmsCompletionListItems","DequeueUmsCompletionListItems function","base.dequeueumscompletionlistitems","winbase/DequeueUmsCompletionListItems"]
old-location: base\dequeueumscompletionlistitems.htm
tech.root: backup
ms.assetid: 91499eb9-9fc5-4135-95f6-1bced78f1e07
ms.date: 12/05/2018
ms.keywords: DequeueUmsCompletionListItems, DequeueUmsCompletionListItems function, base.dequeueumscompletionlistitems, winbase/DequeueUmsCompletionListItems
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 (64-bit only) [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DequeueUmsCompletionListItems
 - winbase/DequeueUmsCompletionListItems
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernel32.dll
 - API-MS-Win-Core-ums-l1-1-0.dll
api_name:
 - DequeueUmsCompletionListItems
req.apiset: api-ms-win-core-ums-l1-1-0 (introduced in Windows 7)
---

# DequeueUmsCompletionListItems function


## -description

Retrieves user-mode scheduling (UMS) worker threads from the specified UMS completion list.

> [!WARNING]
> As of Windows 11, user-mode scheduling is not supported. All calls fail with the error `ERROR_NOT_SUPPORTED`.

## -parameters

### -param UmsCompletionList [in]

A pointer to the completion list from which to retrieve worker threads.

### -param WaitTimeOut [in]

The time-out interval for the retrieval operation, in milliseconds. The function returns if the interval elapses, even if no worker threads are queued to the completion list.

If the <i>WaitTimeOut</i> parameter is zero, the completion list is checked for available worker threads without waiting for worker threads to become available. If the <i>WaitTimeOut</i> parameter is INFINITE, the function's time-out interval never elapses. This is not recommended, however, because it causes the function to block until one or more worker threads become available.

### -param UmsThreadList [out]

A pointer to a UMS_CONTEXT variable. On output, this parameter receives a pointer to the first UMS thread context in a list of UMS thread contexts. 

If no worker threads are available before the time-out specified by the <i>WaitTimeOut</i> parameter, this parameter is set to NULL.

## -returns

If the function succeeds, it returns a nonzero value.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Possible error values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
No threads became available before the specified time-out interval elapsed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">UMS is not supported.</td>
</tr>
</table>

## -remarks

The system queues a UMS worker thread to a completion list when the worker thread is created or when a previously blocked worker thread becomes unblocked. The <b>DequeueUmsCompletionListItems</b> function retrieves a pointer to a list of all thread contexts in the specified completion list. The <a href="/windows/desktop/api/winbase/nf-winbase-getnextumslistitem">GetNextUmsListItem</a> function can be used to pop UMS thread contexts off the list into the scheduler's own ready thread queue. The scheduler is responsible for selecting threads to run based on priorities chosen by the application.

Do not run UMS threads directly from the list provided by <b>DequeueUmsCompletionListItems</b>, or run a thread transferred from the list to  the ready thread queue before the list is completely empty. This can cause unpredictable behavior in the application.

If more than one caller attempts to retrieve threads from a shared completion list, only the first caller retrieves the threads. For subsequent callers,  the <b>DequeueUmsCompletionListItems</b> function returns success but the <i>UmsThreadList</i> parameter is set to NULL.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-getnextumslistitem">GetNextUmsListItem</a>
