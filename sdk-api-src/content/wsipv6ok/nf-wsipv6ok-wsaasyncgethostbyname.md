---
UID: NF:wsipv6ok.WSAAsyncGetHostByName
title: WSAAsyncGetHostByName macro (wsipv6ok.h)
description: The WSAAsyncGetHostByName macro function (wsipv6ok.h) asynchronously retrieves host information that corresponds to a host name.
helpviewer_keywords: ["WSAAsyncGetHostByName","WSAAsyncGetHostByName function [Winsock]","_win32_wsaasyncgethostbyname_2","winsock.wsaasyncgethostbyname_2","wsipv6ok/WSAAsyncGetHostByName"]
old-location: winsock\wsaasyncgethostbyname_2.htm
tech.root: WinSock
ms.assetid: 1a2b9c76-6e84-4ac2-b5c1-a2268edd0c49
ms.date: 08/16/2022
ms.keywords: WSAAsyncGetHostByName, WSAAsyncGetHostByName function [Winsock], _win32_wsaasyncgethostbyname_2, winsock.wsaasyncgethostbyname_2, wsipv6ok/WSAAsyncGetHostByName
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
 - WSAAsyncGetHostByName
 - wsipv6ok/WSAAsyncGetHostByName
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
 - WSAAsyncGetHostByName
---

# WSAAsyncGetHostByName macro


## -description

The 
<b>WSAAsyncGetHostByName</b> function asynchronously retrieves host information that corresponds to a host name.
<div class="alert"><b>Note</b>  The 
<b>WSAAsyncGetHostByName</b> function is not designed to provide parallel resolution of several names. Therefore, applications that issue several requests should not expect them to be executed concurrently. Alternatively, applications can start another thread and use the 
<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo">getaddrinfo</a> function to resolve names in an IP-version agnostic manner. Developers creating Windows Sockets 2 applications are urged to use the 
<b>getaddrinfo</b> function to enable smooth transition to IPv6 compatibility.</div><div> </div>

## -parameters

### -param a [in]

Handle of the window that will receive a message when the asynchronous request completes.

### -param b [in]

Message to be received when the asynchronous request completes.

### -param c [in]

Pointer to the null-terminated name of the host.

### -param d [out]

Pointer to the data area to receive the 
<a href="/windows/desktop/api/winsock/ns-winsock-hostent">hostent</a> data. The data area must be larger than the size of a 
<b>hostent</b> structure because the specified data area is used by Windows Sockets to contain a 
<b>hostent</b> structure and all of the data referenced by members of the 
<b>hostent</b> structure. A buffer of MAXGETHOSTSTRUCT bytes is recommended.

### -param e [in]

Size of data area for the <i>buf</i> parameter, in bytes.

## -remarks

The 
<b>WSAAsyncGetHostByName</b> function is an asynchronous version of 
<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname">gethostbyname</a>, and is used to retrieve host name and address information corresponding to a host name. Windows Sockets initiates the operation and returns to the caller immediately, passing back an opaque asynchronous task handle that which the application can use to identify the operation. When the operation is completed, the results (if any) are copied into the buffer provided by the caller and a message is sent to the application's window.

When the asynchronous operation has completed, the application window indicated by the <i>hWnd</i> parameter receives message in the <i>wMsg</i> parameter. The <i>wParam</i> parameter contains the asynchronous task handle as returned by the original function call. The high 16 bits of <i>lParam</i> contain any error code. The error code can be any error as defined in Winsock2.h. An error code of zero indicates successful completion of the asynchronous operation.

On successful completion, the buffer specified to the original function call contains a 
<a href="/windows/desktop/api/winsock/ns-winsock-hostent">hostent</a> structure. To access the elements of this structure, the original buffer address should be cast to a 
<b>hostent</b> structure pointer and accessed as appropriate.

If the error code is 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOBUFS</a>, the size of the buffer specified by <i>buflen</i> in the original call was too small to contain all the resulting information. In this case, the low 16 bits of <i>lParam</i> contain the size of buffer required to supply all the requisite information. If the application decides that the partial data is inadequate, it can reissue the 
<b>WSAAsyncGetHostByName</b> function call with a buffer large enough to receive all the desired information (that is, no smaller than the low 16 bits of <i>lParam</i>).

The buffer specified to this function is used by Windows Sockets to construct a 
<a href="/windows/desktop/api/winsock/ns-winsock-hostent">hostent</a> structure together with the contents of data areas referenced by members of the same 
<b>hostent</b> structure. To avoid the 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOBUFS</a> error, the application should provide a buffer of at least MAXGETHOSTSTRUCT bytes (as defined in Winsock2.h).

The error code and buffer length should be extracted from the <i>lParam</i> using the macros <b>WSAGETASYNCERROR</b> and <b>WSAGETASYNCBUFLEN</b>, defined in Winsock2.h as:


```cpp
#include <windows.h>

#define WSAGETASYNCBUFLEN(lParam)           LOWORD(lParam)
#define WSAGETASYNCERROR(lParam)            HIWORD(lParam)

```


The use of these macros will maximize the portability of the source code for the application.

<b>WSAAsyncGetHostByName</b> is guaranteed to resolve the string returned by a successful call to 
<a href="/windows/desktop/api/winsock/nf-winsock-gethostname">gethostname</a>.

## -see-also

<a href="/windows/desktop/api/winsock/nf-winsock-wsacancelasyncrequest">WSACancelAsyncRequest</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo">getaddrinfo</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname">gethostbyname</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getnameinfo">getnameinfo</a>



<a href="/windows/desktop/api/winsock/ns-winsock-hostent">hostent</a>
