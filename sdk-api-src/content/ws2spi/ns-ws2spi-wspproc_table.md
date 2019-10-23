---
UID: NS:ws2spi._WSPPROC_TABLE
title: WSPPROC_TABLE
description: Contains a table of pointers to service provider functions.
ms.date: 4/26/2019
ms.keywords: _WSPPROC_TABLE, WSPPROC_TABLE
ms.topic: language-reference
targetos: Windows
product: Windows
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
req.target-min-winversvr: Minimum supported server
Windows 2000 Server [desktop apps only]
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
---

## -description
The <b>WSPPROC_TABLE</b> structure contains a table of pointers to service provider functions.

## -struct-fields
```C++
} WSPPROC_TABLE, FAR * LPWSPPROC_TABLE;
```

### -field lpWSPAccept

A pointer to the <b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspaccept">LPWSPAccept</a></b> function.

### -field lpWSPAddressToString

A pointer to the [**WSPAddressToString**](wspaddresstostring-2.md) function.

### -field lpWSPAsyncSelect

A pointer to the <b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspasyncselect">LPWSPAsyncSelect</a><b> function.

### -field lpWSPBind

A pointer to the <b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspbind">LPWSPBind</a></b> function.

### -field lpWSPCancelBlockingCall


A pointer to the <b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspcancelblockingcall">LPWSPCancelBlockingCall</a></b> function.

### -field lpWSPCleanup

 

A pointer to the [**WSPCleanup**](wspcleanup-2.md) function.

### -field lpWSPCloseSocket

 

A pointer to the <b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspclosecoket">LPWSPCloseSocket</a></b> function.

### -field lpWSPConnect

 

A pointer to the <b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspconnect">LPWSPConnect</a></b> function.

### -field lpWSPDuplicateSocket

 

A pointer to the [**WSPDuplicateSocket**](wspduplicatesocket-2.md) function.

### -field lpWSPEnumNetworkEvents

 
A pointer to the [**WSPEnumNetworkEvents**](wspenumnetworkevents-2.md) function.

### -field lpWSPEventSelect

 

A pointer to the [<b>LPWSPEventSelect</b>](wspeventselect-2.md) function.

### -field lpWSPGetOverlappedResult

 

A pointer to the [<b>LPWSPGetOverlappedResult</b>](wspgetoverlappedresult-2.md) function.

### -field lpWSPGetPeerName

A pointer to the    function.


### -field lpWSPGetSockName

A pointer to the [**WSPGetSockName**](wspgetsockname-2.md) function.

### -field lpWSPGetSockOpt


A pointer to the <b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspgetsockopt">LPWSPGetSockopt</a></b> function.

### -field lpWSPGetQOSByName

 

A pointer to the [**WSPGetQOSByName**](wspgetqosbyname-2.md) function.

### -field lpWSPIoctl

 

A pointer to the <b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspioctl">LPWSPIoctl</a></b> function.

### -field lpWSPJoinLeaf

 

A pointer to the <b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspjoinleaf">LPWSPJoinLeaf</a></b> function.

### -field lpWSPListen

 

A pointer to the <b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwsplisten">LPWSPListen</a></b> function.

### -field lpWSPRecv

 

A pointer to the <b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwsprecv">LPWSPRecv</a></b> function.

### -field lpWSPRecvDisconnect

 

A pointer to the [**WSPRecvDisconnect**](wsprecvdisconnect-2.md) function.

### -field lpWSPRecvFrom

 

A pointer to the <b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwsprecvfrom">LPWSPRecvFrom</a></b> function.

### -field lpWSPSelect

 

A pointer to the [<b>LPWSPSelect</b>](wspselect-2.md) function.

### -field lpWSPSend

 

A pointer to the <b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspsend">LPWSPSend</a></b> function.

### -field lpWSPSendDisconnect

 

A pointer to the [**WSPSendDisconnect**](wspsenddisconnect-2.md) function.

### -field lpWSPSendTo

 

A pointer to the <b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspsendto">LPWSPSendTo</a></b> function.

### -field lpWSPSetSockOpt

 

A pointer to the <b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspsetsockopt">LPWSPSetSockOpt</a></b> function.

### -field lpWSPShutdown

 

A pointer to the <b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspshutdown">LPWSPShutdown</a></b> function.

### -field lpWSPSocket

 

A pointer to the <a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspsocket">LPWSPSocket</a> function.

### -field lpWSPStringToAddress

 

A pointer to the <a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspstringtoaddress">LPWSPStringToAddress<a> function.

## -remarks
The <b>WSPPROC_TABLE</b> structure contains a table of pointers to service provider functions that are returned by the <a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nf-ws2spi-wspstartup">WSPStartup<a> function.

## -see-also
<b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspaccept">LPWSPAccept</a></b>


<b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspstringtoaddress">LPWSPStringToAddress<a></b>


<b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspasyncselect">LPWSPAsyncSelect</a><b>

<b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspbind">LPWSPBind</a></b>

<b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspcancelblockingcall">LPWSPCancelBlockingCall</a></b>

<b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspcleanup">LPWSPCleanup</a></b>

<b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspclosecoket">LPWSPCloseSocket</a></b>

<b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspconnect">LPWSPConnect</a></b>

<b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspduplicatesocket">LPWSPDuplicateSocket</a></b>

<b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspenumnetworkevents">LPWSPEnumNetworkEvents</a></b>

<b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspgetoverlappedresult">LPWSPGetOverlappedResult</a></b>

<b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspgetqosbyname">LPWSPGetQOSByName</a></b>

<b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspgetsockname">LPWSPGetSockName</a></b>

<b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspgetsockopt">LPWSPGetSockopt</a></b>

<b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspioctl">LPWSPIoctl</a></b>

<b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspjoinleaf">LPWSPJoinLeaf</a></b>

<b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwsplisten">LPWSPListen</a></b>

<b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwsprecv">LPWSPRecv</a></b>

<b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwsprecvdisconnect">LPWSPRecvDisconnect</a></b>

<b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwsprecvfrom">LPWSPRecvFrom</a></b>

<b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspsend">LPWSPSend</a></b>

<b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspsenddisconnect">LPWSPSendDisconnect</a></b>

<b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspsendto">LPWSPSendTo</a></b>

<b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspsetsockopt">LPWSPSetSockOpt</a></b>

<b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspshutdown">LPWSPShutdown</a></b>

<a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspsocket">LPWSPSocket</a>

<a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nf-ws2spi-wspstartup">WSPStartup<a>

<a href=" https://docs.microsoft.com/en-us/windows/win32/api/winsock2/nf-winsock2-wsastringtoaddressa">WSAStringToAddress<a>

