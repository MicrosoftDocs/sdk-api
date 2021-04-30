---
UID: NF:winsock2.WSAAsyncGetHostByName
title: WSAAsyncGetHostByName function (winsock2.h)
description: The WSAAsyncGetHostByName function asynchronously retrieves host information that corresponds to a host name.Note  The WSAAsyncGetHostByName function is not designed to provide parallel resolution of several names.
helpviewer_keywords: ["WSAAsyncGetHostByName","WSAAsyncGetHostByName function [Winsock]","_win32_wsaasyncgethostbyname_2","winsock.wsaasyncgethostbyname_2","wsipv6ok/WSAAsyncGetHostByName"]
old-location: winsock\wsaasyncgethostbyname_2.htm
tech.root: WinSock
ms.assetid: 1a2b9c76-6e84-4ac2-b5c1-a2268edd0c49
ms.date: 12/05/2018
ms.keywords: WSAAsyncGetHostByName, WSAAsyncGetHostByName function [Winsock], _win32_wsaasyncgethostbyname_2, winsock.wsaasyncgethostbyname_2, wsipv6ok/WSAAsyncGetHostByName
req.header: winsock2.h
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
 - winsock2/WSAAsyncGetHostByName
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

# WSAAsyncGetHostByName function


## -description

The 
<b>WSAAsyncGetHostByName</b> function asynchronously retrieves host information that corresponds to a host name.
<div class="alert"><b>Note</b>  The 
<b>WSAAsyncGetHostByName</b> function is not designed to provide parallel resolution of several names. Therefore, applications that issue several requests should not expect them to be executed concurrently. Alternatively, applications can start another thread and use the 
<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo">getaddrinfo</a> function to resolve names in an IP-version agnostic manner. Developers creating Windows Sockets 2 applications are urged to use the 
<b>getaddrinfo</b> function to enable smooth transition to IPv6 compatibility.</div><div> </div>

## -parameters

### -param hWnd

TBD

### -param wMsg

TBD

### -param name

TBD

### -param buf

TBD

### -param buflen

TBD




#### - a [in]

Handle of the window that will receive a message when the asynchronous request completes.


#### - b [in]

Message to be received when the asynchronous request completes.


#### - c [in]

Pointer to the null-terminated name of the host.


#### - d [out]

Pointer to the data area to receive the 
<a href="/windows/desktop/api/winsock/ns-winsock-hostent">hostent</a> data. The data area must be larger than the size of a 
<b>hostent</b> structure because the specified data area is used by Windows Sockets to contain a 
<b>hostent</b> structure and all of the data referenced by members of the 
<b>hostent</b> structure. A buffer of MAXGETHOSTSTRUCT bytes is recommended.


#### - e [in]

Size of data area for the <i>buf</i> parameter, in bytes.

## -returns

The return value specifies whether or not the asynchronous operation was successfully initiated. It does not imply success or failure of the operation itself.

If no error occurs, 
<b>WSAAsyncGetHostByName</b> returns a nonzero value of type HANDLE that is the asynchronous task handle (not to be confused with a Windows HTASK) for the request. This value can be used in two ways. It can be used to cancel the operation using 
<a href="/windows/desktop/api/winsock/nf-winsock-wsacancelasyncrequest">WSACancelAsyncRequest</a>, or it can be used to match up asynchronous operations and completion messages by examining the <i>wParam</i> message parameter.

If the asynchronous operation could not be initiated, 
<b>WSAAsyncGetHostByName</b> returns a zero value, and a specific error number can be retrieved by calling 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>.

The following error codes can be set when an application window receives a message. As described above, they can be extracted from the <i>lParam</i> in the reply message using the WSAGETASYNCERROR macro.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
The network subsystem has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOBUFS</a></b></dt>
</dl>
</td>
<td width="60%">
Insufficient buffer space is available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>name</i> or <i>buf</i> parameter is not in a valid part of the process address space.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAHOST_NOT_FOUND</a></b></dt>
</dl>
</td>
<td width="60%">
Authoritative answer host not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSATRY_AGAIN</a></b></dt>
</dl>
</td>
<td width="60%">
A nonauthoritative host not found, or SERVERFAIL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANO_RECOVERY</a></b></dt>
</dl>
</td>
<td width="60%">
Nonrecoverable errors: FORMERR, REFUSED, NOTIMP.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANO_DATA</a></b></dt>
</dl>
</td>
<td width="60%">
Valid name, no data record of requested type.

</td>
</tr>
</table>
 

The following errors can occur at the time of the function call, and indicate that the asynchronous operation could not be initiated.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANOTINITIALISED</a></td>
<td>A successful 
<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a> call must occur before using this function.</td>
</tr>
<tr>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETDOWN</a></td>
<td>The network subsystem has failed.</td>
</tr>
<tr>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINPROGRESS</a></td>
<td>A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.</td>
</tr>
<tr>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEWOULDBLOCK</a></td>
<td>The asynchronous operation cannot be scheduled at this time due to resource or other constraints within the Windows Sockets implementation.</td>
</tr>
</table>

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