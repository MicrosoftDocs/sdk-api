---
UID: NC:mswsock.LPFN_RIODEREGISTERBUFFER
title: LPFN_RIODEREGISTERBUFFER
description: Deregisters a registered buffer used with the Winsock registered I/O extensions.
helpviewer_keywords: ["LPFN_RIODEREGISTERBUFFER"]
old-location: 
tech.root: WinSock
ms.assetid: 5D5C3469-0D5B-4E89-BE59-8D8AE9DBA5DE
ms.date: 01/30/2019
ms.keywords: LPFN_RIODEREGISTERBUFFER
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
 - LPFN_RIODEREGISTERBUFFER
 - mswsock/LPFN_RIODEREGISTERBUFFER
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - mswsock.h
api_name:
 - LPFN_RIODEREGISTERBUFFER
---

## -description

The **RIODeregisterBuffer** function deregisters a registered buffer used with the Winsock registered I/O extensions.

## -parameters

### -param BufferId

A descriptor identifying a registered buffer.

## -remarks

The **RIODeregisterBuffer** function deregisters a registered buffer. When a buffer is deregistered, the application is indicating that it is done with the buffer identifier passed in the *BufferId* parameter. Any subsequent calls to other functions that try to use this buffer identifier will fail.

If a buffer that is still in use is deregistered, the results are undefined. This is considered a serious error. In the [**RIORESULT**](../mswsockdef/ns-mswsockdef-rioresult.md) structure returned by the [**RIODequeueCompletion**](./nc-mswsock-lpfn_riodequeuecompletion.md) function, the status will be unchanged from the normal status. An application developer can detect this error condition using the Application Verifier tool.

If an invalid buffer identifier is passed in the *BufferId* parameter, this is ignored by the **RIODeregisterBuffer** function.

> [!Note]  
> The function pointer to the **RIODeregisterBuffer** function must be obtained at run time by making a call to the [**WSAIoctl**](../winsock2/nf-winsock2-wsaioctl.md) function with the **SIO\_GET\_MULTIPLE\_EXTENSION\_FUNCTION\_POINTER** opcode specified. The input buffer passed to the **WSAIoctl** function must contain **WSAID\_MULTIPLE\_RIO**, a globally unique identifier (GUID) whose value identifies the Winsock registered I/O extension functions. On success, the output returned by the **WSAIoctl** function contains a pointer to the [**RIO\_EXTENSION\_FUNCTION\_TABLE**](./ns-mswsock-rio_extension_function_table.md) structure that contains pointers to the Winsock registered I/O extension functions. The **SIO\_GET\_MULTIPLE\_EXTENSION\_FUNCTION\_POINTER** IOCTL is defined in the *Ws2def.h* header file. The **WSAID\_MULTIPLE\_RIO** GUID is defined in the *Mswsock.h* header file.

 

**Windows Phone 8:** This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

**Windows 8.1** and **Windows Server 2012 R2**: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also