---
UID: NF:processthreadsapi.QueueUserAPC2
tech.root: processthreadsapi
title: QueueUserAPC2 function (processthreadsapi.h)
ms.date: 08/05/2022
targetos: Windows
description: Adds a user-mode asynchronous procedure call (APC) object to the APC queue of the specified thread. (QueueUserAPC2)
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Kernel32.dll
req.header: processthreadsapi.h
req.idl: 
req.include-header: Windows.h
req.irql: 
req.kmdf-ver: 
req.lib: Kernel32.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11 (Build 22000)
req.target-min-winversvr: Windows Server 2022 (Build 20348)
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - api-ms-win-core-processthreads-l1-1-8.dll
 - api-ms-win-core-processthreads-l1-1-7.dll
 - api-ms-win-core-processthreads-l1-1-6.dll
 - api-ms-win-core-processthreads-l1-1-5.dll
 - processthreadsapi.h
api_name:
 - QueueUserAPC2
f1_keywords:
 - QueueUserAPC2
 - processthreadsapi/QueueUserAPC2
dev_langs:
 - c++
---

# QueueUserAPC2 function

## -description

Adds a user-mode [asynchronous procedure call](/windows/win32/sync/asynchronous-procedure-calls) (APC) object to the APC queue of the specified thread.

## -parameters

### -param ApcRoutine

A pointer to the application-supplied APC function to be called when the specified thread performs an alertable wait operation. For more information, see [APCProc](/windows/desktop/api/winnt/nc-winnt-papcfunc).

For special user-mode APCs, an alertable wait is not required. See [Remarks](#remarks) for more information about special user-mode APCs.

### -param Thread

A handle to the thread. The handle must have <b>THREAD_SET_CONTEXT</b> access permission. For more information, see [Synchronization Object Security and Access Rights](/windows/desktop/Sync/synchronization-object-security-and-access-rights).

### -param Data

A single value that is passed to the APC function pointed to by the *ApcRoutine* parameter.

### -param Flags

A value from [QUEUE_USER_APC_FLAGS enumeration](ne-processthreadsapi-queue_user_apc_flags.md) that modifies the behavior of the user-mode APC.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call [GetLastError](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## -remarks

Regular user-mode APCs are only executed if the target thread is in an alertable state. See [QueueUserAPC function](nf-processthreadsapi-queueuserapc.md) for additional remarks on regular user-mode APCs.

Special user-mode APCs always execute, even if the target thread is not in an alertable state. For example, if the target thread is currently executing user-mode code, or if the target thread is currently performing an alertable wait, the target thread will be interrupted immediately for APC execution. If the target thread is executing a system call, or performing a non-alertable wait, the APC will be executed after the system call or non-alertable wait finishes (the wait is not interrupted).

Since the execution of the special user-mode APC is not synchronized with the target thread, particular care must be taken (beyond the normal requirements for multithreading and synchronization). For example, when acquiring any locks, the interrupted target thread may already own the lock or be in the process of acquiring or releasing the lock. In addition, because there are no facilities to block a thread from receiving special user-mode APCs, a special user-mode APC can be executed on a target thread that is already executing a special user-mode APC.

Currently, special user-mode APCs are only supported on native architectures, and not when running under WoW.

## -see-also
