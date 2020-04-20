---
UID: NC:mswsock.LPFN_RIORECEIVE
title: LPFN_RIORECEIVE
description: Receives network data on a connected registered I/O TCP socket or a bound registered I/O UDP socket for use with the Winsock registered I/O extensions.helpviewer_keywords: ["LPFN_RIORECEIVE"]
old-location: 
tech.root: WinSock
ms.assetid: 26726277-4907-47A1-BACF-868389B46EA8
ms.date: 01/30/19
ms.keywords: LPFN_RIORECEIVE
f1_keywords:
- mswsock/LPFN_RIORECEIVE
dev_langs:
- c++
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
topic_type:
- apiref
api_type:
- LibDef
api_location:
- mswsock.h
api_name:
- LPFN_RIORECEIVE
---

## -description

The **RIOReceive** function receives network data on a connected registered I/O TCP socket or a bound registered I/O UDP socket for use with the Winsock registered I/O extensions.

## -parameters

### -param SocketQueue

A descriptor that identifies a connected registered I/O TCP socket or a bound registered I/O UDP socket.

### -param pData

A description of the portion of the registered buffer in which to receive data.

This parameter may be NULL for a bound registered I/O UDP socket if the application does not need to receive the data payload in the UDP datagram.


### -param DataBufferCount

A data buffer count parameter that indicates if data is to be received in the buffer pointed to by the *pData* parameter.

This parameter should be set to zero if the *pData* is NULL. Otherwise, this parameter should be set to 1.


### -param Flags

A set of flags that modify the behavior of the **RIOReceive** function.

The *Flags* parameter can contain a combination of the following options defined in the *Mswsockdef.h* header file:



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Flag</th><th>Meaning</th></tr></thead><tbody><tr class="odd"><td><span id="RIO_MSG_COMMIT_ONLY"></span><span id="rio_msg_commit_only"></span><dl> <dt><strong>RIO_MSG_COMMIT_ONLY</strong></dt> </dl></td><td>Previous requests added with <strong>RIO_MSG_DEFER</strong> flag will be committed. <br/> When the <strong>RIO_MSG_COMMIT_ONLY</strong> flag is set, no other flags may be specified. When the <strong>RIO_MSG_COMMIT_ONLY</strong> flag is set, the <em>pData</em> and <em>RequestContext</em> parameters must be NULL and the <em>DataBufferCount</em> parameter must be zero. <br/> This flag would normally be used occasionally after a number of requests were issued with the <strong>RIO_MSG_DEFER</strong> flag set. This eliminates the need when using the <strong>RIO_MSG_DEFER</strong> flag to make the last request without the <strong>RIO_MSG_DEFER</strong> flag, which causes the last request to complete much slower than other requests. <br/> Unlike other calls to the <strong>RIOReceive</strong> function, when the <strong>RIO_MSG_COMMIT_ONLY</strong> flag is set calls to the <strong>RIOReceive</strong> function do not need to be serialized. For a single [<strong>RIO_RQ</strong>](/windows/win32/winsock/riorqueue), the <strong>RIOReceive</strong> function can be called with <strong>RIO_MSG_COMMIT_ONLY</strong> on one thread while calling the <strong>RIOReceive</strong> function on another thread.<br/></td></tr><tr class="even"><td><span id="RIO_MSG_DONT_NOTIFY"></span><span id="rio_msg_dont_notify"></span><dl> <dt><strong>RIO_MSG_DONT_NOTIFY</strong></dt> </dl></td><td>The request should not trigger the [<strong>RIONotify</strong>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) function when request completion is inserted into its completion queue.<br/></td></tr><tr class="odd"><td><span id="RIO_MSG_DEFER"></span><span id="rio_msg_defer"></span><dl> <dt><strong>RIO_MSG_DEFER</strong></dt> </dl></td><td>The request does not need to be executed immediately. This will insert the request into the request queue, but it may or may not trigger the execution of the request. <br/> Data reception may be delayed until a receive request is made on the [<strong>RIO_RQ</strong>](/windows/win32/winsock/riorqueue) passed in the <em>SocketQueue</em> parameter without the <strong>RIO_MSG_DEFER</strong> flag set. To trigger execution for all receives in a request queue, call the <strong>RIOReceive</strong> or [<strong>RIOReceiveEx</strong>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex) function without the <strong>RIO_MSG_DEFER</strong> flag set. <br/><blockquote>[!Note]<br />
The receive request is charged against the outstanding I/O capacity on the [<strong>RIO_RQ</strong>](/windows/win32/winsock/riorqueue) passed in the <em>SocketQueue</em> parameter regardless of whether <strong>RIO_MSG_DEFER</strong> is set.</blockquote><br/></td></tr><tr class="even"><td><span id="RIO_MSG_WAITALL"></span><span id="rio_msg_waitall"></span><dl> <dt><strong>RIO_MSG_WAITALL</strong></dt> </dl></td><td>The <strong>RIOReceive</strong> function will not complete until one of the following events occurs:<br/><ul><li>The buffer segment supplied by the caller in the <em>pData</em> parameter is completely full.</li><li>The connection has been closed.</li><li>The request has been canceled or an error occurred.</li></ul><br/> This flag is not supported on UDP sockets.<br/></td></tr></tbody></table>




### -param RequestContext

The request context to associate with this receive operation.

## -returns

If no error occurs, the **RIOReceive** function returns **TRUE**. In this case, the receive operation is successfully initiated and the completion will have already been queued or the operation has been successfully initiated and the completion will be queued at a later time.

A value of **FALSE** indicates the function failed, the operation was not successfully initiated and no completion indication will be queued. A specific error code can be retrieved by calling the [**WSAGetLastError**](/windows/win32/api/winsock/nf-winsock-wsagetlasterror) function.



| Return code                                                                                                                                                       | Description                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**[WSAEFAULT](/windows/win32/winsock/windows-sockets-error-codes-2#wsaefault)**</dt> </dl>                           | The system detected an invalid pointer address in attempting to use a pointer argument in a call. This error is returned if a buffer identifier is deregistered or a buffer is freed for any of the [**RIO\_BUF**](/windows/win32/api/mswsockdef/ns-mswsockdef-rio_buf) structures passed in parameters before the operation is queued or invoked.<br/>                                   |
| <dl> <dt>**[WSAEINVAL](/windows/win32/winsock/windows-sockets-error-codes-2#wsaeinval)**</dt> </dl>                           | An invalid parameter was passed to the function. <br/> This error is returned if the *SocketQueue* parameter is not valid, the *Flags* parameter contains an value not valid for a receive operation, or the integrity of the completion queue has been compromised. This error can also be returned for other issues with parameters.<br/> |
| <dl> <dt>**[WSAENOBUFS](/windows/win32/winsock/windows-sockets-error-codes-2#wsaenobufs)**</dt> </dl>                         | Sufficient memory could not be allocated. This error is returned if the I/O completion queue associated with the *SocketQueue* parameter is full or the I/O completion queue was created with zero receive entries.<br/>                                                                                                                          |
| <dl> <dt>**[WSA\_OPERATION\_ABORTED](/windows/win32/winsock/windows-sockets-error-codes-2#wsa-operation-aborted)**</dt> </dl> | The operation has been canceled while the receive operation was pending. This error is returned if the socket is closed locally or remotely, or the **SIO\_FLUSH** command in [**WSAIoctl**](/windows/win32/api/winsock2/nf-winsock2-wsaioctl) is executed on this socket.<br/>                                                                                                     |




## -remarks

An application can use the **RIOReceive** function to receive network data into any buffer completely contained within a single registered buffer. The **Offset** and **Length** members of the [**RIO\_BUF**](/windows/win32/api/mswsockdef/ns-mswsockdef-rio_buf) structure pointed to by the *pData* parameter determine where the network data is received in the buffer.

Once the **RIOReceive** function is called, the buffer passed in the *pData* parameter including the [**RIO\_BUFFERID**](/windows/win32/winsock/rio-bufferid) in the **BufferId** member of [**RIO\_BUF**](/windows/win32/api/mswsockdef/ns-mswsockdef-rio_buf) structure must remain valid for the duration of the receive operation.

In order to avoid race conditions, a buffer associated with a receive request should not be read or written before the request completes. This includes using the buffer as the source for a send request or the destination for another receive request. Portions of a registered buffer not associated with any receive request are not included in this restriction.

The *Flags* parameter can be used to influence the behavior of the **RIOReceive** function invocation beyond the options specified for the associated socket. The behavior of this function is determined by a combination of any socket options set on the socket associated with the *SocketQueue* parameter and the values specified in the *Flags* parameter.

> [!Note]  
> The function pointer to the **RIOReceive** function must be obtained at run time by making a call to the [**WSAIoctl**](/windows/win32/api/winsock2/nf-winsock2-wsaioctl) function with the **SIO\_GET\_MULTIPLE\_EXTENSION\_FUNCTION\_POINTER** opcode specified. The input buffer passed to the **WSAIoctl** function must contain **WSAID\_MULTIPLE\_RIO**, a globally unique identifier (GUID) whose value identifies the Winsock registered I/O extension functions. On success, the output returned by the **WSAIoctl** function contains a pointer to the [**RIO\_EXTENSION\_FUNCTION\_TABLE**](/windows/win32/api/mswsock/ns-mswsock-rio_extension_function_table) structure that contains pointers to the Winsock registered I/O extension functions. The **SIO\_GET\_MULTIPLE\_EXTENSION\_FUNCTION\_POINTER** IOCTL is defined in the *Ws2def.h* header file. The **WSAID\_MULTIPLE\_RIO** GUID is defined in the *Mswsock.h* header file.

 

**Windows Phone 8:** This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

**Windows 8.1** and **Windows Server 2012 R2**: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

