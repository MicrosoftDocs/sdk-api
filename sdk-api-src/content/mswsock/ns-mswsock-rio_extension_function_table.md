---
UID: NS:mswsock._RIO_EXTENSION_FUNCTION_TABLE
title: RIO_EXTENSION_FUNCTION_TABLE (mswsock.h)
description: Contains information on the functions that implement the Winsock registered I/O extensions.
helpviewer_keywords: ["*PRIO_EXTENSION_FUNCTION_TABLE","PRIO_EXTENSION_FUNCTION_TABLE","PRIO_EXTENSION_FUNCTION_TABLE structure pointer [Winsock]","RIO_EXTENSION_FUNCTION_TABLE","RIO_EXTENSION_FUNCTION_TABLE structure [Winsock]","mswsockdef/PRIO_EXTENSION_FUNCTION_TABLE","mswsockdef/RIO_EXTENSION_FUNCTION_TABLE","winsock.rio_extension_function_table"]
old-location: winsock\rio_extension_function_table.htm
tech.root: WinSock
ms.assetid: 33C190B0-DE01-47A0-93AF-627FC5C5FF48
ms.date: 12/05/2018
ms.keywords: '*PRIO_EXTENSION_FUNCTION_TABLE, PRIO_EXTENSION_FUNCTION_TABLE, PRIO_EXTENSION_FUNCTION_TABLE structure pointer [Winsock], RIO_EXTENSION_FUNCTION_TABLE, RIO_EXTENSION_FUNCTION_TABLE structure [Winsock], mswsockdef/PRIO_EXTENSION_FUNCTION_TABLE, mswsockdef/RIO_EXTENSION_FUNCTION_TABLE, winsock.rio_extension_function_table'
req.header: mswsock.h
req.include-header: Mswsock.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: RIO_EXTENSION_FUNCTION_TABLE, *PRIO_EXTENSION_FUNCTION_TABLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RIO_EXTENSION_FUNCTION_TABLE
 - mswsock/_RIO_EXTENSION_FUNCTION_TABLE
 - PRIO_EXTENSION_FUNCTION_TABLE
 - mswsock/PRIO_EXTENSION_FUNCTION_TABLE
 - RIO_EXTENSION_FUNCTION_TABLE
 - mswsock/RIO_EXTENSION_FUNCTION_TABLE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mswsockdef.h
api_name:
 - RIO_EXTENSION_FUNCTION_TABLE
---

# RIO_EXTENSION_FUNCTION_TABLE structure


## -description

The <b>RIO_EXTENSION_FUNCTION_TABLE</b> structure contains information on the  functions that implement the Winsock registered I/O extensions.

## -struct-fields

### -field cbSize

The size, in bytes, of the structure.

### -field RIOReceive

A pointer to the <a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive">RIOReceive</a> function.

### -field RIOReceiveEx

A pointer to the <a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex">RIOReceiveEx</a> function.

### -field RIOSend

A pointer to the <a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend">RIOSend</a> function.

### -field RIOSendEx

A pointer to the <a href="/previous-versions/windows/desktop/legacy/hh437216(v=vs.85)">RIOSendEx</a> function.

### -field RIOCloseCompletionQueue

A pointer to the <a href="/previous-versions/windows/desktop/legacy/hh448837(v=vs.85)">RIOCloseCompletionQueue</a> function.

### -field RIOCreateCompletionQueue

A pointer to the <a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreatecompletionqueue">RIOCreateCompletionQueue</a> function.

### -field RIOCreateRequestQueue

A pointer to the <a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue">RIOCreateRequestQueue</a> function.

### -field RIODequeueCompletion

A pointer to the <a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion">RIODequeueCompletion</a> function.

### -field RIODeregisterBuffer

A pointer to the <a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer">RIODeregisterBuffer</a> function.

### -field RIONotify

A pointer to the <a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify">RIONotify</a> function.

### -field RIORegisterBuffer

A pointer to the <a href="/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)">RIORegisterBuffer</a> function.

### -field RIOResizeCompletionQueue

A pointer to the <a href="/previous-versions/windows/desktop/legacy/hh437202(v=vs.85)">RIOResizeCompletionQueue</a> function.

### -field RIOResizeRequestQueue

A pointer to the <a href="/previous-versions/windows/desktop/legacy/hh437204(v=vs.85)">RIOResizeRequestQueue</a> function.

## -remarks

The <b>RIO_EXTENSION_FUNCTION_TABLE</b> structure contains information on the  functions that implement the Winsock registered I/O extensions.

The function pointers for the 
Winsock registered I/O extension functions must be obtained at run time by making a call to the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a> function with the <b>SIO_GET_MULTIPLE_EXTENSION_FUNCTION_POINTER</b> opcode specified. The input buffer passed to the <b>WSAIoctl</b> function must contain <b>WSAID_MULTIPLE_RIO</b>, a globally unique identifier (GUID) whose value identifies the Winsock registered I/O  extension functions. On success, the output returned by the <b>WSAIoctl</b> function contains a pointer to the <b>RIO_EXTENSION_FUNCTION_TABLE</b> structure that contains pointers to the Winsock registered I/O  extension functions. The <b>SIO_GET_MULTIPLE_EXTENSION_FUNCTION_POINTER</b> IOCTL is defined in the <i>Ws2def.h</i> header file.The <b>WSAID_MULTIPLE_RIO</b> GUID is defined in the <i>Mswsock.h</i> header file.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/hh448837(v=vs.85)">RIOCloseCompletionQueue</a>



<a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreatecompletionqueue">RIOCreateCompletionQueue</a>



<a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue">RIOCreateRequestQueue</a>



<a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion">RIODequeueCompletion</a>



<a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer">RIODeregisterBuffer</a>



<a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify">RIONotify</a>



<a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive">RIOReceive</a>



<a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex">RIOReceiveEx</a>



<a href="/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)">RIORegisterBuffer</a>



<a href="/previous-versions/windows/desktop/legacy/hh437202(v=vs.85)">RIOResizeCompletionQueue</a>



<a href="/previous-versions/windows/desktop/legacy/hh437204(v=vs.85)">RIOResizeRequestQueue</a>



<a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend">RIOSend</a>



<a href="/previous-versions/windows/desktop/legacy/hh437216(v=vs.85)">RIOSendEx</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a>