---
UID: NC:mswsock.LPFN_RIOCREATEREQUESTQUEUE
title: LPFN_RIOCREATEREQUESTQUEUE
description: Creates a registered I/O socket descriptor using a specified socket and I/O completion queues for use with the Winsock registered I/O extensions.
helpviewer_keywords: ["LPFN_RIOCREATEREQUESTQUEUE"]
old-location: 
tech.root: WinSock
ms.assetid: CB69E0B6-519D-4268-A09B-196BBB6EB460
ms.date: 01/30/2019
ms.keywords: LPFN_RIOCREATEREQUESTQUEUE
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
 - LPFN_RIOCREATEREQUESTQUEUE
 - mswsock/LPFN_RIOCREATEREQUESTQUEUE
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - mswsock.h
api_name:
 - LPFN_RIOCREATEREQUESTQUEUE
---

## -description

The **RIOCreateRequestQueue** function creates a registered I/O socket descriptor using a specified socket and I/O completion queues for use with the Winsock registered I/O extensions.

## -parameters

### -param Socket

A descriptor that identifies the socket.

### -param MaxOutstandingReceive

The maximum number of outstanding receives allowed on the socket.

This parameter is usually a small number for most applications.

### -param MaxReceiveDataBuffers

The maximum number of receive data buffers on the socket.

> [!Note]  
> For Windows 8 and Windows Server 2012 , this parameter must be **1**.

### -param MaxOutstandingSend

The maximum number of outstanding sends allowed on the socket.

### -param MaxSendDataBuffers

The maximum number of send data buffers on the socket.

> [!Note]  
> For Windows 8 and Windows Server 2012 , this parameter must be **1**.

### -param ReceiveCQ

A descriptor that identifies the I/O completion queue to use for receive request completions.

### -param SendCQ

A descriptor that identifies the I/O completion queue to use for send request completions.

This parameter may have the same value as the *ReceiveCQ* parameter.

### -param SocketContext

The socket context to associate with this request queue.

## -returns

If no error occurs, the **RIOCreateRequestQueue** function returns a descriptor referencing a new request queue. Otherwise, a value of **RIO\_INVALID\_RQ** is returned, and a specific error code can be retrieved by calling the [**WSAGetLastError**](../winsock/nf-winsock-wsagetlasterror.md) function.



| Return code                                                                                                                                     | Description                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**[WSAEINVAL](/windows/win32/winsock/windows-sockets-error-codes-2#wsaeinval)**</dt> </dl>         | An invalid parameter was passed to the function. <br/> This error is returned if the *ReceiveCQ* or *SendCQ* parameters contained **RIO\_INVALID\_CQ**. This error is returned if both the *MaxOutstandingReceive* and *MaxOutstandingSend* parameters are zero. This error is also returned if the socket passed in the *Socket* parameter is in the process of initializing or closing.<br/> |
| <dl> <dt>**[WSAENOBUFS](/windows/win32/winsock/windows-sockets-error-codes-2#wsaenobufs)**</dt> </dl>       | Sufficient memory could not be allocated. This error is returned if there was insufficient memory to allocate the request queue based on the parameters. This error is also returned if the network session limit was exceeded. <br/>                                                                                                                                                                |
| <dl> <dt>**[WSAENOTSOCK](/windows/win32/winsock/windows-sockets-error-codes-2#wsaenotsock)**</dt> </dl>     | The descriptor is not a socket. This error is returned if the *Socket* parameter is not a valid socket.<br/>                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**[WSAEOPNOTSUPP](/windows/win32/winsock/windows-sockets-error-codes-2#wsaeopnotsupp)**</dt> </dl> | The attempted operation is not supported for the type of object referenced. This error is returned for a socket in the *Socket* parameter for an unsupported socket type (**SOCK\_RAW**, for example)<br/>                                                                                                                                                                                           |

## -remarks

The **RIOCreateRequestQueue** function creates a registered I/O socket descriptor using a specified socket and I/O completion queues. An application must call **RIOCreateRequestQueue** to obtain a [**RIO\_RQ**](/windows/win32/winsock/riorqueue) for a Winsock socket before the application can use the [**RIOSend**](./nc-mswsock-lpfn_riosend.md), [**RIOSendEx**](./nc-mswsock-lpfn_riosendex.md), [**RIOReceive**](./nc-mswsock-lpfn_rioreceive.md), or [**RIOReceiveEx**](./nc-mswsock-lpfn_rioreceiveex.md) functions. In order to obtain a **RIO\_RQ**, the Winsock socket must be associated with completion queues for send and receive, although the same completion queue can be used for both.

Due to the finite size of completion queues, a socket may only be associated with a completion queue for send and receive operations if it guarantees not to exceed the capacity for total queued completions. Therefore, socket specific limits are established by the call to the **RIOCreateRequestQueue** function. These limits are used both during the **RIOCreateRequestQueue** call to verify sufficient space in the completion queues to accommodate the socket requests and during request initiation time to make sure that the request does not cause the socket to exceed its limits.

The send and receive queues can be associated with multiple sockets. The sizes of the send and receive queues must be greater than or equal to the send and receive sizes of all attached sockets. As request queues are closed by closing the sockets using the [**closesocket**](../winsock/nf-winsock-closesocket.md) function, those slots will be freed up for use by other sockets.

> [!Note]  
> For purposes of efficiency, access to the completion queues ([**RIO\_CQ**](/windows/win32/winsock/riocqueue) structs) and request queues ([**RIO\_RQ**](/windows/win32/winsock/riorqueue) structs) are not protected by synchronization primitives. If you need to access a completion or request queue from multiple threads, access should be coordinated by a critical section, slim reader write lock or similar mechanism. This locking is not needed for access by a single thread. Different threads can access separate requests/completion queues without locks. The need for synchronization occurs only when multiple threads try to access the same queue. Synchronization is also required if multiple threads issue sends and receives on the same socket because the send and receive operations use the socket’s request queue.

 

When an application is finished using the [**RIO\_RQ**](/windows/win32/winsock/riorqueue), the application should call the [**closesocket**](../winsock/nf-winsock-closesocket.md) function to close the socket and free the associated resources.

> [!Note]  
> The function pointer to the **RIOCreateRequestQueue** function must be obtained at run time by making a call to the [**WSAIoctl**](../winsock2/nf-winsock2-wsaioctl.md) function with the **SIO\_GET\_MULTIPLE\_EXTENSION\_FUNCTION\_POINTER** opcode specified. The input buffer passed to the **WSAIoctl** function must contain **WSAID\_MULTIPLE\_RIO**, a globally unique identifier (GUID) whose value identifies the Winsock registered I/O extension functions. On success, the output returned by the **WSAIoctl** function contains a pointer to the [**RIO\_EXTENSION\_FUNCTION\_TABLE**](./ns-mswsock-rio_extension_function_table.md) structure that contains pointers to the Winsock registered I/O extension functions. The **SIO\_GET\_MULTIPLE\_EXTENSION\_FUNCTION\_POINTER** IOCTL is defined in the *Ws2def.h* header file. The **WSAID\_MULTIPLE\_RIO** GUID is defined in the *Mswsock.h* header file.

 

**Windows Phone 8:** This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

**Windows 8.1** and **Windows Server 2012 R2**: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also