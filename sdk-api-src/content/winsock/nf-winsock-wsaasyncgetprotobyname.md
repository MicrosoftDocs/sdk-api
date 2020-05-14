---
UID: NF:winsock.WSAAsyncGetProtoByName
title: WSAAsyncGetProtoByName function (winsock.h)
description: The WSAAsyncGetProtoByName function asynchronously retrieves protocol information that corresponds to a protocol name.helpviewer_keywords: ["WSAAsyncGetProtoByName","WSAAsyncGetProtoByName function [Winsock]","_win32_wsaasyncgetprotobyname_2","winsock.wsaasyncgetprotobyname_2","winsock/WSAAsyncGetProtoByName"]
old-location: winsock\wsaasyncgetprotobyname_2.htm
tech.root: WinSock
ms.assetid: 747c40fd-5dc1-4533-896e-bc1c4368d7bd
ms.date: 12/05/2018
ms.keywords: WSAAsyncGetProtoByName, WSAAsyncGetProtoByName function [Winsock], _win32_wsaasyncgetprotobyname_2, winsock.wsaasyncgetprotobyname_2, winsock/WSAAsyncGetProtoByName
f1_keywords:
- winsock/WSAAsyncGetProtoByName
dev_langs:
- c++
req.header: winsock.h
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
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Ws2_32.dll
api_name:
- WSAAsyncGetProtoByName
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WSAAsyncGetProtoByName function


## -description


The 
<b>WSAAsyncGetProtoByName</b> function asynchronously retrieves protocol information that corresponds to a protocol name.


## -parameters




### -param hWnd [in]

Handle of the window that will receive a message when the asynchronous request completes.


### -param wMsg [in]

Message to be received when the asynchronous request completes.


### -param name [in]

Pointer to the null-terminated protocol name to be resolved.


### -param buf [out]

Pointer to the data area to receive the 
<a href="https://docs.microsoft.com/windows/desktop/api/winsock/ns-winsock-protoent">protoent</a> data. The data area must be larger than the size of a 
<b>protoent</b> structure because the data area is used by Windows Sockets to contain a 
<b>protoent</b> structure and all of the data that is referenced by members of the 
<b>protoent</b> structure. A buffer of MAXGETHOSTSTRUCT bytes is recommended.


### -param buflen [out]

Size of data area for the <i>buf</i> parameter, in bytes.


## -returns



The return value specifies whether or not the asynchronous operation was successfully initiated. It does not imply success or failure of the operation itself.

If no error occurs, 
<b>WSAAsyncGetProtoByName</b> returns a nonzero value of type HANDLE that is the asynchronous task handle for the request (not to be confused with a Windows HTASK). This value can be used in two ways. It can be used to cancel the operation using 
<a href="https://docs.microsoft.com/windows/desktop/api/winsock/nf-winsock-wsacancelasyncrequest">WSACancelAsyncRequest</a>, or it can be used to match up asynchronous operations and completion messages, by examining the <i>wParam</i> message parameter.

If the asynchronous operation could not be initiated, 
<b>WSAAsyncGetProtoByName</b> returns a zero value, and a specific error number can be retrieved by calling 
<a href="https://docs.microsoft.com/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>.

The following error codes can be set when an application window receives a message. As described above, they can be extracted from the <i>lParam</i> in the reply message using the <b>WSAGETASYNCERROR</b> macro.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
The network subsystem has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOBUFS</a></b></dt>
</dl>
</td>
<td width="60%">
Insufficient buffer space is available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>name</i> or <i>buf</i> parameter is not in a valid part of the process address space.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAHOST_NOT_FOUND</a></b></dt>
</dl>
</td>
<td width="60%">
Authoritative answer protocol not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSATRY_AGAIN</a></b></dt>
</dl>
</td>
<td width="60%">
A nonauthoritative protocol not found, or server failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANO_RECOVERY</a></b></dt>
</dl>
</td>
<td width="60%">
Nonrecoverable errors, the protocols database is not accessible.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANO_DATA</a></b></dt>
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
<td><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANOTINITIALISED</a></td>
<td>A successful 
<a href="https://docs.microsoft.com/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a> call must occur before using this function.</td>
</tr>
<tr>
<td><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETDOWN</a></td>
<td>The network subsystem has failed.</td>
</tr>
<tr>
<td><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINPROGRESS</a></td>
<td>A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.</td>
</tr>
<tr>
<td><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEWOULDBLOCK</a></td>
<td>The asynchronous operation cannot be scheduled at this time due to resource or other constraints within the Windows Sockets implementation.</td>
</tr>
</table>
 




## -remarks



The 
<b>WSAAsyncGetProtoByName</b> function is an asynchronous version of 
<a href="https://docs.microsoft.com/windows/desktop/api/winsock/nf-winsock-getprotobyname">getprotobyname</a>. It is used to retrieve the protocol name and number from the Windows Sockets database corresponding to a given protocol name. Windows Sockets initiates the operation and returns to the caller immediately, passing back an opaque, asynchronous task handle that the application can use to identify the operation. When the operation is completed, the results (if any) are copied into the buffer provided by the caller and a message is sent to the application's window.

When the asynchronous operation has completed, the application window indicated by the <i>hWnd</i> parameter receives message in the <i>wMsg</i> parameter. The <i>wParam</i> parameter contains the asynchronous task handle as returned by the original function call. The high 16 bits of <i>lParam</i> contain any error code. The error code can be any error as defined in Winsock2.h. An error code of zero indicates successful completion of the asynchronous operation.

On successful completion, the buffer specified to the original function call contains a 
<a href="https://docs.microsoft.com/windows/desktop/api/winsock/ns-winsock-protoent">protoent</a> structure. To access the members of this structure, the original buffer address should be cast to a 
<b>protoent</b> structure pointer and accessed as appropriate.

If the error code is <a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOBUFS</a>, the size of the buffer specified by <i>buflen</i> in the original call was too small to contain all the resulting information. In this case, the low 16 bits of <i>lParam</i> contain the size of buffer required to supply all the requisite information. If the application decides that the partial data is inadequate, it can reissue the 
<b>WSAAsyncGetProtoByName</b> function call with a buffer large enough to receive all the desired information (that is, no smaller than the low 16 bits of <i>lParam</i>).

The buffer specified to this function is used by Windows Sockets to construct a 
<a href="https://docs.microsoft.com/windows/desktop/api/winsock/ns-winsock-protoent">protoent</a> structure together with the contents of data areas referenced by members of the same 
<b>protoent</b> structure. To avoid the 
<a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOBUFS</a> error noted above, the application should provide a buffer of at least MAXGETHOSTSTRUCT bytes (as defined in Winsock2.h).

The error code and buffer length should be extracted from the <i>lParam</i> using the macros <b>WSAGETASYNCERROR</b> and <b>WSAGETASYNCBUFLEN</b>, defined in Winsock2.h as:


```cpp
#include <windows.h>

#define WSAGETASYNCBUFLEN(lParam)           LOWORD(lParam)
#define WSAGETASYNCERROR(lParam)            HIWORD(lParam)

```


The use of these macros will maximize the portability of the source code for the application.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winsock/nf-winsock-wsacancelasyncrequest">WSACancelAsyncRequest</a>



<a href="https://docs.microsoft.com/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winsock/nf-winsock-getprotobyname">getprotobyname</a>
 

 

