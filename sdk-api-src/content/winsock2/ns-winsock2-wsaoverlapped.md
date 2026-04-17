---
UID: NS:winsock2._WSAOVERLAPPED
title: WSAOVERLAPPED (winsock2.h)
description: Provides a communication medium between the initiation of an overlapped I/O operation and its subsequent completion.
helpviewer_keywords: ["*LPWSAOVERLAPPED","LPWSAOVERLAPPED","LPWSAOVERLAPPED structure pointer [Winsock]","WSAOVERLAPPED","WSAOVERLAPPED structure [Winsock]","_win32_wsaoverlapped_2","winsock.wsaoverlapped_2","winsock2/LPWSAOVERLAPPED","winsock2/WSAOVERLAPPED"]
old-location: winsock\wsaoverlapped_2.htm
tech.root: WinSock
ms.assetid: 91004241-e0ea-4bda-a0f5-71688ac83038
ms.date: 04/17/2026
ms.keywords: '*LPWSAOVERLAPPED, LPWSAOVERLAPPED, LPWSAOVERLAPPED structure pointer [Winsock], WSAOVERLAPPED, WSAOVERLAPPED structure [Winsock], _win32_wsaoverlapped_2, winsock.wsaoverlapped_2, winsock2/LPWSAOVERLAPPED, winsock2/WSAOVERLAPPED'
req.header: winsock2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: WSAOVERLAPPED, *LPWSAOVERLAPPED
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSAOVERLAPPED
 - winsock2/_WSAOVERLAPPED
 - LPWSAOVERLAPPED
 - winsock2/LPWSAOVERLAPPED
 - WSAOVERLAPPED
 - winsock2/WSAOVERLAPPED
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winsock2.h
api_name:
 - WSAOVERLAPPED
---

# WSAOVERLAPPED structure


## -description

The **WSAOVERLAPPED** structure provides a communication medium between the initiation of an overlapped I/O operation and its subsequent completion.

On Win32, **WSAOVERLAPPED** is a typedef for the [OVERLAPPED](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure — the two structures are identical and interchangeable. **LPWSAOVERLAPPED** is a typedef for `_OVERLAPPED*`. Any function that accepts an **OVERLAPPED** pointer can accept an **LPWSAOVERLAPPED**, and vice versa.

> [!NOTE]
> On 16-bit Windows (Win16), **WSAOVERLAPPED** was a distinct structure. On all modern (Win32) platforms, it is identical to **OVERLAPPED**.

## -struct-fields

### -field Internal

Type: **ULONG_PTR**

Reserved for internal use by the operating system. When an overlapped I/O request is issued, the system sets this member to **STATUS_PENDING**. When the operation completes, the system sets it to the NT status code for the completed request. Applications must not modify this field.

For IFS (installable file system) socket providers, this field is managed directly by the kernel. Non-IFS providers may use it as needed, but must not depend on its value across calls.

### -field InternalHigh

Type: **ULONG_PTR**

Reserved for internal use by the operating system. On completion of an overlapped I/O request, the system sets this member to the number of bytes transferred. Applications must not modify this field.

### -field Offset

Type: **DWORD**

Reserved for use by service providers. Winsock overlapped operations on sockets do not use a file offset, so this member is not meaningful for socket I/O. Initialize to zero before use.

> [!NOTE]
> **Offset** and **OffsetHigh** are part of a union with **Pointer** (see below). Only one of these alternatives should be used for a given operation.

### -field OffsetHigh

Type: **DWORD**

Reserved for use by service providers. The high-order 32 bits of the file position, paired with **Offset** to form a 64-bit value. Not used for socket I/O. Initialize to zero before use.

### -field hEvent

Type: **HANDLE**

A handle to a **WSAEVENT** (event object) that the system sets to the signaled state when the overlapped I/O operation completes.

- **With a completion routine** (the `lpCompletionRoutine` parameter of the Winsock call is non-NULL): The system ignores `hEvent` on completion. Applications are free to use this field for their own purposes in this case — a common pattern is to store a context pointer here, cast to **HANDLE**.

- **Without a completion routine and without an I/O completion port**: Set `hEvent` to a valid **WSAEVENT** handle created with [WSACreateEvent](/windows/desktop/api/winsock2/nf-winsock2-wsacreateevent). The system signals the event when the operation completes. Use [WSAGetOverlappedResult](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult) to retrieve the result and reset the event.

- **With an I/O completion port**: When a socket is associated with an I/O completion port via [CreateIoCompletionPort](/windows/desktop/FileIO/createiocompletionport), completion notifications are delivered to the port rather than through `hEvent`. In this case, `hEvent` is ignored by the system and may be set to NULL.

Always initialize this member to a valid event handle or NULL before passing the structure to any overlapped Winsock function. Leaving it uninitialized may cause unpredictable behavior.

#### - Pointer

Type: **PVOID**

An alternative member in the same union as **Offset** and **OffsetHigh**. Reserved for use by service providers. Initialize to NULL before use.

## -remarks

The **WSAOVERLAPPED** structure (and its alias **OVERLAPPED**) is the standard mechanism for asynchronous I/O notification in Windows. All overlapped Winsock functions — such as [WSARecv](/windows/desktop/api/winsock2/nf-winsock2-wsarecv), [WSASend](/windows/desktop/api/winsock2/nf-winsock2-wsasend), and [WSASendTo](/windows/desktop/api/winsock2/nf-winsock2-wsasendto) — accept a pointer to a **WSAOVERLAPPED** structure.

**Initialization:** Always zero-initialize the **WSAOVERLAPPED** structure before use, except for `hEvent`, which must be set to either NULL or a valid event handle. Passing an uninitialized structure to an overlapped function may cause the function to fail with **ERROR_INVALID_PARAMETER**.

**Lifetime:** The **WSAOVERLAPPED** structure (and all buffers associated with the overlapped operation) must remain valid and pinned in memory until the operation completes. Do not free or modify the structure while an operation is pending.

**Completion notification:** Three mechanisms are available:

| Mechanism | How to use |
|-----------|------------|
| Event object | Set `hEvent` to a valid **WSAEVENT**. Wait on the event, then call **WSAGetOverlappedResult**. |
| Completion routine | Pass a non-NULL `lpCompletionRoutine`. The routine is called in an alertable wait state. |
| I/O completion port | Associate the socket handle with an IOCP using **CreateIoCompletionPort**. Poll with **GetQueuedCompletionStatus**. |

For more information about the underlying structure layout and general overlapped I/O semantics, see [OVERLAPPED](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped).

## -see-also

<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>

<a href="/windows/desktop/api/winsock/nf-winsock-wsacleanup">WSACleanup</a>

<a href="/windows/desktop/api/winsock2/nf-winsock2-wsacloseevent">WSACloseEvent</a>

<a href="/windows/desktop/api/winsock2/nf-winsock2-wsacreateevent">WSACreateEvent</a>

<a href="/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult">WSAGetOverlappedResult</a>

<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecv">WSARecv</a>

<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasend">WSASend</a>

<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasendto">WSASendTo</a>

<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasocketa">WSASocket</a>

<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a>

<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a>

<a href="/windows/desktop/api/winsock/nf-winsock-closesocket">closesocket</a>
