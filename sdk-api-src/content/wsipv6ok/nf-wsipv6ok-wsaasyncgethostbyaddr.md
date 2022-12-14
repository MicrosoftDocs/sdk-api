---
UID: NF:wsipv6ok.WSAAsyncGetHostByAddr
title: WSAAsyncGetHostByAddr macro (wsipv6ok.h)
description: The WSAAsyncGetHostByAddr macro function (wsipv6ok.h) asynchronously retrieves host information that corresponds to an address.
helpviewer_keywords: ["WSAAsyncGetHostByAddr","WSAAsyncGetHostByAddr function [Winsock]","_win32_wsaasyncgethostbyaddr_2","winsock.wsaasyncgethostbyaddr_2","wsipv6ok/WSAAsyncGetHostByAddr"]
old-location: winsock\wsaasyncgethostbyaddr_2.htm
tech.root: WinSock
ms.assetid: 814cbb2e-8dd2-44b0-b8be-cfc5491bdc49
ms.date: 08/16/2022
ms.keywords: WSAAsyncGetHostByAddr, WSAAsyncGetHostByAddr function [Winsock], _win32_wsaasyncgethostbyaddr_2, winsock.wsaasyncgethostbyaddr_2, wsipv6ok/WSAAsyncGetHostByAddr
req.header: wsipv6ok.h
req.include-header: Winsock2.h, Winsock.h
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
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WSAAsyncGetHostByAddr
 - wsipv6ok/WSAAsyncGetHostByAddr
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - WSAAsyncGetHostByAddr
---

# WSAAsyncGetHostByAddr macro


## -description

The 
<b>WSAAsyncGetHostByAddr</b> function asynchronously retrieves host information that corresponds to an address.
<div class="alert"><b>Note</b>  The 
<b>WSAAsyncGetHostByAddr</b> function is not designed to provide parallel resolution of several addresses. Therefore, applications that issue several requests should not expect them to be executed concurrently. Alternatively, applications can start another thread and use the 
<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getnameinfo">getnameinfo</a> function to resolve addresses in an IP-version agnostic manner. Developers creating Windows Sockets 2 applications are urged to use the 
<b>getnameinfo</b> function to enable smooth transition to IPv6 compatibility.</div><div> </div>

## -parameters

### -param a [in]

Handle of the window that will receive a message when the asynchronous request completes.

### -param b [in]

Message to be received when the asynchronous request completes.

### -param c [in]

Pointer to the network address for the host. Host addresses are stored in network byte order.

### -param d [in]

Length of the address, in bytes.

### -param e [in]

Type of the address.

### -param f [out]

Pointer to the data area to receive the 
<a href="/windows/desktop/api/winsock/ns-winsock-hostent">hostent</a> data. The data area must be larger than the size of a 
<b>hostent</b> structure because the data area is used by Windows Sockets to contain a 
<b>hostent</b> structure and all of the data referenced by members of the 
<b>hostent</b> structure. A buffer of MAXGETHOSTSTRUCT bytes is recommended.

### -param g [in]

Size of data area for the <i>buf</i> parameter, in bytes.

## -remarks

The 
<b>WSAAsyncGetHostByAddr</b> function is an asynchronous version of 
<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr">gethostbyaddr</a>. It is used to retrieve the host name and address information that corresponds to a network address. Windows Sockets initiates the operation and returns to the caller immediately, passing back an opaque, asynchronous task handle that the application can use to identify the operation. When the operation is completed, the results (if any) are copied into the buffer provided by the caller and a message is sent to the application's window.

When the asynchronous operation has completed, the application window indicated by the <i>hWnd</i> parameter receives message in the <i>wMsg</i> parameter. The <i>wParam</i> parameter contains the asynchronous task handle as returned by the original function call. The high 16 bits of <i>lParam</i> contain any error code. The error code can be any error as defined in Winsock2.h. An error code of zero indicates successful completion of the asynchronous operation.

On successful completion, the buffer specified to the original function call contains a 
<a href="/windows/desktop/api/winsock/ns-winsock-hostent">hostent</a> structure. To access the members of this structure, the original buffer address is cast to a 
<b>hostent</b> structure pointer and accessed as appropriate.

If the error code is 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOBUFS</a>, the size of the buffer specified by <i>buflen</i> in the original call was too small to contain all the resulting information. In this case, the low 16 bits of <i>lParam</i> contain the size of buffer required to supply all the requisite information. If the application decides that the partial data is inadequate, it can reissue the 
<b>WSAAsyncGetHostByAddr</b> function call with a buffer large enough to receive all the desired information (that is, no smaller than the low 16 bits of <i>lParam</i>).

The buffer specified to this function is used by Windows Sockets to construct a structure together with the contents of data areas referenced by members of the same 
<a href="/windows/desktop/api/winsock/ns-winsock-hostent">hostent</a> structure. To avoid the 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOBUFS</a> error, the application should provide a buffer of at least MAXGETHOSTSTRUCT bytes (as defined in Winsock2.h).

The error code and buffer length should be extracted from the <i>lParam</i> using the macros <b>WSAGETASYNCERROR</b> and <b>WSAGETASYNCBUFLEN</b>, defined in Winsock2.h as:


```cpp
#include <windows.h>

#define WSAGETASYNCBUFLEN(lParam)           LOWORD(lParam)
#define WSAGETASYNCERROR(lParam)            HIWORD(lParam)

```


The use of these macros will maximize the portability of the source code for the application.

## -see-also

<a href="/windows/desktop/api/winsock/nf-winsock-wsacancelasyncrequest">WSACancelAsyncRequest</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo">getaddrinfo</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr">gethostbyaddr</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getnameinfo">getnameinfo</a>



<a href="/windows/desktop/api/winsock/ns-winsock-hostent">hostent</a>
