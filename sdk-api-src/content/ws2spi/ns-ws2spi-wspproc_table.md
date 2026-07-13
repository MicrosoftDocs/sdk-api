---
UID: NS:ws2spi._WSPPROC_TABLE
title: WSPPROC_TABLE
description: Contains a table of pointers to service provider functions.
tech.root: winsock
helpviewer_keywords: ["_WSPPROC_TABLE","WSPPROC_TABLE"]
ms.date: 4/26/2019
ms.keywords: _WSPPROC_TABLE, WSPPROC_TABLE
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: ws2spi.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.target-type: 
req.typenames: WSPPROC_TABLE, *LPWSPPROC_TABLE
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - ws2spi.h
api_name:
 - _WSPPROC_TABLE
 - WSPPROC_TABLE
f1_keywords:
 - _WSPPROC_TABLE
 - ws2spi/_WSPPROC_TABLE
 - LPWSPPROC_TABLE
 - ws2spi/LPWSPPROC_TABLE
 - WSPPROC_TABLE
 - ws2spi/WSPPROC_TABLE
---

## -description

The **WSPPROC_TABLE** structure contains a table of pointers to service provider functions.

## -struct-fields

```C++
} WSPPROC_TABLE, FAR * LPWSPPROC_TABLE;
```

### -field lpWSPAccept

A pointer to the **[LPWSPAccept](nc-ws2spi-lpwspaccept.md)** function.

### -field lpWSPAddressToString

A pointer to the [**LPWSPAddressToString**](nc-ws2spi-lpwspaddresstostring.md) function.

### -field lpWSPAsyncSelect

A pointer to the **[LPWSPAsyncSelect](nc-ws2spi-lpwspasyncselect.md)** function.

### -field lpWSPBind

A pointer to the <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspbind">LPWSPBind</a></b> function.

### -field lpWSPCancelBlockingCall

A pointer to the <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspcancelblockingcall">LPWSPCancelBlockingCall</a></b> function.

### -field lpWSPCleanup

 

A pointer to the [**WSPCleanup**](./nc-ws2spi-lpwspcleanup.md) function.

### -field lpWSPCloseSocket

 

A pointer to the <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspclosesocket">LPWSPCloseSocket</a></b> function.

### -field lpWSPConnect

 

A pointer to the <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspconnect">LPWSPConnect</a></b> function.

### -field lpWSPDuplicateSocket

 

A pointer to the [**WSPDuplicateSocket**](./nc-ws2spi-lpwspduplicatesocket.md) function.

### -field lpWSPEnumNetworkEvents

 
A pointer to the [**WSPEnumNetworkEvents**](./nc-ws2spi-lpwspenumnetworkevents.md) function.

### -field lpWSPEventSelect

 

A pointer to the [**LPWSPEventSelect**](./nc-ws2spi-lpwspenumnetworkevents.md) function.

### -field lpWSPGetOverlappedResult

 

A pointer to the [**LPWSPGetOverlappedResult**](./nc-ws2spi-lpwspgetoverlappedresult.md) function.

### -field lpWSPGetPeerName

A pointer to the    function.

### -field lpWSPGetSockName

A pointer to the [**WSPGetSockName**](./nc-ws2spi-lpwspgetsockname.md) function.

### -field lpWSPGetSockOpt

A pointer to the <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspgetsockopt">LPWSPGetSockopt</a></b> function.

### -field lpWSPGetQOSByName

 

A pointer to the [**WSPGetQOSByName**](./nc-ws2spi-lpwspgetqosbyname.md) function.

### -field lpWSPIoctl

 

A pointer to the <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspioctl">LPWSPIoctl</a></b> function.

### -field lpWSPJoinLeaf

 

A pointer to the <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspjoinleaf">LPWSPJoinLeaf</a></b> function.

### -field lpWSPListen

 

A pointer to the <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwsplisten">LPWSPListen</a></b> function.

### -field lpWSPRecv

 

A pointer to the <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwsprecv">LPWSPRecv</a></b> function.

### -field lpWSPRecvDisconnect

 

A pointer to the [**WSPRecvDisconnect**](./nc-ws2spi-lpwsprecvdisconnect.md) function.

### -field lpWSPRecvFrom

 

A pointer to the <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwsprecvfrom">LPWSPRecvFrom</a></b> function.

### -field lpWSPSelect

 

A pointer to the [**LPWSPSelect**](./nc-ws2spi-lpwspselect.md) function.

### -field lpWSPSend

 

A pointer to the <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsend">LPWSPSend</a></b> function.

### -field lpWSPSendDisconnect

 

A pointer to the [**WSPSendDisconnect**](./nc-ws2spi-lpwspsenddisconnect.md) function.

### -field lpWSPSendTo

 

A pointer to the <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsendto">LPWSPSendTo</a></b> function.

### -field lpWSPSetSockOpt

 

A pointer to the <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsetsockopt">LPWSPSetSockOpt</a></b> function.

### -field lpWSPShutdown

 

A pointer to the <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspshutdown">LPWSPShutdown</a></b> function.

### -field lpWSPSocket

 

A pointer to the <a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsocket">LPWSPSocket</a> function.

### -field lpWSPStringToAddress

 

A pointer to the <a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspstringtoaddress">LPWSPStringToAddress</a> function.

## -remarks

The **WSPPROC_TABLE** structure contains a table of pointers to service provider functions that are returned by the <a href="/windows/win32/api/ws2spi/nf-ws2spi-wspstartup">WSPStartup</a> function.

## -see-also

**[LPWSPAccept](nc-ws2spi-lpwspaccept.md)**


<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspstringtoaddress">LPWSPStringToAddress</a>**


**[LPWSPAsyncSelect](nc-ws2spi-lpwspasyncselect.md)**

<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspbind">LPWSPBind</a></b>

<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspcancelblockingcall">LPWSPCancelBlockingCall</a></b>

<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspcleanup">LPWSPCleanup</a></b>

<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspclosesocket">LPWSPCloseSocket</a></b>

<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspconnect">LPWSPConnect</a></b>

<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspduplicatesocket">LPWSPDuplicateSocket</a></b>

<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspenumnetworkevents">LPWSPEnumNetworkEvents</a></b>

<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspgetoverlappedresult">LPWSPGetOverlappedResult</a></b>

<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspgetqosbyname">LPWSPGetQOSByName</a></b>

<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspgetsockname">LPWSPGetSockName</a></b>

<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspgetsockopt">LPWSPGetSockopt</a></b>

<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspioctl">LPWSPIoctl</a></b>

<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspjoinleaf">LPWSPJoinLeaf</a></b>

<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwsplisten">LPWSPListen</a></b>

<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwsprecv">LPWSPRecv</a></b>

<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwsprecvdisconnect">LPWSPRecvDisconnect</a></b>

<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwsprecvfrom">LPWSPRecvFrom</a></b>

<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsend">LPWSPSend</a></b>

<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsenddisconnect">LPWSPSendDisconnect</a></b>

<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsendto">LPWSPSendTo</a></b>

<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsetsockopt">LPWSPSetSockOpt</a></b>

<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspshutdown">LPWSPShutdown</a></b>

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsocket">LPWSPSocket</a>

<a href="/windows/win32/api/ws2spi/nf-ws2spi-wspstartup">WSPStartup</a>

<a href=" /windows/win32/api/winsock2/nf-winsock2-wsastringtoaddressa">WSAStringToAddress</a>