---
UID: NC:winsock2.LPWSAOVERLAPPED_COMPLETION_ROUTINE
title: LPWSAOVERLAPPED_COMPLETION_ROUTINE
description: TBD (LPWSAOVERLAPPED_COMPLETION_ROUTINE)
ms.date: 07/27/2022
tech.root: WinSock
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: winsock2.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - winsock2.h
api_name:
 - LPWSAOVERLAPPED_COMPLETION_ROUTINE
f1_keywords:
 - LPWSAOVERLAPPED_COMPLETION_ROUTINE
 - winsock2/LPWSAOVERLAPPED_COMPLETION_ROUTINE
dev_langs:
 - c++
---

## -description

**LPWSAOVERLAPPED_COMPLETION_ROUTINE** is a function pointer type. You implement a matching callback function in your app, and pass that to functions such as [WSAIoctl](./nf-winsock2-wsaioctl.md), [WSARecv](./nf-winsock2-wsarecv.md), and [WSASend](./nf-winsock2-wsasend.md), among others.

The system calls your callback function when the asynchronous input and output (I/O) operation is completed or canceled, and the calling thread is in an alertable state (by using the <a href="/windows/win32/api/synchapi/nf-synchapi-sleepex">SleepEx</a>, <a href="/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjectsex">MsgWaitForMultipleObjectsEx</a>, <a href="/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex">WaitForSingleObjectEx</a>, or <a href="/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjectsex">WaitForMultipleObjectsEx</a> function with the <i>fAlertable</i> parameter set to <b>TRUE</b>).

## -parameters

### -param dwError

Type: IN **[DWORD](/windows/win32/winprog/windows-data-types)**

The I/O completion status. This parameter can be one of the <a href="/windows/win32/Debug/system-error-codes">system error codes</a>.

### -param cbTransferred

Type: IN **[DWORD](/windows/win32/winprog/windows-data-types)**

The number of bytes transferred. If an error occurs, this parameter is zero.

### -param lpOverlapped

Type: IN **[LPWSAOVERLAPPED](./ns-winsock2-wsaoverlapped.md)**

A pointer to the [**WSAOVERLAPPED**](./ns-winsock2-wsaoverlapped.md) structure specified by the asynchronous I/O function.

The system doesn't use the [**WSAOVERLAPPED**](./ns-winsock2-wsaoverlapped.md) structure after the completion routine is called, so the completion routine can deallocate the memory used by the overlapped structure.

### -param dwFlags

Type: IN **[DWORD](/windows/win32/winprog/windows-data-types)**

Flags associated with the call.

## -remarks

See [**LPOVERLAPPED_COMPLETION_ROUTINE**](../minwinbase/nc-minwinbase-lpoverlapped_completion_routine.md).

## -see-also
