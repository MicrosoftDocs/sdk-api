---
UID: NS:ws2spi._WSPPROC_TABLE
title: "_WSPPROC_TABLE"
author: windows-driver-content
description: Contains a table of pointers to service provider functions.
old-location: winsock\wspproc_table.htm
old-project: WinSock
ms.assetid: f6fbf6da-58c5-4cef-8897-789a1e02aabb
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: "*LPWSPPROC_TABLE, FAR * LPWSPPROC_TABLE, FAR * LPWSPPROC_TABLE structure [Winsock], WSPPROC_TABLE, WSPPROC_TABLE structure [Winsock], _WSPPROC_TABLE, winsock.wspproc_table, ws2spi/FAR * LPWSPPROC_TABLE, ws2spi/WSPPROC_TABLE"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: WSPPROC_TABLE, *LPWSPPROC_TABLE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ws2spi.h
api_name:
-	WSPPROC_TABLE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSPPROC_TABLE structure


## -description


The 
<b>WSPPROC_TABLE</b> structure contains a table of pointers to service provider functions.


## -struct-fields




### -field lpWSPAccept

Type: <b>LPWSPACCEPT</b>

A pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff566266">WSPAccept</a> function.


### -field lpWSPAddressToString

Type: <b>LPWSPADDRESSTOSTRING</b>

A pointer to the <a href="https://msdn.microsoft.com/7a6d8f77-7235-4cd1-90e1-9b5260137246">WSPAddressToString</a> function.


### -field lpWSPAsyncSelect

Type: <b>LPWSPASYNCSELECT</b>

A pointer to the <a href="https://msdn.microsoft.com/a96e0c2f-8bd0-4fcf-b7bd-67b3f7f53005">WSPAsyncSelect</a> function.


### -field lpWSPBind

Type: <b>LPWSPBIND</b>

A pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff566268">WSPBind</a> function. 


### -field lpWSPCancelBlockingCall

Type: <b>LPWSPCANCELBLOCKINGCALL</b>

A pointer to the <a href="https://msdn.microsoft.com/9219c733-43af-414b-8a38-78da52757bd1">WSPCancelBlockingCall</a> function. 


### -field lpWSPCleanup

Type: <b>LPWSPCLEANUP</b>

A pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff566270">WSPCleanup</a> function. 


### -field lpWSPCloseSocket

Type: <b>LPWSPCLOSESOCKET</b>

A pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff566273">WSPCloseSocket</a> function. 


### -field lpWSPConnect

Type: <b>LPWSPCONNECT</b>

A pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff566275">WSPConnect</a> function. 


### -field lpWSPDuplicateSocket

Type: <b>LPWSPDUPLICATESOCKET</b>

A pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff566282">WSPDuplicateSocket</a> function. 


### -field lpWSPEnumNetworkEvents

Type: <b>LPWSPENUMNETWORKEVENTS</b>

A pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff566284">WSPEnumNetworkEvents</a> function. 


### -field lpWSPEventSelect

Type: <b>LPWSPEVENTSELECT</b>

A pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff566287">WSPEventSelect</a> function. 


### -field lpWSPGetOverlappedResult

Type: <b>LPWSPGETOVERLAPPEDRESULT</b>

A pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff566288">WSPGetOverlappedResult</a> function. 


### -field lpWSPGetPeerName

Type: <b>LPWSPGETPEERNAME</b>

A pointer to the <a href="https://msdn.microsoft.com/e543b21b-8cf8-4b7b-a4b5-5a43db999786">WSPGetPeerName</a> function. 


### -field lpWSPGetSockName

Type: <b>LPWSPGETSOCKNAME</b>

A pointer to the <a href="https://msdn.microsoft.com/8e5ff6dc-f24f-4418-8de8-356f74a37eaa">WSPGetSockName</a> function. 


### -field lpWSPGetSockOpt

Type: <b>LPWSPGETSOCKOPT</b>

A pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff566292">WSPGetSockOpt</a> function. 


### -field lpWSPGetQOSByName

Type: <b>LPWSPGETQOSBYNAME</b>

A pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff566290">WSPGetQOSByName</a> function. 


### -field lpWSPIoctl

Type: <b>LPWSPIOCTL</b>

A pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff566296">WSPIoctl</a> function. 


### -field lpWSPJoinLeaf

Type: <b>LPWSPJOINLEAF</b>

A pointer to the <a href="https://msdn.microsoft.com/3b0451e2-0e4c-4da7-b16c-37c242632bdd">WSPJoinLeaf</a> function. 


### -field lpWSPListen

Type: <b>LPWSPLISTEN</b>

A pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff566297">WSPListen</a> function. 


### -field lpWSPRecv

Type: <b>LPWSPRECV</b>

A pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff566309">WSPRecv</a> function. 


### -field lpWSPRecvDisconnect

Type: <b>LPWSPRECVDISCONNECT</b>

A pointer to the <a href="https://msdn.microsoft.com/c94da7d7-9b5a-44e2-894d-b3f1e31047e0">WSPRecvDisconnect</a> function. 


### -field lpWSPRecvFrom

Type: <b>LPWSPRECVFROM</b>

A pointer to the <a href="https://msdn.microsoft.com/f405cddf-b02e-41dd-bd65-fc73200c5fb3">WSPRecvFrom</a> function. 


### -field lpWSPSelect

Type: <b>LPWSPSELECT</b>

A pointer to the <a href="https://msdn.microsoft.com/a8f2922d-2474-406d-b1c7-631f05ccdd9c">WSPSelect</a> function. 


### -field lpWSPSend

Type: <b>LPWSPSEND</b>

A pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff566316">WSPSend</a> function. 


### -field lpWSPSendDisconnect

Type: <b>LPWSPSENDDISCONNECT</b>

A pointer to the <a href="https://msdn.microsoft.com/ac6ef0c7-61b2-4408-8f0d-ab68191ef8e8">WSPSendDisconnect</a> function. 


### -field lpWSPSendTo

Type: <b>LPWSPSENDTO</b>

A pointer to the <a href="https://msdn.microsoft.com/9e788289-6545-4e5e-9d00-f284b2337fcd">WSPSendTo</a> function. 


### -field lpWSPSetSockOpt

Type: <b>LPWSPSETSOCKOPT</b>

A pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff566318">WSPSetSockOpt</a> function. 


### -field lpWSPShutdown

Type: <b>LPWSPSHUTDOWN</b>

A pointer to the <a href="https://msdn.microsoft.com/b2de40a5-6978-43a6-aa1c-35c10284f09c">WSPShutdown</a> function. 


### -field lpWSPSocket

Type: <b>LPWSPSOCKET</b>

A pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff566319">WSPSocket</a> function. 


### -field lpWSPStringToAddress

Type: <b>LPWSPSTRINGTOADDRESS</b>

A pointer to the <a href="https://msdn.microsoft.com/65cf8f7e-7ef0-472c-82d8-e8f7df9976a9">WSPStringToAddress</a> function. 


## -remarks



 The 
<b>WSPPROC_TABLE</b> structure contains a table of pointers to service provider functions that are returned by the <a href="https://msdn.microsoft.com/9ebfe81c-bed6-4bde-b1dd-5eaefbaac9cf">WSPStartup</a> function.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff566266">WSPAccept</a>



<a href="https://msdn.microsoft.com/7a6d8f77-7235-4cd1-90e1-9b5260137246">WSPAddressToString</a>



<a href="https://msdn.microsoft.com/a96e0c2f-8bd0-4fcf-b7bd-67b3f7f53005">WSPAsyncSelect</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566268">WSPBind</a>



<a href="https://msdn.microsoft.com/9219c733-43af-414b-8a38-78da52757bd1">WSPCancelBlockingCall</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566270">WSPCleanup</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566273">WSPCloseSocket</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566275">WSPConnect</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566282">WSPDuplicateSocket</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566284">WSPEnumNetworkEvents</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566288">WSPGetOverlappedResult</a>



<a href="https://msdn.microsoft.com/e543b21b-8cf8-4b7b-a4b5-5a43db999786">WSPGetPeerName</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566290">WSPGetQOSByName</a>



<a href="https://msdn.microsoft.com/8e5ff6dc-f24f-4418-8de8-356f74a37eaa">WSPGetSockName</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566292">WSPGetSockOpt</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566296">WSPIoctl</a>



<a href="https://msdn.microsoft.com/3b0451e2-0e4c-4da7-b16c-37c242632bdd">WSPJoinLeaf</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566297">WSPListen</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566309">WSPRecv</a>



<a href="https://msdn.microsoft.com/c94da7d7-9b5a-44e2-894d-b3f1e31047e0">WSPRecvDisconnect</a>



<a href="https://msdn.microsoft.com/f405cddf-b02e-41dd-bd65-fc73200c5fb3">WSPRecvFrom</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566316">WSPSend</a>



<a href="https://msdn.microsoft.com/ac6ef0c7-61b2-4408-8f0d-ab68191ef8e8">WSPSendDisconnect</a>



<a href="https://msdn.microsoft.com/9e788289-6545-4e5e-9d00-f284b2337fcd">WSPSendTo</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566318">WSPSetSockOpt</a>



<a href="https://msdn.microsoft.com/b2de40a5-6978-43a6-aa1c-35c10284f09c">WSPShutdown</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566319">WSPSocket</a>



<a href="https://msdn.microsoft.com/9ebfe81c-bed6-4bde-b1dd-5eaefbaac9cf">WSPStartup</a>



<a href="https://msdn.microsoft.com/65cf8f7e-7ef0-472c-82d8-e8f7df9976a9">WSPStringToAddress</a>
 

 

