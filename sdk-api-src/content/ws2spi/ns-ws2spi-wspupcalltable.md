---
UID: NS:ws2spi._WSPUPCALLTABLE
title: WSPUPCALLTABLE (ws2spi.h)
description: Contains a table of pointers to service provider upcall functions.
helpviewer_keywords: ["*LPWSPUPCALLTABLE","FAR * LPWSPUPCALLTABLE","FAR * LPWSPUPCALLTABLE structure [Winsock]","WSPUPCALLTABLE","WSPUPCALLTABLE structure [Winsock]","winsock.wspupcalltable","ws2spi/FAR * LPWSPUPCALLTABLE","ws2spi/WSPUPCALLTABLE"]
old-location: winsock\wspupcalltable.htm
tech.root: WinSock
ms.assetid: a5abf488-3e78-4e4e-ae5f-201bf0d77fc9
ms.date: 12/05/2018
ms.keywords: '*LPWSPUPCALLTABLE, FAR * LPWSPUPCALLTABLE, FAR * LPWSPUPCALLTABLE structure [Winsock], WSPUPCALLTABLE, WSPUPCALLTABLE structure [Winsock], winsock.wspupcalltable, ws2spi/FAR * LPWSPUPCALLTABLE, ws2spi/WSPUPCALLTABLE'
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
targetos: Windows
req.typenames: WSPUPCALLTABLE, *LPWSPUPCALLTABLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSPUPCALLTABLE
 - ws2spi/_WSPUPCALLTABLE
 - LPWSPUPCALLTABLE
 - ws2spi/LPWSPUPCALLTABLE
 - WSPUPCALLTABLE
 - ws2spi/WSPUPCALLTABLE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ws2spi.h
api_name:
 - WSPUPCALLTABLE
---

# WSPUPCALLTABLE structure


## -description

The 
**WSPUPCALLTABLE** structure contains a table of pointers to service provider upcall functions.

## -struct-fields

### -field lpWPUCloseEvent

Type: **LPWPUCLOSEEVENT**

A pointer to the <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpucloseevent">WPUCloseEvent</a> function.

### -field lpWPUCloseSocketHandle

Type: **LPWPUCLOSESOCKETHANDLE**

A pointer to the <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpuclosesockethandle">WPUCloseSocketHandle</a> function.

### -field lpWPUCreateEvent

Type: **LPWPUCREATEEVENT**

A pointer to the <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpucreateevent">WPUCreateEvent</a> function.

### -field lpWPUCreateSocketHandle

Type: **LPWPUCREATESOCKETHANDLE**

A pointer to the <a href="/windows/win32/api/ws2spi/nf-ws2spi-wpucreatesockethandle">WPUCreateSocketHandle</a> function.

### -field lpWPUFDIsSet

Type: **LPWPUFDISSET**

A pointer to the <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpufdisset">WPUFDIsSet</a> function.

### -field lpWPUGetProviderPath

Type: **LPWPUGETPROVIDERPATH**

A pointer to the <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpugetproviderpath">WPUGetProviderPath</a> function.

### -field lpWPUModifyIFSHandle

Type: **LPWPUMODIFYIFSHANDLE**

A pointer to the <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpumodifyifshandle">WPUModifyIFSHandle</a> function.

### -field lpWPUPostMessage

Type: **LPWPUPOSTMESSAGE**

A pointer to the <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpupostmessage">WPUPostMessage</a> function.

### -field lpWPUQueryBlockingCallback

Type: **LPWPUQUERYBLOCKINGCALLBACK**

A pointer to the <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueryblockingcallback">WPUQueryBlockingCallback</a> function.

### -field lpWPUQuerySocketHandleContext

Type: **LPWPUQUERYSOCKETHANDLECONTEXT**

A pointer to the <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpuquerysockethandlecontext">WPUQuerySocketHandleContext</a> function.

### -field lpWPUQueueApc

Type: **LPWPUQUEUEAPC**

A pointer to the <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc">WPUQueueApc</a> function.

### -field lpWPUResetEvent

Type: **LPWPURESETEVENT**

A pointer to the <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpuresetevent">WPUResetEvent</a> function.

### -field lpWPUSetEvent

Type: **LPWPUSETEVENT**

A pointer to the <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpusetevent">WPUSetEvent</a> function.

### -field lpWPUOpenCurrentThread

Type: **LPWPUOPENCURRENTTHREAD**

A pointer to the <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpuopencurrentthread">WPUOpenCurrentThread</a> function.

### -field lpWPUCloseThread

Type: **LPWPUCLOSETHREAD**

A pointer to the <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpuclosethread">WPUCloseThread</a> function.

## -remarks

The **WSPUPCALLTABLE** structure contains a table of pointers to service provider upcall functions that are passed to the <a href="/windows/win32/api/ws2spi/nf-ws2spi-wspstartup">WSPStartup</a> function.

## -see-also

<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpucloseevent">WPUCloseEvent</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpuclosesockethandle">WPUCloseSocketHandle</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpuclosethread">WPUCloseThread</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpucreateevent">WPUCreateEvent</a>



<a href="/windows/win32/api/ws2spi/nf-ws2spi-wpucreatesockethandle">WPUCreateSocketHandle</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpufdisset">WPUFDIsSet</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpugetproviderpath">WPUGetProviderPath</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpumodifyifshandle">WPUModifyIFSHandle</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpuopencurrentthread">WPUOpenCurrentThread</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpupostmessage">WPUPostMessage</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueryblockingcallback">WPUQueryBlockingCallback</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpuquerysockethandlecontext">WPUQuerySocketHandleContext</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc">WPUQueueApc</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpuresetevent">WPUResetEvent</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpusetevent">WPUSetEvent</a>



<a href="/windows/win32/api/ws2spi/nf-ws2spi-wspstartup">WSPStartup</a>

