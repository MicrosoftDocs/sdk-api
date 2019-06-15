---
UID: NS:ws2spi._WSATHREADID
title: WSATHREADID (ws2spi.h)
author: windows-sdk-content
description: The WSATHREADID structure enables a provider to identify a thread on which asynchronous procedure calls (APCs) can be queued using the WPUQueueApc function.
old-location: winsock\wsathreadid_2.htm
tech.root: WinSock
ms.assetid: eeea1139-1d14-4f53-bd64-833539b53bed
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPWSATHREADID, LPWSATHREADID, LPWSATHREADID structure pointer [Winsock], WSATHREADID, WSATHREADID structure [Winsock], _win32_wsathreadid_2, winsock.wsathreadid_2, ws2spi/LPWSATHREADID, ws2spi/WSATHREADID"
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
 - WSATHREADID
product: Windows
targetos: Windows
req.typenames: WSATHREADID, *LPWSATHREADID
req.redist: 
ms.custom: 19H1
---

# WSATHREADID structure


## -description


The 
<b>WSATHREADID</b> structure enables a provider to identify a thread on which asynchronous procedure calls (APCs) can be queued using the 
<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc">WPUQueueApc</a> function.


## -struct-fields




### -field ThreadHandle

Handle to the thread ID.


### -field Reserved

Reserved.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc">WPUQueueApc</a>



<a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566296(v%3dvs.85)"> WSPIoctl</a>



<a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566309(v%3dvs.85)">WSPRecv</a>



<a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566316(v%3dvs.85)">WSPSend</a>
 

 

