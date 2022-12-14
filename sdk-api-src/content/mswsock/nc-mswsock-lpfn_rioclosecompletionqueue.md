---
UID: NC:mswsock.LPFN_RIOCLOSECOMPLETIONQUEUE
title: LPFN_RIOCLOSECOMPLETIONQUEUE
description: Closes an existing completion queue used for I/O completion notification by send and receive requests with the Winsock registered I/O extensions.
helpviewer_keywords: ["LPFN_RIOCLOSECOMPLETIONQUEUE"]
old-location: 
tech.root: WinSock
ms.assetid: A5700ACD-3F4B-4AFF-8BA1-6AC59402E06C
ms.date: 01/30/2019
ms.keywords: LPFN_RIOCLOSECOMPLETIONQUEUE
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: mswsock.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - LPFN_RIOCLOSECOMPLETIONQUEUE
 - mswsock/LPFN_RIOCLOSECOMPLETIONQUEUE
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - mswsock.h
api_name:
 - LPFN_RIOCLOSECOMPLETIONQUEUE
---

## -description

The **RIOCloseCompletionQueue** function closes an existing completion queue used for I/O completion notification by send and receive requests with the Winsock registered I/O extensions.

## -parameters

### -param CQ

A descriptor identifying an existing completion queue.

## -remarks

The **RIOCloseCompletionQueue** function closes an existing completion queue used for I/O completion. The [**RIO\_CQ**](/windows/win32/winsock/riocqueue) passed in the *CQ* parameter is locked for writing by the kernel. The completion queue is marked as invalid, so that new completions cannot be added. Any new completions to be added are silently dropped. The application is expected to tracking any pending send or receive operations.

If an invalid completion queue is passed in the *CQ* parameter (**RIO\_INVALID\_CQ**, for example), this is ignored by the **RIOCloseCompletionQueue** function.

> [!Note]  
> The function pointer to the **RIOCloseCompletionQueue** function must be obtained at run time by making a call to the [**WSAIoctl**](../winsock2/nf-winsock2-wsaioctl.md) function with the **SIO\_GET\_MULTIPLE\_EXTENSION\_FUNCTION\_POINTER** opcode specified. The input buffer passed to the **WSAIoctl** function must contain **WSAID\_MULTIPLE\_RIO**, a globally unique identifier (GUID) whose value identifies the Winsock registered I/O extension functions. On success, the output returned by the **WSAIoctl** function contains a pointer to the [**RIO\_EXTENSION\_FUNCTION\_TABLE**](./ns-mswsock-rio_extension_function_table.md) structure that contains pointers to the Winsock registered I/O extension functions. The **SIO\_GET\_MULTIPLE\_EXTENSION\_FUNCTION\_POINTER** IOCTL is defined in the *Ws2def.h* header file. The **WSAID\_MULTIPLE\_RIO** GUID is defined in the *Mswsock.h* header file.

 

**Windows Phone 8:** This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

**Windows 8.1** and **Windows Server 2012 R2**: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also