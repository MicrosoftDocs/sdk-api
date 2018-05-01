---
UID: NS:ws2spi._WSATHREADID
title: "_WSATHREADID"
author: windows-driver-content
description: The WSATHREADID structure enables a provider to identify a thread on which asynchronous procedure calls (APCs) can be queued using the WPUQueueApc function.
old-location: winsock\wsathreadid_2.htm
old-project: WinSock
ms.assetid: eeea1139-1d14-4f53-bd64-833539b53bed
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: "*LPWSATHREADID, LPWSATHREADID, LPWSATHREADID structure pointer [Winsock], WSATHREADID, WSATHREADID structure [Winsock], _WSATHREADID, _win32_wsathreadid_2, winsock.wsathreadid_2, ws2spi/LPWSATHREADID, ws2spi/WSATHREADID"
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
req.typenames: WSATHREADID, *LPWSATHREADID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ws2spi.h
api_name:
-	WSATHREADID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSATHREADID structure


## -description



			The 
<b>WSATHREADID</b> structure enables a provider to identify a thread on which asynchronous procedure calls (APCs) can be queued using the 
<a href="https://msdn.microsoft.com/4326547e-85e2-409c-9f36-aa013853dfd9">WPUQueueApc</a> function.


## -struct-fields




### -field ThreadHandle

Handle to the thread ID.


### -field Reserved

Reserved.


## -see-also




<a href="https://msdn.microsoft.com/4326547e-85e2-409c-9f36-aa013853dfd9">WPUQueueApc</a>



<a href="https://msdn.microsoft.com/098d85e3-8fe2-46c2-966d-deae4b12afd6"> WSPIoctl</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566309">WSPRecv</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566316">WSPSend</a>
 

 

