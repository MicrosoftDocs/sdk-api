---
UID: NS:ws2spi._WSPUPCALLTABLE
title: "_WSPUPCALLTABLE"
author: windows-sdk-content
description: Contains a table of pointers to service provider upcall functions.
old-location: winsock\wspupcalltable.htm
tech.root: WinSock
ms.assetid: a5abf488-3e78-4e4e-ae5f-201bf0d77fc9
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*LPWSPUPCALLTABLE, FAR * LPWSPUPCALLTABLE, FAR * LPWSPUPCALLTABLE structure [Winsock], WSPUPCALLTABLE, WSPUPCALLTABLE structure [Winsock], _WSPUPCALLTABLE, winsock.wspupcalltable, ws2spi/FAR * LPWSPUPCALLTABLE, ws2spi/WSPUPCALLTABLE"
ms.prod: windows
ms.technology: windows-sdk
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
 - WSPUPCALLTABLE
product: Windows
targetos: Windows
req.typenames: WSPUPCALLTABLE, *LPWSPUPCALLTABLE
req.redist: 
---

# _WSPUPCALLTABLE structure


## -description


The 
<b>WSPUPCALLTABLE</b> structure contains a table of pointers to service provider upcall functions.


## -struct-fields




### -field lpWPUCloseEvent

Type: <b>LPWPUCLOSEEVENT</b>

A pointer to the <a href="https://msdn.microsoft.com/d8c6133b-e5a7-4936-a796-0930bb95fd0c">WPUCloseEvent</a> function. 


### -field lpWPUCloseSocketHandle

Type: <b>LPWPUCLOSESOCKETHANDLE</b>

A pointer to the <a href="https://msdn.microsoft.com/c125b763-6c5a-4a83-ba34-79e898fdc9fe">WPUCloseSocketHandle</a> function. 


### -field lpWPUCreateEvent

Type: <b>LPWPUCREATEEVENT</b>

A pointer to the <a href="https://msdn.microsoft.com/61e71e93-e35f-4122-bd4d-c103f652d2ca">WPUCreateEvent</a> function. 


### -field lpWPUCreateSocketHandle

Type: <b>LPWPUCREATESOCKETHANDLE</b>

A pointer to the <a href="https://msdn.microsoft.com/ecbf9d8b-b705-4160-ac77-afa5b1501534">WPUCreateSocketHandle</a> function. 


### -field lpWPUFDIsSet

Type: <b>LPWPUFDISSET</b>

A pointer to the <a href="https://msdn.microsoft.com/87726b13-ede4-4c73-be98-4ad4180ea3e7">WPUFDIsSet</a> function. 


### -field lpWPUGetProviderPath

Type: <b>LPWPUGETPROVIDERPATH</b>

A pointer to the <a href="https://msdn.microsoft.com/fb59e69a-bee4-4807-9ef2-cbcc8c0d367f">WPUGetProviderPath</a> function. 


### -field lpWPUModifyIFSHandle

Type: <b>LPWPUMODIFYIFSHANDLE</b>

A pointer to the <a href="https://msdn.microsoft.com/f58971eb-0948-4e16-a767-1d4cba9ec721">WPUModifyIFSHandle</a> function. 


### -field lpWPUPostMessage

Type: <b>LPWPUPOSTMESSAGE</b>

A pointer to the <a href="https://msdn.microsoft.com/f4241941-c39f-441e-aad4-b84f2f8ed828">WPUPostMessage</a> function. 


### -field lpWPUQueryBlockingCallback

Type: <b>LPWPUQUERYBLOCKINGCALLBACK</b>

A pointer to the <a href="https://msdn.microsoft.com/08e6215c-536f-4ab2-9d34-096b919ef0be">WPUQueryBlockingCallback</a> function. 


### -field lpWPUQuerySocketHandleContext

Type: <b>LPWPUQUERYSOCKETHANDLECONTEXT</b>

A pointer to the <a href="https://msdn.microsoft.com/661ddff0-b80c-4e24-84b3-b444ef1c2ad6">WPUQuerySocketHandleContext</a> function. 


### -field lpWPUQueueApc

Type: <b>LPWPUQUEUEAPC</b>

A pointer to the <a href="https://msdn.microsoft.com/4326547e-85e2-409c-9f36-aa013853dfd9">WPUQueueApc</a> function. 


### -field lpWPUResetEvent

Type: <b>LPWPURESETEVENT</b>

A pointer to the <a href="https://msdn.microsoft.com/a3385c77-899c-4772-88b9-fb3e0fab54e0">WPUResetEvent</a> function. 


### -field lpWPUSetEvent

Type: <b>LPWPUSETEVENT</b>

A pointer to the <a href="https://msdn.microsoft.com/d5caa926-1223-4917-85ba-4f79731e955a">WPUSetEvent</a> function. 


### -field lpWPUOpenCurrentThread

Type: <b>LPWPUOPENCURRENTTHREAD</b>

A pointer to the <a href="https://msdn.microsoft.com/92d21f29-240f-407e-89a7-bbbb8f9bf0eb">WPUOpenCurrentThread</a> function. 


### -field lpWPUCloseThread

Type: <b>LPWPUCLOSETHREAD</b>

A pointer to the <a href="https://msdn.microsoft.com/1a5e7a99-484f-4862-bd28-edf85debc8e5">WPUCloseThread</a> function. 


## -remarks



The <b>WSPUPCALLTABLE</b> structure contains a table of pointers to service provider upcall functions that are passed to the <a href="https://msdn.microsoft.com/9ebfe81c-bed6-4bde-b1dd-5eaefbaac9cf">WSPStartup</a> function.




## -see-also




<a href="https://msdn.microsoft.com/d8c6133b-e5a7-4936-a796-0930bb95fd0c">WPUCloseEvent</a>



<a href="https://msdn.microsoft.com/c125b763-6c5a-4a83-ba34-79e898fdc9fe">WPUCloseSocketHandle</a>



<a href="https://msdn.microsoft.com/1a5e7a99-484f-4862-bd28-edf85debc8e5">WPUCloseThread</a>



<a href="https://msdn.microsoft.com/61e71e93-e35f-4122-bd4d-c103f652d2ca">WPUCreateEvent</a>



<a href="https://msdn.microsoft.com/ecbf9d8b-b705-4160-ac77-afa5b1501534">WPUCreateSocketHandle</a>



<a href="https://msdn.microsoft.com/87726b13-ede4-4c73-be98-4ad4180ea3e7">WPUFDIsSet</a>



<a href="https://msdn.microsoft.com/fb59e69a-bee4-4807-9ef2-cbcc8c0d367f">WPUGetProviderPath</a>



<a href="https://msdn.microsoft.com/f58971eb-0948-4e16-a767-1d4cba9ec721">WPUModifyIFSHandle</a>



<a href="https://msdn.microsoft.com/92d21f29-240f-407e-89a7-bbbb8f9bf0eb">WPUOpenCurrentThread</a>



<a href="https://msdn.microsoft.com/f4241941-c39f-441e-aad4-b84f2f8ed828">WPUPostMessage</a>



<a href="https://msdn.microsoft.com/08e6215c-536f-4ab2-9d34-096b919ef0be">WPUQueryBlockingCallback</a>



<a href="https://msdn.microsoft.com/661ddff0-b80c-4e24-84b3-b444ef1c2ad6">WPUQuerySocketHandleContext</a>



<a href="https://msdn.microsoft.com/4326547e-85e2-409c-9f36-aa013853dfd9">WPUQueueApc</a>



<a href="https://msdn.microsoft.com/a3385c77-899c-4772-88b9-fb3e0fab54e0">WPUResetEvent</a>



<a href="https://msdn.microsoft.com/d5caa926-1223-4917-85ba-4f79731e955a">WPUSetEvent</a>



<a href="https://msdn.microsoft.com/9ebfe81c-bed6-4bde-b1dd-5eaefbaac9cf">WSPStartup</a>
 

 

