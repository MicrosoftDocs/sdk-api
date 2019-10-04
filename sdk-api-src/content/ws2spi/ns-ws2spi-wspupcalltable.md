---
UID: NS:ws2spi._WSPUPCALLTABLE
title: WSPUPCALLTABLE (ws2spi.h)
author: windows-sdk-content
description: Contains a table of pointers to service provider upcall functions.
old-location: winsock\wspupcalltable.htm
tech.root: WinSock
ms.assetid: a5abf488-3e78-4e4e-ae5f-201bf0d77fc9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPWSPUPCALLTABLE, FAR * LPWSPUPCALLTABLE, FAR * LPWSPUPCALLTABLE structure [Winsock], WSPUPCALLTABLE, WSPUPCALLTABLE structure [Winsock], winsock.wspupcalltable, ws2spi/FAR * LPWSPUPCALLTABLE, ws2spi/WSPUPCALLTABLE"
ms.topic: struct
f1_keywords: 
 - "ws2spi/WSPUPCALLTABLE"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: WSPUPCALLTABLE, *LPWSPUPCALLTABLE
req.redist: 
ms.custom: 19H1
---

# WSPUPCALLTABLE structure


## -description


The 
<b>WSPUPCALLTABLE</b> structure contains a table of pointers to service provider upcall functions.


## -struct-fields




### -field lpWPUCloseEvent

Type: <b>LPWPUCLOSEEVENT</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wpucloseevent">WPUCloseEvent</a> function. 


### -field lpWPUCloseSocketHandle

Type: <b>LPWPUCLOSESOCKETHANDLE</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wpuclosesockethandle">WPUCloseSocketHandle</a> function. 


### -field lpWPUCreateEvent

Type: <b>LPWPUCREATEEVENT</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wpucreateevent">WPUCreateEvent</a> function. 


### -field lpWPUCreateSocketHandle

Type: <b>LPWPUCREATESOCKETHANDLE</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wpucreatesockethandle">WPUCreateSocketHandle</a> function. 


### -field lpWPUFDIsSet

Type: <b>LPWPUFDISSET</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wpufdisset">WPUFDIsSet</a> function. 


### -field lpWPUGetProviderPath

Type: <b>LPWPUGETPROVIDERPATH</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wpugetproviderpath">WPUGetProviderPath</a> function. 


### -field lpWPUModifyIFSHandle

Type: <b>LPWPUMODIFYIFSHANDLE</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wpumodifyifshandle">WPUModifyIFSHandle</a> function. 


### -field lpWPUPostMessage

Type: <b>LPWPUPOSTMESSAGE</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wpupostmessage">WPUPostMessage</a> function. 


### -field lpWPUQueryBlockingCallback

Type: <b>LPWPUQUERYBLOCKINGCALLBACK</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueryblockingcallback">WPUQueryBlockingCallback</a> function. 


### -field lpWPUQuerySocketHandleContext

Type: <b>LPWPUQUERYSOCKETHANDLECONTEXT</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wpuquerysockethandlecontext">WPUQuerySocketHandleContext</a> function. 


### -field lpWPUQueueApc

Type: <b>LPWPUQUEUEAPC</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc">WPUQueueApc</a> function. 


### -field lpWPUResetEvent

Type: <b>LPWPURESETEVENT</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wpuresetevent">WPUResetEvent</a> function. 


### -field lpWPUSetEvent

Type: <b>LPWPUSETEVENT</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wpusetevent">WPUSetEvent</a> function. 


### -field lpWPUOpenCurrentThread

Type: <b>LPWPUOPENCURRENTTHREAD</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wpuopencurrentthread">WPUOpenCurrentThread</a> function. 


### -field lpWPUCloseThread

Type: <b>LPWPUCLOSETHREAD</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wpuclosethread">WPUCloseThread</a> function. 


## -remarks



The <b>WSPUPCALLTABLE</b> structure contains a table of pointers to service provider upcall functions that are passed to the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wspstartup">WSPStartup</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wpucloseevent">WPUCloseEvent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wpuclosesockethandle">WPUCloseSocketHandle</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wpuclosethread">WPUCloseThread</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wpucreateevent">WPUCreateEvent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wpucreatesockethandle">WPUCreateSocketHandle</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wpufdisset">WPUFDIsSet</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wpugetproviderpath">WPUGetProviderPath</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wpumodifyifshandle">WPUModifyIFSHandle</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wpuopencurrentthread">WPUOpenCurrentThread</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wpupostmessage">WPUPostMessage</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueryblockingcallback">WPUQueryBlockingCallback</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wpuquerysockethandlecontext">WPUQuerySocketHandleContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc">WPUQueueApc</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wpuresetevent">WPUResetEvent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wpusetevent">WPUSetEvent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wspstartup">WSPStartup</a>
 

 

