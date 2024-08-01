---
UID: NF:threadpoollegacyapiset.QueueUserWorkItem
title: QueueUserWorkItem function (threadpoollegacyapiset.h)
description: Queues a work item to a worker thread in the thread pool.
helpviewer_keywords: ["QueueUserWorkItem","QueueUserWorkItem function","WT_EXECUTEDEFAULT","WT_EXECUTEINIOTHREAD","WT_EXECUTEINPERSISTENTTHREAD","WT_EXECUTELONGFUNCTION","WT_TRANSFER_IMPERSONATION","_win32_queueuserworkitem","base.queueuserworkitem","threadpoollegacyapiset/QueueUserWorkItem","winbase/QueueUserWorkItem"]
old-location: base\queueuserworkitem.htm
tech.root: backup
ms.assetid: 96f34b51-3784-4bb7-ae40-067f8113ff39
ms.date: 12/05/2018
ms.keywords: QueueUserWorkItem, QueueUserWorkItem function, WT_EXECUTEDEFAULT, WT_EXECUTEINIOTHREAD, WT_EXECUTEINPERSISTENTTHREAD, WT_EXECUTELONGFUNCTION, WT_TRANSFER_IMPERSONATION, _win32_queueuserworkitem, base.queueuserworkitem, threadpoollegacyapiset/QueueUserWorkItem, winbase/QueueUserWorkItem
req.header: threadpoollegacyapiset.h
req.include-header: Windows.h on Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - QueueUserWorkItem
 - threadpoollegacyapiset/QueueUserWorkItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-threadpool-legacy-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - QueueUserWorkItem
---

# QueueUserWorkItem function


## -description

Queues a work item to a worker thread in the 
<a href="/windows/desktop/ProcThread/thread-pooling">thread pool</a>.

## -parameters

### -param Function [in]

A pointer to the application-defined callback function of type <b>LPTHREAD_START_ROUTINE</b> to be executed by the thread in the thread pool. This value represents the starting address of the thread. This callback function must not call the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread">TerminateThread</a> function. 

The return value of the callback function is not used.

For more information, see 
<a href="/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)">ThreadProc</a>.

### -param Context [in, optional]

A single parameter value to be passed to the thread function.

### -param Flags [in]

The flags that control execution. This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WT_EXECUTEDEFAULT"></a><a id="wt_executedefault"></a><dl>
<dt><b>WT_EXECUTEDEFAULT</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
By default, the callback function is queued to a non-I/O worker thread.

The callback function is queued to a thread that uses I/O completion ports, which means they cannot perform an alertable wait. Therefore, if I/O completes and generates an APC, the APC might wait indefinitely because there is no guarantee that the thread will enter an alertable wait state after the callback completes.

</td>
</tr>
<tr>
<td width="40%"><a id="WT_EXECUTEINIOTHREAD"></a><a id="wt_executeiniothread"></a><dl>
<dt><b>WT_EXECUTEINIOTHREAD</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
This flag is not used.

<b>Windows Server 2003 and Windows XP:  </b>The callback function is queued to an I/O worker thread. This flag should be used if the function should be executed in a thread that waits in an alertable state. 


I/O worker threads were removed starting with Windows Vista and Windows Server 2008.

</td>
</tr>
<tr>
<td width="40%"><a id="WT_EXECUTEINPERSISTENTTHREAD"></a><a id="wt_executeinpersistentthread"></a><dl>
<dt><b>WT_EXECUTEINPERSISTENTTHREAD</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
The callback function is queued to a thread that never terminates. It does not guarantee that the same thread is used each time. This flag should be used only for short tasks or it could affect other timer operations. 


This flag must be set if the thread calls functions that use APCs. For more information, see <a href="/windows/desktop/Sync/asynchronous-procedure-calls">Asynchronous Procedure Calls</a>.

Note that currently no worker thread is truly persistent, although worker threads do not terminate if there are any pending I/O requests.

</td>
</tr>
<tr>
<td width="40%"><a id="WT_EXECUTELONGFUNCTION"></a><a id="wt_executelongfunction"></a><dl>
<dt><b>WT_EXECUTELONGFUNCTION</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
The callback function can perform a long wait. This flag helps the system to decide if it should create a new thread.

</td>
</tr>
<tr>
<td width="40%"><a id="WT_TRANSFER_IMPERSONATION"></a><a id="wt_transfer_impersonation"></a><dl>
<dt><b>WT_TRANSFER_IMPERSONATION</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
Callback functions will use the current access token, whether it is a process or impersonation token. If this flag is not specified, callback functions execute only with the process token.

<b>Windows XP:  </b>This flag is not supported until Windows XP SP2 and Windows Server 2003.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If a function in a DLL is queued to a worker thread, be sure that the function has completed execution before the DLL is unloaded.

By default, the thread pool has a maximum of 512 threads per process. To raise the queue limit, use the <b>WT_SET_MAX_THREADPOOL_THREAD</b> macro defined in WinNT.h.


``` syntax
#define WT_SET_MAX_THREADPOOL_THREADS(Flags,Limit) \
    ((Flags)|=(Limit)<<16)
```

Use this macro in the call to <b>QueueUserWorkItem</b> to specify the <i>Flags</i> parameter. The macro parameters are the desired flags and the new limit, up to (2&lt;&lt;16)-1 threads. However, the size of the queue is limited by the size of the kernel nonpaged pool. Note that your application can improve its performance by keeping the number of worker threads low.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0500 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/ProcThread/thread-pooling">Thread Pooling</a>



<a href="/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)">ThreadProc</a>
