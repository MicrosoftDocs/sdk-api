---
UID: NS:ws2spi._WSPPROC_TABLE
title: "_WSPPROC_TABLE"
author: windows-sdk-content
description: Contains a table of pointers to service provider functions.
old-location: winsock\wspproc_table.htm
old-project: WinSock
ms.assetid: f6fbf6da-58c5-4cef-8897-789a1e02aabb
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*LPWSPPROC_TABLE, FAR * LPWSPPROC_TABLE, FAR * LPWSPPROC_TABLE structure [Winsock], WSPPROC_TABLE, WSPPROC_TABLE structure [Winsock], _WSPPROC_TABLE, winsock.wspproc_table, ws2spi/FAR * LPWSPPROC_TABLE, ws2spi/WSPPROC_TABLE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ws2spi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WSPPROC_TABLE, *LPWSPPROC_TABLE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ws2spi.h
api_name:
 - WSPPROC_TABLE
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

A pointer to the <a href="https://msdn.microsoft.com/d73aa3a8-cef5-485d-b2ba-b2fe42ab6200">WSPAccept</a> function.


### -field lpWSPAddressToString

Type: <b>LPWSPADDRESSTOSTRING</b>

A pointer to the <a href="https://msdn.microsoft.com/7a6d8f77-7235-4cd1-90e1-9b5260137246">WSPAddressToString</a> function.


### -field lpWSPAsyncSelect

Type: <b>LPWSPASYNCSELECT</b>

A pointer to the <a href="https://msdn.microsoft.com/a96e0c2f-8bd0-4fcf-b7bd-67b3f7f53005">WSPAsyncSelect</a> function.


### -field lpWSPBind

Type: <b>LPWSPBIND</b>

A pointer to the <a href="https://msdn.microsoft.com/0fe5a66a-1126-494c-b4da-8041841685c6">WSPBind</a> function. 


### -field lpWSPCancelBlockingCall

Type: <b>LPWSPCANCELBLOCKINGCALL</b>

A pointer to the <a href="https://msdn.microsoft.com/9219c733-43af-414b-8a38-78da52757bd1">WSPCancelBlockingCall</a> function. 


### -field lpWSPCleanup

Type: <b>LPWSPCLEANUP</b>

A pointer to the <a href="https://msdn.microsoft.com/401a8c78-48f5-4f80-9708-6d75877fe738">WSPCleanup</a> function. 


### -field lpWSPCloseSocket

Type: <b>LPWSPCLOSESOCKET</b>

A pointer to the <a href="https://msdn.microsoft.com/0190f561-68fa-45d8-9702-3caae58bf0cc">WSPCloseSocket</a> function. 


### -field lpWSPConnect

Type: <b>LPWSPCONNECT</b>

A pointer to the <a href="https://msdn.microsoft.com/1daca98e-57d8-47f1-af5f-778a33b2c538">WSPConnect</a> function. 


### -field lpWSPDuplicateSocket

Type: <b>LPWSPDUPLICATESOCKET</b>

A pointer to the <a href="https://msdn.microsoft.com/6d9cf472-357e-4226-b53e-09083b42ed13">WSPDuplicateSocket</a> function. 


### -field lpWSPEnumNetworkEvents

Type: <b>LPWSPENUMNETWORKEVENTS</b>

A pointer to the <a href="https://msdn.microsoft.com/65f7a93b-3596-4318-a90c-79889ffabdeb">WSPEnumNetworkEvents</a> function. 


### -field lpWSPEventSelect

Type: <b>LPWSPEVENTSELECT</b>

A pointer to the <a href="https://msdn.microsoft.com/e23e0370-5776-4544-b845-c578c5a514bd">WSPEventSelect</a> function. 


### -field lpWSPGetOverlappedResult

Type: <b>LPWSPGETOVERLAPPEDRESULT</b>

A pointer to the <a href="https://msdn.microsoft.com/8156b8ab-00f8-4325-9b81-3e43053f4f56">WSPGetOverlappedResult</a> function. 


### -field lpWSPGetPeerName

Type: <b>LPWSPGETPEERNAME</b>

A pointer to the <a href="https://msdn.microsoft.com/e543b21b-8cf8-4b7b-a4b5-5a43db999786">WSPGetPeerName</a> function. 


### -field lpWSPGetSockName

Type: <b>LPWSPGETSOCKNAME</b>

A pointer to the <a href="https://msdn.microsoft.com/8e5ff6dc-f24f-4418-8de8-356f74a37eaa">WSPGetSockName</a> function. 


### -field lpWSPGetSockOpt

Type: <b>LPWSPGETSOCKOPT</b>

A pointer to the <a href="https://msdn.microsoft.com/ec63c7a5-2cee-4bdf-ab24-a91d2ea9eb5e">WSPGetSockOpt</a> function. 


### -field lpWSPGetQOSByName

Type: <b>LPWSPGETQOSBYNAME</b>

A pointer to the <a href="https://msdn.microsoft.com/2e218a9b-6db5-4c5a-94e1-207886c401a5">WSPGetQOSByName</a> function. 


### -field lpWSPIoctl

Type: <b>LPWSPIOCTL</b>

A pointer to the <a href="https://msdn.microsoft.com/098d85e3-8fe2-46c2-966d-deae4b12afd6">WSPIoctl</a> function. 


### -field lpWSPJoinLeaf

Type: <b>LPWSPJOINLEAF</b>

A pointer to the <a href="https://msdn.microsoft.com/3b0451e2-0e4c-4da7-b16c-37c242632bdd">WSPJoinLeaf</a> function. 


### -field lpWSPListen

Type: <b>LPWSPLISTEN</b>

A pointer to the <a href="https://msdn.microsoft.com/43d588dd-7aa2-405b-8f9d-b167bbbc6574">WSPListen</a> function. 


### -field lpWSPRecv

Type: <b>LPWSPRECV</b>

A pointer to the <a href="https://msdn.microsoft.com/5304a5d6-bc99-4a6f-8eeb-668bbd93fc84">WSPRecv</a> function. 


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

A pointer to the <a href="https://msdn.microsoft.com/4d741663-34f5-41b9-ba8f-77d45382d50b">WSPSend</a> function. 


### -field lpWSPSendDisconnect

Type: <b>LPWSPSENDDISCONNECT</b>

A pointer to the <a href="https://msdn.microsoft.com/ac6ef0c7-61b2-4408-8f0d-ab68191ef8e8">WSPSendDisconnect</a> function. 


### -field lpWSPSendTo

Type: <b>LPWSPSENDTO</b>

A pointer to the <a href="https://msdn.microsoft.com/9e788289-6545-4e5e-9d00-f284b2337fcd">WSPSendTo</a> function. 


### -field lpWSPSetSockOpt

Type: <b>LPWSPSETSOCKOPT</b>

A pointer to the <a href="https://msdn.microsoft.com/2b440208-ca10-424a-8f18-3241b4e0184c">WSPSetSockOpt</a> function. 


### -field lpWSPShutdown

Type: <b>LPWSPSHUTDOWN</b>

A pointer to the <a href="https://msdn.microsoft.com/b2de40a5-6978-43a6-aa1c-35c10284f09c">WSPShutdown</a> function. 


### -field lpWSPSocket

Type: <b>LPWSPSOCKET</b>

A pointer to the <a href="https://msdn.microsoft.com/16735fd1-289d-425a-8ad2-c20d73888b1b">WSPSocket</a> function. 


### -field lpWSPStringToAddress

Type: <b>LPWSPSTRINGTOADDRESS</b>

A pointer to the <a href="https://msdn.microsoft.com/65cf8f7e-7ef0-472c-82d8-e8f7df9976a9">WSPStringToAddress</a> function. 


## -remarks



 The 
<b>WSPPROC_TABLE</b> structure contains a table of pointers to service provider functions that are returned by the <a href="https://msdn.microsoft.com/9ebfe81c-bed6-4bde-b1dd-5eaefbaac9cf">WSPStartup</a> function.




## -see-also




<a href="https://msdn.microsoft.com/d73aa3a8-cef5-485d-b2ba-b2fe42ab6200">WSPAccept</a>



<a href="https://msdn.microsoft.com/7a6d8f77-7235-4cd1-90e1-9b5260137246">WSPAddressToString</a>



<a href="https://msdn.microsoft.com/a96e0c2f-8bd0-4fcf-b7bd-67b3f7f53005">WSPAsyncSelect</a>



<a href="https://msdn.microsoft.com/0fe5a66a-1126-494c-b4da-8041841685c6">WSPBind</a>



<a href="https://msdn.microsoft.com/9219c733-43af-414b-8a38-78da52757bd1">WSPCancelBlockingCall</a>



<a href="https://msdn.microsoft.com/401a8c78-48f5-4f80-9708-6d75877fe738">WSPCleanup</a>



<a href="https://msdn.microsoft.com/0190f561-68fa-45d8-9702-3caae58bf0cc">WSPCloseSocket</a>



<a href="https://msdn.microsoft.com/1daca98e-57d8-47f1-af5f-778a33b2c538">WSPConnect</a>



<a href="https://msdn.microsoft.com/6d9cf472-357e-4226-b53e-09083b42ed13">WSPDuplicateSocket</a>



<a href="https://msdn.microsoft.com/65f7a93b-3596-4318-a90c-79889ffabdeb">WSPEnumNetworkEvents</a>



<a href="https://msdn.microsoft.com/8156b8ab-00f8-4325-9b81-3e43053f4f56">WSPGetOverlappedResult</a>



<a href="https://msdn.microsoft.com/e543b21b-8cf8-4b7b-a4b5-5a43db999786">WSPGetPeerName</a>



<a href="https://msdn.microsoft.com/2e218a9b-6db5-4c5a-94e1-207886c401a5">WSPGetQOSByName</a>



<a href="https://msdn.microsoft.com/8e5ff6dc-f24f-4418-8de8-356f74a37eaa">WSPGetSockName</a>



<a href="https://msdn.microsoft.com/ec63c7a5-2cee-4bdf-ab24-a91d2ea9eb5e">WSPGetSockOpt</a>



<a href="https://msdn.microsoft.com/098d85e3-8fe2-46c2-966d-deae4b12afd6">WSPIoctl</a>



<a href="https://msdn.microsoft.com/3b0451e2-0e4c-4da7-b16c-37c242632bdd">WSPJoinLeaf</a>



<a href="https://msdn.microsoft.com/43d588dd-7aa2-405b-8f9d-b167bbbc6574">WSPListen</a>



<a href="https://msdn.microsoft.com/5304a5d6-bc99-4a6f-8eeb-668bbd93fc84">WSPRecv</a>



<a href="https://msdn.microsoft.com/c94da7d7-9b5a-44e2-894d-b3f1e31047e0">WSPRecvDisconnect</a>



<a href="https://msdn.microsoft.com/f405cddf-b02e-41dd-bd65-fc73200c5fb3">WSPRecvFrom</a>



<a href="https://msdn.microsoft.com/4d741663-34f5-41b9-ba8f-77d45382d50b">WSPSend</a>



<a href="https://msdn.microsoft.com/ac6ef0c7-61b2-4408-8f0d-ab68191ef8e8">WSPSendDisconnect</a>



<a href="https://msdn.microsoft.com/9e788289-6545-4e5e-9d00-f284b2337fcd">WSPSendTo</a>



<a href="https://msdn.microsoft.com/2b440208-ca10-424a-8f18-3241b4e0184c">WSPSetSockOpt</a>



<a href="https://msdn.microsoft.com/b2de40a5-6978-43a6-aa1c-35c10284f09c">WSPShutdown</a>



<a href="https://msdn.microsoft.com/16735fd1-289d-425a-8ad2-c20d73888b1b">WSPSocket</a>



<a href="https://msdn.microsoft.com/9ebfe81c-bed6-4bde-b1dd-5eaefbaac9cf">WSPStartup</a>



<a href="https://msdn.microsoft.com/65cf8f7e-7ef0-472c-82d8-e8f7df9976a9">WSPStringToAddress</a>
 

 

