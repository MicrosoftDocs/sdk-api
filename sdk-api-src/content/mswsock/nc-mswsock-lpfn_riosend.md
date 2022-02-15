---
UID: NC:mswsock.LPFN_RIOSEND
title: LPFN_RIOSEND
description: Sends network data on a connected registered I/O TCP socket or a bound registered I/O UDP socket for use with the Winsock registered I/O extensions.
helpviewer_keywords: ["LPFN_RIOSEND"]
old-location: 
tech.root: WinSock
ms.assetid: A1CE9224-1E8C-46F8-AD7B-DBCBEBC670F7
ms.date: 01/30/2019
ms.keywords: LPFN_RIOSEND
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
 - LPFN_RIOSEND
 - mswsock/LPFN_RIOSEND
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - mswsock.h
api_name:
 - LPFN_RIOSEND
---

## -description

The **RIOSend** function sends network data on a connected registered I/O TCP socket or a bound registered I/O UDP socket for use with the Winsock registered I/O extensions.

## -parameters

### -param SocketQueue

A descriptor that identifies a connected registered I/O TCP socket or a bound registered I/O UDP socket.

### -param pData

A description of the portion of the registered buffer from which to send data.

This parameter may be NULL for a bound registered I/O UDP socket if the application does not need to send a data payload in the UDP datagram.

### -param DataBufferCount

A data buffer count parameter that indicates if data is to be sent in the buffer pointed to by the *pData* parameter.

This parameter should be set to zero if the *pData* is NULL. Otherwise, this parameter should be set to 1.

### -param Flags

A set of flags that modify the behavior of the **RIOSend** function.

The *Flags* parameter can contain a combination of the following options defined in the *Mswsockdef.h* header file:



<table><colgroup><col /><col /></colgroup><thead><tr> and <em>RequestContext</em> parameters must be NULL and the <em>DataBufferCount</em> parameter must be zero. <br/> This flag would normally be used occasionally after a number of requests were issued with the <strong>RIO_MSG_DEFER</strong> flag set. This eliminates the need when using the <strong>RIO_MSG_DEFER</strong> flag to make the last request without the <strong>RIO_MSG_DEFER</strong> flag, which causes the last request to complete much slower than other requests. <br/> Unlike other calls to the <strong>RIOSend</strong> function, when the <strong>RIO_MSG_COMMIT_ONLY</strong> flag is set calls to the <strong>RIOSend</strong> function do not need to be serialized. For a single [<strong>RIO_RQ</strong>](/windows/win32/winsock/riorqueue), the <strong>RIOSend</strong> function can be called with <strong>RIO_MSG_COMMIT_ONLY</strong> on one thread while calling the <strong>RIOSend</strong> function on another thread.<br/></td></tr><tr>RIO_RQ</strong>](/windows/win32/winsock/riorqueue) passed in the <em>SocketQueue</em> parameter without the <strong>RIO_MSG_DEFER</strong> flag set. To trigger execution for all sends in a send queue, call the <strong>RIOSend</strong> or [<strong>RIOSendEx</strong>](./nc-mswsock-lpfn_riosendex.md) function without the <strong>RIO_MSG_DEFER</strong> flag set. <br/><blockquote>[!Note]<br />
The send request is charged against the outstanding I/O capacity on the [<strong>RIO_RQ</strong>](/windows/win32/winsock/riorqueue) passed in the <em>SocketQueue</em> parameter regardless of whether <strong>RIO_MSG_DEFER</strong> is set.</blockquote><br/></td></tr></tbody></table>

### -param RequestContext

The request context to associate with this send operation.

## -returns

If no error occurs, the **RIOSend** function returns **TRUE**. In this case, the send operation is successfully initiated and the completion will have already been queued or the operation has been successfully initiated and the completion will be queued at a later time.

A value of **FALSE** indicates the function failed, the operation was not successfully initiated and no completion indication will be queued. A specific error code can be retrieved by calling the [**WSAGetLastError**](../winsock/nf-winsock-wsagetlasterror.md) function.



| Return code                                                                                                                                         | Description                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**[WSAEFAULT](/windows/win32/winsock/windows-sockets-error-codes-2#wsaefault)**</dt> </dl>             | The system detected an invalid pointer address in attempting to use a pointer argument in a call. This error is returned if a buffer identifier is deregistered or a buffer is freed for any of the [**RIO\_BUF**](../mswsockdef/ns-mswsockdef-rio_buf.md) structures passed in parameters before the operation is queued or invoked.<br/>                                |
| <dl> <dt>**[WSAEINVAL](/windows/win32/winsock/windows-sockets-error-codes-2#wsaeinval)**</dt> </dl>             | An invalid parameter was passed to the function. <br/> This error is returned if the *SocketQueue* parameter is not valid, the *Flags* parameter contains a value not valid for a send operation, or the integrity of the completion queue has been compromised. This error can also be returned for other issues with parameters.<br/> |
| <dl> <dt>**[WSAENOBUFS](/windows/win32/winsock/windows-sockets-error-codes-2#wsaenobufs)**</dt> </dl>           | Sufficient memory could not be allocated. This error is returned if the I/O completion queue associated with the *SocketQueue* parameter is full or the I/O completion queue was created with zero send entries.<br/>                                                                                                                          |
| <dl> <dt>**[WSA\_IO\_PENDING](/windows/win32/winsock/windows-sockets-error-codes-2#wsa-io-pending)**</dt> </dl> | The operation has been successfully initiated and the completion will be queued at a later time.<br/>                                                                                                                                                                                                                                          |

## -remarks

An application can use the **RIOSend** function to send network data from any buffer completely contained within a single registered buffer. The **Offset** and **Length** members of the [**RIO\_BUF**](../mswsockdef/ns-mswsockdef-rio_buf.md) structure pointed to by the *pData* parameter determine the network data to be sent from the buffer.

The buffer associated with a send operation must not be used concurrently with another send or receive operation. The buffer, and buffer registration, must remain valid for the duration of a send operation. This means that you should not pass the same PRIO\_BUF to a RIOSend(Ex) request when one is already pending. Only after an in-flight RIOSend(Ex) request is complete should you re-use the same PRIO\_BUF (either with the same offset or with a different offset and length). Furthermore, when send data references a registered buffer (either a portion or the entire buffer), the entire registered buffer must not be used until the send has completed. This includes using a portion of the registered buffer for a receive operation or another send operation.

The *Flags* parameter can be used to influence the behavior of the **RIOSend** function beyond the options specified for the associated socket. The behavior of this function is determined by a combination of any socket options set on the socket associated with the *SocketQueue* parameter and the values specified in the *Flags* parameter.

> [!Note]  
> The function pointer to the **RIOSend** function must be obtained at run time by making a call to the [**WSAIoctl**](../winsock2/nf-winsock2-wsaioctl.md) function with the **SIO\_GET\_MULTIPLE\_EXTENSION\_FUNCTION\_POINTER** opcode specified. The input buffer passed to the **WSAIoctl** function must contain **WSAID\_MULTIPLE\_RIO**, a globally unique identifier (GUID) whose value identifies the Winsock registered I/O extension functions. On success, the output returned by the **WSAIoctl** function contains a pointer to the [**RIO\_EXTENSION\_FUNCTION\_TABLE**](./ns-mswsock-rio_extension_function_table.md) structure that contains pointers to the Winsock registered I/O extension functions. The **SIO\_GET\_MULTIPLE\_EXTENSION\_FUNCTION\_POINTER** IOCTL is defined in the *Ws2def.h* header file. The **WSAID\_MULTIPLE\_RIO** GUID is defined in the *Mswsock.h* header file.

 

**Windows Phone 8:** This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

**Windows 8.1** and **Windows Server 2012 R2**: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also