---
UID: NS:winsock2.timeval
title: TIMEVAL (winsock2.h)
description: The TIMEVAL structure (winsock2.h) is used to specify a time interval. It is associated with the Berkeley Software Distribution (BSD) Time.h header file.  
helpviewer_keywords: ["*LPTIMEVAL","*PTIMEVAL","TIMEVAL","_win32_timeval_2","timeval","timeval structure [Winsock]","winsock.timeval_2","winsock/timeval"]
old-location: winsock\timeval_2.htm
tech.root: WinSock
ms.assetid: 3024c961-bb47-40ac-a49c-b12cd431e4e7
ms.date: 08/03/2022
ms.keywords: '*LPTIMEVAL, *PTIMEVAL, TIMEVAL, _win32_timeval_2, timeval, timeval structure [Winsock], winsock.timeval_2, winsock/timeval'
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
targetos: Windows
req.typenames: TIMEVAL, *PTIMEVAL, *LPTIMEVAL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - timeval
 - winsock2/timeval
 - PTIMEVAL
 - winsock2/PTIMEVAL
 - TIMEVAL
 - winsock2/TIMEVAL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winsock.h
api_name:
 - timeval
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

The <b>timeval</b> structure is used in Windows Sockets by the <a href="/windows/desktop/api/winsock2/nf-winsock2-select">select</a> function to specify the maximum time the function can take to complete. The time interval is a combination of the values in <b>tv_sec</b> and <b>tv_usec</b> members.

Several functions are added on Windows Vista and later that use the  <b>timeval</b> structure. These functions include <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a>, <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-setaddrinfoexa">SetAddrInfoEx</a>, <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbylist">WSAConnectByList</a>, and <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamea">WSAConnectByName</a>.

## -see-also

<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-setaddrinfoexa">SetAddrInfoEx</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbylist">WSAConnectByList</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamea">WSAConnectByName</a>



<a href="/windows/desktop/api/winsock/ns-winsock-linger">linger</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-select">select</a>
