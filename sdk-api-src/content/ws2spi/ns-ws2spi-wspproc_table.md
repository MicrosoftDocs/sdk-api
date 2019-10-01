---
UID: NS:ws2spi._WSPPROC_TABLE
title: WSPPROC_TABLE (ws2spi.h)
author: windows-sdk-content
description: Contains a table of pointers to service provider functions.
old-location: winsock\wspproc_table.htm
tech.root: WinSock
ms.assetid: f6fbf6da-58c5-4cef-8897-789a1e02aabb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPWSPPROC_TABLE, FAR * LPWSPPROC_TABLE, FAR * LPWSPPROC_TABLE structure [Winsock], WSPPROC_TABLE, WSPPROC_TABLE structure [Winsock], winsock.wspproc_table, ws2spi/FAR * LPWSPPROC_TABLE, ws2spi/WSPPROC_TABLE"
ms.topic: struct
f1_keywords: 
 - "ws2spi/WSPPROC_TABLE"
req.header: ws2spi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ws2spi.h
api_name:
 - WSPPROC_TABLE
targetos: Windows
req.typenames: WSPPROC_TABLE, *LPWSPPROC_TABLE
req.redist: 
ms.custom: 19H1
---

# WSPPROC_TABLE structure


## -description


The 
<b>WSPPROC_TABLE</b> structure contains a table of pointers to service provider functions.


## -struct-fields




### -field lpWSPAccept

Type: <b>LPWSPACCEPT</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpwspaccept">WSPAccept</a> function.


### -field lpWSPAddressToString

Type: <b>LPWSPADDRESSTOSTRING</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpwspaddresstostring">WSPAddressToString</a> function.


### -field lpWSPAsyncSelect

Type: <b>LPWSPASYNCSELECT</b>

A pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)">WSPAsyncSelect</a> function.


### -field lpWSPBind

Type: <b>LPWSPBIND</b>

A pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566268(v=vs.85)">WSPBind</a> function. 


### -field lpWSPCancelBlockingCall

Type: <b>LPWSPCANCELBLOCKINGCALL</b>

A pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)">WSPCancelBlockingCall</a> function. 


### -field lpWSPCleanup

Type: <b>LPWSPCLEANUP</b>

A pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566270(v=vs.85)">WSPCleanup</a> function. 


### -field lpWSPCloseSocket

Type: <b>LPWSPCLOSESOCKET</b>

A pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566273(v=vs.85)">WSPCloseSocket</a> function. 


### -field lpWSPConnect

Type: <b>LPWSPCONNECT</b>

A pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566275(v=vs.85)">WSPConnect</a> function. 


### -field lpWSPDuplicateSocket

Type: <b>LPWSPDUPLICATESOCKET</b>

A pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566282(v=vs.85)">WSPDuplicateSocket</a> function. 


### -field lpWSPEnumNetworkEvents

Type: <b>LPWSPENUMNETWORKEVENTS</b>

A pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566284(v=vs.85)">WSPEnumNetworkEvents</a> function. 


### -field lpWSPEventSelect

Type: <b>LPWSPEVENTSELECT</b>

A pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566287(v=vs.85)">WSPEventSelect</a> function. 


### -field lpWSPGetOverlappedResult

Type: <b>LPWSPGETOVERLAPPEDRESULT</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpwspgetoverlappedresult">WSPGetOverlappedResult</a> function. 


### -field lpWSPGetPeerName

Type: <b>LPWSPGETPEERNAME</b>

A pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms742278(v=vs.85)">WSPGetPeerName</a> function. 


### -field lpWSPGetSockName

Type: <b>LPWSPGETSOCKNAME</b>

A pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms742280(v=vs.85)">WSPGetSockName</a> function. 


### -field lpWSPGetSockOpt

Type: <b>LPWSPGETSOCKOPT</b>

A pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566292(v=vs.85)">WSPGetSockOpt</a> function. 


### -field lpWSPGetQOSByName

Type: <b>LPWSPGETQOSBYNAME</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpwspgetqosbyname">WSPGetQOSByName</a> function. 


### -field lpWSPIoctl

Type: <b>LPWSPIOCTL</b>

A pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566296(v=vs.85)">WSPIoctl</a> function. 


### -field lpWSPJoinLeaf

Type: <b>LPWSPJOINLEAF</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpwspjoinleaf">WSPJoinLeaf</a> function. 


### -field lpWSPListen

Type: <b>LPWSPLISTEN</b>

A pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566297(v=vs.85)">WSPListen</a> function. 


### -field lpWSPRecv

Type: <b>LPWSPRECV</b>

A pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566309(v=vs.85)">WSPRecv</a> function. 


### -field lpWSPRecvDisconnect

Type: <b>LPWSPRECVDISCONNECT</b>

A pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms742285(v=vs.85)">WSPRecvDisconnect</a> function. 


### -field lpWSPRecvFrom

Type: <b>LPWSPRECVFROM</b>

A pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)">WSPRecvFrom</a> function. 


### -field lpWSPSelect

Type: <b>LPWSPSELECT</b>

A pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)">WSPSelect</a> function. 


### -field lpWSPSend

Type: <b>LPWSPSEND</b>

A pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566316(v=vs.85)">WSPSend</a> function. 


### -field lpWSPSendDisconnect

Type: <b>LPWSPSENDDISCONNECT</b>

A pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)">WSPSendDisconnect</a> function. 


### -field lpWSPSendTo

Type: <b>LPWSPSENDTO</b>

A pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)">WSPSendTo</a> function. 


### -field lpWSPSetSockOpt

Type: <b>LPWSPSETSOCKOPT</b>

A pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566318(v=vs.85)">WSPSetSockOpt</a> function. 


### -field lpWSPShutdown

Type: <b>LPWSPSHUTDOWN</b>

A pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)">WSPShutdown</a> function. 


### -field lpWSPSocket

Type: <b>LPWSPSOCKET</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpwspsocket">WSPSocket</a> function. 


### -field lpWSPStringToAddress

Type: <b>LPWSPSTRINGTOADDRESS</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpwspstringtoaddress">WSPStringToAddress</a> function. 


## -remarks



 The 
<b>WSPPROC_TABLE</b> structure contains a table of pointers to service provider functions that are returned by the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wspstartup">WSPStartup</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpwspaccept">WSPAccept</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpwspaddresstostring">WSPAddressToString</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)">WSPAsyncSelect</a>



<a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566268(v=vs.85)">WSPBind</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)">WSPCancelBlockingCall</a>



<a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566270(v=vs.85)">WSPCleanup</a>



<a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566273(v=vs.85)">WSPCloseSocket</a>



<a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566275(v=vs.85)">WSPConnect</a>



<a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566282(v=vs.85)">WSPDuplicateSocket</a>



<a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566284(v=vs.85)">WSPEnumNetworkEvents</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpwspgetoverlappedresult">WSPGetOverlappedResult</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms742278(v=vs.85)">WSPGetPeerName</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpwspgetqosbyname">WSPGetQOSByName</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms742280(v=vs.85)">WSPGetSockName</a>



<a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566292(v=vs.85)">WSPGetSockOpt</a>



<a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566296(v=vs.85)">WSPIoctl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpwspjoinleaf">WSPJoinLeaf</a>



<a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566297(v=vs.85)">WSPListen</a>



<a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566309(v=vs.85)">WSPRecv</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms742285(v=vs.85)">WSPRecvDisconnect</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)">WSPRecvFrom</a>



<a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566316(v=vs.85)">WSPSend</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)">WSPSendDisconnect</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)">WSPSendTo</a>



<a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566318(v=vs.85)">WSPSetSockOpt</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)">WSPShutdown</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpwspsocket">WSPSocket</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wspstartup">WSPStartup</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpwspstringtoaddress">WSPStringToAddress</a>
 

 

