---
UID: NC:mswsock.LPFN_RIOREGISTERBUFFER
title: LPFN_RIOREGISTERBUFFER
description: Registers a RIO\_BUFFERID, a registered buffer descriptor, with a specified buffer for use with the Winsock registered I/O extensions.
helpviewer_keywords: ["LPFN_RIOREGISTERBUFFER"]
old-location: 
tech.root: WinSock
ms.assetid: CAADCC2F-1443-410F-A860-375C9AAE208E
ms.date: 01/30/2019
ms.keywords: LPFN_RIOREGISTERBUFFER
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
 - LPFN_RIOREGISTERBUFFER
 - mswsock/LPFN_RIOREGISTERBUFFER
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - mswsock.h
api_name:
 - LPFN_RIOREGISTERBUFFER
---

## -description

The **RIORegisterBuffer** function registers a [**RIO\_BUFFERID**](/windows/win32/winsock/rio-bufferid), a registered buffer descriptor, with a specified buffer for use with the Winsock registered I/O extensions.

## -parameters

### -param DataBuffer

A pointer to the beginning of the memory buffer to register.

### -param DataLength

The length, in bytes, in the buffer to register.

## -returns

If no error occurs, the **RIORegisterBuffer** function returns a registered buffer descriptor. Otherwise, a value of **RIO\_INVALID\_BUFFERID** is returned, and a specific error code can be retrieved by calling the [**WSAGetLastError**](../winsock/nf-winsock-wsagetlasterror.md) function.



| Return code                                                                                                                             | Description                                                                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**[WSAEFAULT](/windows/win32/winsock/windows-sockets-error-codes-2#wsaefault)**</dt> </dl> | The system detected an invalid pointer address in attempting to use a pointer argument in a call. This error is returned if an invalid buffer pointer is passed in *DataBuffer* parameter.<br/> |
| <dl> <dt>**[WSAEINVAL](/windows/win32/winsock/windows-sockets-error-codes-2#wsaeinval)**</dt> </dl> | An invalid parameter was passed to the function. <br/> This error is returned if the *DataLength* parameter is zero.<br/>                                                                 |

## -remarks

The **RIORegisterBuffer** function creates a registered buffer identifier for a specified buffer. When a buffer is registered, the virtual memory pages containing the buffer will be locked into physical memory.

If several small, non-contiguous buffers are registered, the physical memory footprint for the buffers may effectively be as large as an entire memory page per registration. In these cases it may be beneficial to allocate multiple request buffers together.

There is also a small amount of overhead in physical memory used for the buffer registration itself. So if there are many allocations aggregated into single larger allocation, the physical memory footprint may be reduced further by aggregating the buffer registrations as well. In this case the application may need to take extra care to ensure that the buffers are eventually deregistered, but not while any send or receive requests are outstanding.

A portion of a registered buffer is passed to the [**RIOSend**](./nc-mswsock-lpfn_riosend.md), [**RIOSendEx**](./nc-mswsock-lpfn_riosendex.md), [**RIOReceive**](./nc-mswsock-lpfn_rioreceive.md), and [**RIOReceiveEx**](./nc-mswsock-lpfn_rioreceiveex.md) functions in the *pData* parameter for sending or receiving data.

When the buffer identifier is no longer needed, call the [**RIODeregisterBuffer**](./nc-mswsock-lpfn_rioderegisterbuffer.md) function to deregister the buffer identifier.

> [!Note]  
> The function pointer to the **RIORegisterBuffer** function must be obtained at run time by making a call to the [**WSAIoctl**](../winsock2/nf-winsock2-wsaioctl.md) function with the **SIO\_GET\_MULTIPLE\_EXTENSION\_FUNCTION\_POINTER** opcode specified. The input buffer passed to the **WSAIoctl** function must contain **WSAID\_MULTIPLE\_RIO**, a globally unique identifier (GUID) whose value identifies the Winsock registered I/O extension functions. On success, the output returned by the **WSAIoctl** function contains a pointer to the [**RIO\_EXTENSION\_FUNCTION\_TABLE**](./ns-mswsock-rio_extension_function_table.md) structure that contains pointers to the Winsock registered I/O extension functions. The **SIO\_GET\_MULTIPLE\_EXTENSION\_FUNCTION\_POINTER** IOCTL is defined in the *Ws2def.h* header file. The **WSAID\_MULTIPLE\_RIO** GUID is defined in the *Mswsock.h* header file.

 

**Windows Phone 8:** This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

**Windows 8.1** and **Windows Server 2012 R2**: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also