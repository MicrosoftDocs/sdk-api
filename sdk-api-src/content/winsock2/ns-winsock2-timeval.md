---
UID: NS:winsock2.timeval
title: TIMEVAL (winsock2.h)
author: windows-sdk-content
description: The timeval structure is used to specify a time interval. It is associated with the Berkeley Software Distribution (BSD) Time.h header file.
old-location: winsock\timeval_2.htm
tech.root: WinSock
ms.assetid: 3024c961-bb47-40ac-a49c-b12cd431e4e7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPTIMEVAL, *PTIMEVAL, TIMEVAL, _win32_timeval_2, timeval, timeval structure [Winsock], winsock.timeval_2, winsock/timeval"
ms.topic: struct
f1_keywords: 
 - "winsock2/timeval"
dev_langs:
 - c++
req.header: winsock2.h
req.include-header: Winsock2.h
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
 - winsock.h
api_name:
 - timeval
targetos: Windows
req.typenames: TIMEVAL, *PTIMEVAL, *LPTIMEVAL
req.redist: 
ms.custom: 19H1
---

# TIMEVAL structure


## -description


The 
<b>timeval</b> structure is used to specify a time interval. It is associated with the Berkeley Software Distribution (BSD) <i>Time.h</i> header file.


## -struct-fields




### -field tv_sec

Time interval, in seconds.


### -field tv_usec

Time interval, in microseconds. This value is used in combination with the <b>tv_sec</b> member to represent time interval values  that are not a multiple of seconds. 


## -remarks



The <b>timeval</b> structure is used in Windows Sockets by the <a href="https://docs.microsoft.com/windows/desktop/api/winsock2/nf-winsock2-select">select</a> function to specify the maximum time the function can take to complete. The time interval is a combination of the values in <b>tv_sec</b> and <b>tv_usec</b> members.

Several functions are added on Windows Vista and later that use the  <b>timeval</b> structure. These functions include <a href="https://docs.microsoft.com/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a>, <a href="https://docs.microsoft.com/windows/desktop/api/ws2tcpip/nf-ws2tcpip-setaddrinfoexa">SetAddrInfoEx</a>, <a href="https://docs.microsoft.com/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbylist">WSAConnectByList</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamea">WSAConnectByName</a>. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2tcpip/nf-ws2tcpip-setaddrinfoexa">SetAddrInfoEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbylist">WSAConnectByList</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamea">WSAConnectByName</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winsock/ns-winsock-linger">linger</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winsock2/nf-winsock2-select">select</a>
 

 

