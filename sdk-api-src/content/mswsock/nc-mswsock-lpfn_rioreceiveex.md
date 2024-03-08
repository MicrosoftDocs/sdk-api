---
UID: NC:mswsock.LPFN_RIORECEIVEEX
title: LPFN_RIORECEIVEEX
description: Receives network data on a connected registered I/O TCP socket or a bound registered I/O UDP socket with additional options for use with the Winsock registered I/O extensions.
helpviewer_keywords: ["LPFN_RIORECEIVEEX"]
old-location: 
tech.root: WinSock
ms.assetid: 74C006D0-EE13-4518-8ACC-C0CFD44D09A3
ms.date: 01/30/2019
ms.keywords: LPFN_RIORECEIVEEX
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
 - LPFN_RIORECEIVEEX
 - mswsock/LPFN_RIORECEIVEEX
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - mswsock.h
api_name:
 - LPFN_RIORECEIVEEX
---

## -description

The **RIOReceiveEx** function receives network data on a connected registered I/O TCP socket or a bound registered I/O UDP socket with additional options for use with the Winsock registered I/O extensions.

## -parameters

### -param SocketQueue

A descriptor that identifies a connected registered I/O UDP socket or a bound registered I/O UDP socket.

### -param pData

A description of the portion of the registered buffer in which to receive data.

This parameter may be NULL for a bound registered I/O UDP socket if the application does not need to receive a data payload in the UDP datagram.

### -param DataBufferCount

A data buffer count parameter that indicates if data is to be received in the buffer pointed to by the *pData* parameter.

This parameter should be set to zero if the *pData* is NULL. Otherwise, this parameter should be set to 1.

### -param pLocalAddress

A buffer segment that on completion will hold the local address on which the network data was received.

This parameter may be **NULL** if the application does not want to receive the local address. If this parameter is not **NULL**, then the buffer segment must be at least the size of a [**SOCKADDR\_INET**](../ws2ipdef/ns-ws2ipdef-sockaddr_inet.md) structure.

### -param pRemoteAddress

A buffer segment that on completion will hold the remote address from which the network data was received.

This parameter may be **NULL** if the application does not want to receive the remote address. If this parameter is not **NULL**, then the buffer segment must be at least the size of a [**SOCKADDR\_INET**](../ws2ipdef/ns-ws2ipdef-sockaddr_inet.md) structure.

### -param pControlContext

A buffer slice that on completion will hold additional control information about the receive operation.

This parameter may be **NULL** if the application does not want to receive the additional control information.

### -param pFlags\\A buffer slice that on completion will hold additional information about the set of flags for the receive operation.

This parameter may be **NULL** if the application does not want to receive the additional flags information.

### -param Flags

A set of flags that modify the behavior of the **RIOReceiveEx** function.

The *Flags* parameter can contain a combination of the following options, defined in the `Mswsockdef.h` header file:

#### RIO_MSG_COMMIT_ONLY

Previous requests added with **RIO_MSG_DEFER** flag will be committed.

When the **RIO_MSG_COMMIT_ONLY** flag is set, no other flags may be specified. When the **RIO_MSG_COMMIT_ONLY** flag is set, the *pData*, *pLocalAddress*, *pRemoteAddress*, *pControlContext*, *pFlags*, and *RequestContext* arguments must be NULL, and the *DataBufferCount* argument must be zero.

This flag would normally be used occasionally after a number of requests were issued with the **RIO_MSG_DEFER** flag set. This eliminates the need when using the **RIO_MSG_DEFER** flag to make the last request without the **RIO_MSG_DEFER** flag, which causes the last request to complete much more slowly than other requests.

Unlike other calls to the **RIOReceiveEx** function, when the **RIO_MSG_COMMIT_ONLY** flag is set calls to the **RIOReceiveEx** function do not need to be serialized. For a single [RIO_RQ](/windows/win32/winsock/riorqueue), the **RIOReceiveEx** function can be called with **RIO_MSG_COMMIT_ONLY** on one thread while calling the **RIOReceiveEx** function on another thread.  

#### RIO_MSG_DONT_NOTIFY

The request should not trigger the [RIONotify](./nc-mswsock-lpfn_rionotify.md) function when request completion is inserted into its completion queue.

#### RIO_MSG_DEFER

The request doesn't need to be executed immediately. This will insert the request into the request queue, but it may or may not trigger the execution of the request.

Data reception might be delayed until a receive request is made on the [RIO_RQ](/windows/win32/winsock/riorqueue) passed in the *SocketQueue* parameter without the **RIO_MSG_DEFER** flag set. To trigger execution for all receives in a request queue, call the [RIOReceive](./nc-mswsock-lpfn_rioreceive.md) or **RIOReceiveEx** function without the **RIO_MSG_DEFER** flag set.  

> [!NOTE]
> The receive request is charged against the outstanding I/O capacity on the [RIO_RQ](/windows/win32/winsock/riorqueue) passed in the *SocketQueue* parameter regardless of whether **RIO_MSG_DEFER** is set.

#### RIO_MSG_WAITALL

The **RIOReceiveEx** function won't complete until one of the following events occurs:

* The buffer slice supplied by the caller in the *pData* parameter is completely full.
* The connection has been closed.  
* The request has been canceled or an error occurred.  

This flag is not supported on datagram sockets or on message-oriented connectionless sockets.

### -param RequestContext

The request context to associate with this receive operation.

## -returns

If no error occurs, the **RIOReceiveEx** function returns **TRUE**. In this case, the receive operation is successfully initiated and the completion will have already been queued or the operation has been successfully initiated and the completion will be queued at a later time.

A value of **FALSE** indicates the function failed, the operation was not successfully initiated and no completion indication will be queued. A specific error code can be retrieved by calling the [**WSAGetLastError**](../winsock/nf-winsock-wsagetlasterror.md) function.

| Return code | Description |
|--|--|
| **[WSAEFAULT](/windows/win32/winsock/windows-sockets-error-codes-2#wsaefault)** | The system detected an invalid pointer address in attempting to use a pointer argument in a call. This error is returned if a buffer identifier is deregistered or a buffer is freed for any of the [**RIO\_BUF**](../mswsockdef/ns-mswsockdef-rio_buf.md) structures passed in parameters before the operation is queued or invoked. |
| **[WSAEINVAL](/windows/win32/winsock/windows-sockets-error-codes-2#wsaeinval)** | An invalid parameter was passed to the function. <br/> This error is returned if the *SocketQueue* parameter is not valid, the *dwFlags* parameter contains a value not valid for a receive operation, or the integrity of the completion queue has been compromised. This error can also be returned for other issues with parameters. |
| **[WSAENOBUFS](/windows/win32/winsock/windows-sockets-error-codes-2#wsaenobufs)** | Sufficient memory could not be allocated. This error is returned if the I/O completion queue associated with the *SocketQueue* parameter is full or the I/O completion queue was created with zero receive entries. |
| **[WSA\_OPERATION\_ABORTED](/windows/win32/winsock/windows-sockets-error-codes-2#wsa-operation-aborted)** | The operation has been canceled while the receive operation was pending. This error is returned if the socket is closed locally or remotely, or the SIO\_FLUSH command in [**WSAIoctl**](../winsock2/nf-winsock2-wsaioctl.md) is executed. |

## -remarks

An application can use the **RIOReceiveEx** function to receive network data into any buffer completely contained within a single registered buffer. The **Offset** and **Length** members of the [**RIO\_BUF**](../mswsockdef/ns-mswsockdef-rio_buf.md) structure pointed to by the *pData* parameter determine where the network data is received in the buffer.

Once the **RIOReceiveEx** function is called, the buffer passed in the *pData* parameter including the [**RIO\_BUFFERID**](/windows/win32/winsock/rio-bufferid) in the **BufferId** member of [**RIO\_BUF**](../mswsockdef/ns-mswsockdef-rio_buf.md) structure must remain valid for the duration of the receive operation.

In order to avoid race conditions, a buffer associated with a receive request should not be read or written before the request completes. This includes using the buffer as the source for a send request or the destination for another receive request. Portions of a registered buffer not associated with any receive request are not included in this restriction.

The *pLocalAddress* parameter can be used to retrieve the local address where the data was received. The *pRemoteAddress* parameter can be used to retrieve the remote address from which the data was received. The local and remote addresses are returned as [**SOCKADDR\_INET**](../ws2ipdef/ns-ws2ipdef-sockaddr_inet.md) structures. As a result, the **Length** member of the [**RIO\_BUF**](../mswsockdef/ns-mswsockdef-rio_buf.md) pointed to by *pLocalAddress* or *pRemoteAddress* parameters should be equal or greater than the size of a **SOCKADDR\_INET** structure.

The following table summarizes the various uses of control data available for use with the control information in the *pControlContext* member.

| Protocol | cmsg\_level | cmsg\_type | Description |
|--|--|--|--|
| IPv4 | IPPROTO\_IP | IP\_ORIGINAL\_ARRIVAL\_IF | Receives the original IPv4 arrival interface where the packet was received for datagram sockets. This control data is used by firewalls when a Teredo, 6to4, or ISATAP tunnel is used for IPv4 NAT traversal.<br/> The cmsg\_data\[\] member is a ULONG that contains the IF\_INDEX defined in the *ifdef.h* header file.<br/> For more information, see the [IPPROTO_IP Socket Options](/windows/win32/winsock/ipproto-ip-socket-options) for the IP\_ORIGINAL\_ARRIVAL\_IF socket option. |
| IPv4 | IPPROTO\_IP   | IP\_PKTINFO | Specifies/receives packet information.<br/> For more information, see the [IPPROTO_IP Socket Options](/windows/win32/winsock/ipproto-ip-socket-options) for the IP\_PKTINFO socket option. |
| IPv6 | IPPROTO\_IPV6 | IPV6\_DSTOPTS | Specifies/receives destination options. |
| IPv6 | IPPROTO\_IPV6 | IPV6\_HOPLIMIT | Specifies/receives hop limit.<br/> For more information, see the [**IPPROTO\_IPV6 Socket Options**](/windows/win32/winsock/ipproto-ipv6-socket-options) for the IPV6\_HOPLIMIT socket option. |
| IPv6 | IPPROTO\_IPV6 | IPV6\_HOPOPTS | Specifies/receives hop-by-hop options. |
| IPv6 | IPPROTO\_IPV6 | IPV6\_NEXTHOP | Specifies next-hop address. |
| IPv6 | IPPROTO\_IPV6 | IPV6\_PKTINFO | Specifies/receives packet information.<br/> For more information, see the [**IPPROTO\_IPV6 Socket Options**](/windows/win32/winsock/ipproto-ipv6-socket-options) for the IPV6\_PKTINFO socket option. |
| IPv6 | IPPROTO\_IPV6 | IPV6\_RTHDR | Specifies/receives routing header. |

Control data is made up of one or more control data objects, each beginning with a **WSACMSGHDR** structure, defined as the following:

```C++
} WSACMSGHDR;
```

The members of the **WSACMSGHDR** structure are as follows:

| Term | Description |
|--|--|
| <span id="cmsg_len"></span><span id="CMSG_LEN"></span>cmsg\_len | The number of bytes of data starting from the beginning of the **WSACMSGHDR** to the end of data (excluding padding bytes that may follow data). |
| <span id="cmsg_level"></span><span id="CMSG_LEVEL"></span>cmsg\_level | The protocol that originated the control information. |
| <span id="cmsg_type"></span><span id="CMSG_TYPE"></span>cmsg\_type | The protocol-specific type of control information. |

The *Flags* parameter can be used to influence the behavior of the **RIOReceiveEx** function invocation beyond the options specified for the associated socket. The behavior of this function is determined by a combination of any socket options set on the socket associated with the *SocketQueue* parameter and the values specified in the *Flags* parameter.

> [!NOTE]  
> The function pointer to the **RIOReceiveEx** function must be obtained at run time by making a call to the [**WSAIoctl**](../winsock2/nf-winsock2-wsaioctl.md) function with the **SIO\_GET\_MULTIPLE\_EXTENSION\_FUNCTION\_POINTER** opcode specified. The input buffer passed to the **WSAIoctl** function must contain **WSAID\_MULTIPLE\_RIO**, a globally unique identifier (GUID) whose value identifies the Winsock registered I/O extension functions. On success, the output returned by the **WSAIoctl** function contains a pointer to the [**RIO\_EXTENSION\_FUNCTION\_TABLE**](./ns-mswsock-rio_extension_function_table.md) structure that contains pointers to the Winsock registered I/O extension functions. The **SIO\_GET\_MULTIPLE\_EXTENSION\_FUNCTION\_POINTER** IOCTL is defined in the *Ws2def.h* header file. The **WSAID\_MULTIPLE\_RIO** GUID is defined in the *Mswsock.h* header file.

**Windows Phone 8:** This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

**Windows 8.1** and **Windows Server 2012 R2**: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also
