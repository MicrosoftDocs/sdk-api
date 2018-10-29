---
UID: NF:winsock.WSAAsyncGetHostByAddr
title: WSAAsyncGetHostByAddr function
author: windows-sdk-content
description: The WSAAsyncGetHostByAddr function asynchronously retrieves host information that corresponds to an address.Note  The WSAAsyncGetHostByAddr function is not designed to provide parallel resolution of several addresses.
old-location: winsock\wsaasyncgethostbyaddr_2.htm
tech.root: WinSock
ms.assetid: 814cbb2e-8dd2-44b0-b8be-cfc5491bdc49
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: WSAAsyncGetHostByAddr, WSAAsyncGetHostByAddr function [Winsock], _win32_wsaasyncgethostbyaddr_2, winsock.wsaasyncgethostbyaddr_2, wsipv6ok/WSAAsyncGetHostByAddr
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winsock.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - WSAAsyncGetHostByAddr
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WSAAsyncGetHostByAddr function


## -description


The 
<b>WSAAsyncGetHostByAddr</b> function asynchronously retrieves host information that corresponds to an address.
<div class="alert"><b>Note</b>  The 
<b>WSAAsyncGetHostByAddr</b> function is not designed to provide parallel resolution of several addresses. Therefore, applications that issue several requests should not expect them to be executed concurrently. Alternatively, applications can start another thread and use the 
<a href="https://msdn.microsoft.com/7d1fb0ed-cc32-4b38-8ff5-88c2cca4f375">getnameinfo</a> function to resolve addresses in an IP-version agnostic manner. Developers creating Windows Sockets 2 applications are urged to use the 
<b>getnameinfo</b> function to enable smooth transition to IPv6 compatibility.</div><div> </div>

## -parameters




### -param hWnd

TBD


### -param wMsg

TBD


### -param addr

TBD


### -param len

TBD


### -param type

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

Pointer to the network address for the host. Host addresses are stored in network byte order.


#### - d [in]

Length of the address, in bytes.


#### - e [in]

Type of the address.


#### - f [out]

Pointer to the data area to receive the 
<a href="https://msdn.microsoft.com/f194b9d5-dfaf-4a02-95c6-6d06015aad1d">hostent</a> data. The data area must be larger than the size of a 
<b>hostent</b> structure because the data area is used by Windows Sockets to contain a 
<b>hostent</b> structure and all of the data referenced by members of the 
<b>hostent</b> structure. A buffer of MAXGETHOSTSTRUCT bytes is recommended.


#### - g [in]

Size of data area for the <i>buf</i> parameter, in bytes.


## -returns



The return value specifies whether or not the asynchronous operation was successfully initiated. It does not imply success or failure of the operation itself.

If no error occurs, 
<b>WSAAsyncGetHostByAddr</b> returns a nonzero value of type HANDLE that is the asynchronous task handle (not to be confused with a Windows HTASK) for the request. This value can be used in two ways. It can be used to cancel the operation using 
<a href="https://msdn.microsoft.com/0e53eccf-ef85-43ec-a02c-12896471a7a9">WSACancelAsyncRequest</a>, or it can be used to match up asynchronous operations and completion messages by examining the <i>wParam</i> message parameter.

If the asynchronous operation could not be initiated, 
<b>WSAAsyncGetHostByAddr</b> returns a zero value, and a specific error number can be retrieved by calling 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>.

The following error codes can be set when an application window receives a message. As described above, they can be extracted from the <i>lParam</i> in the reply message using the <b>WSAGETASYNCERROR</b> macro.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAENETDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
The network subsystem has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAENOBUFS</a></b></dt>
</dl>
</td>
<td width="60%">
Insufficient buffer space is available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>addr</i> or <i>buf</i> parameter is not in a valid part of the process address space.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAHOST_NOT_FOUND</a></b></dt>
</dl>
</td>
<td width="60%">
Authoritative answer host not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSATRY_AGAIN</a></b></dt>
</dl>
</td>
<td width="60%">
Nonauthoritative host not found, or SERVERFAIL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSANO_RECOVERY</a></b></dt>
</dl>
</td>
<td width="60%">
Nonrecoverable errors: FORMERR, REFUSED, NOTIMP.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSANO_DATA</a></b></dt>
</dl>
</td>
<td width="60%">
Valid name, no data record of requested type.

</td>
</tr>
</table>
 


<div> </div>


The following errors can occur at the time of the function call, and indicate that the asynchronous operation could not be initiated.

<table>
<tr>
<th>Error Code</th>
<th>Meaning</th>
</tr>
<tr>
<td><a href="windows_sockets_error_codes_2.htm">WSANOTINITIALISED</a></td>
<td>A successful 
<a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a> call must occur before using this function.</td>
</tr>
<tr>
<td><a href="windows_sockets_error_codes_2.htm">WSAENETDOWN</a></td>
<td>The network subsystem has failed.</td>
</tr>
<tr>
<td><a href="windows_sockets_error_codes_2.htm">WSAEINPROGRESS</a></td>
<td>A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.</td>
</tr>
<tr>
<td><a href="windows_sockets_error_codes_2.htm">WSAEWOULDBLOCK</a></td>
<td>The asynchronous operation cannot be scheduled at this time due to resource or other constraints within the Windows Sockets implementation.</td>
</tr>
</table>
 




## -remarks



The 
<b>WSAAsyncGetHostByAddr</b> function is an asynchronous version of 
<a href="https://msdn.microsoft.com/303023e1-a486-4457-80f6-8aa80f6b2c79">gethostbyaddr</a>. It is used to retrieve the host name and address information that corresponds to a network address. Windows Sockets initiates the operation and returns to the caller immediately, passing back an opaque, asynchronous task handle that the application can use to identify the operation. When the operation is completed, the results (if any) are copied into the buffer provided by the caller and a message is sent to the application's window.

When the asynchronous operation has completed, the application window indicated by the <i>hWnd</i> parameter receives message in the <i>wMsg</i> parameter. The <i>wParam</i> parameter contains the asynchronous task handle as returned by the original function call. The high 16 bits of <i>lParam</i> contain any error code. The error code can be any error as defined in Winsock2.h. An error code of zero indicates successful completion of the asynchronous operation.

On successful completion, the buffer specified to the original function call contains a 
<a href="https://msdn.microsoft.com/f194b9d5-dfaf-4a02-95c6-6d06015aad1d">hostent</a> structure. To access the members of this structure, the original buffer address is cast to a 
<b>hostent</b> structure pointer and accessed as appropriate.

If the error code is 
<a href="windows_sockets_error_codes_2.htm">WSAENOBUFS</a>, the size of the buffer specified by <i>buflen</i> in the original call was too small to contain all the resulting information. In this case, the low 16 bits of <i>lParam</i> contain the size of buffer required to supply all the requisite information. If the application decides that the partial data is inadequate, it can reissue the 
<b>WSAAsyncGetHostByAddr</b> function call with a buffer large enough to receive all the desired information (that is, no smaller than the low 16 bits of <i>lParam</i>).

The buffer specified to this function is used by Windows Sockets to construct a structure together with the contents of data areas referenced by members of the same 
<a href="https://msdn.microsoft.com/f194b9d5-dfaf-4a02-95c6-6d06015aad1d">hostent</a> structure. To avoid the 
<a href="windows_sockets_error_codes_2.htm">WSAENOBUFS</a> error, the application should provide a buffer of at least MAXGETHOSTSTRUCT bytes (as defined in Winsock2.h).

The error code and buffer length should be extracted from the <i>lParam</i> using the macros <b>WSAGETASYNCERROR</b> and <b>WSAGETASYNCBUFLEN</b>, defined in Winsock2.h as:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;

#define WSAGETASYNCBUFLEN(lParam)           LOWORD(lParam)
#define WSAGETASYNCERROR(lParam)            HIWORD(lParam)
</pre>
</td>
</tr>
</table></span></div>
The use of these macros will maximize the portability of the source code for the application.




## -see-also




<a href="https://msdn.microsoft.com/0e53eccf-ef85-43ec-a02c-12896471a7a9">WSACancelAsyncRequest</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>



<a href="https://msdn.microsoft.com/7034b866-346e-4a3b-b81b-72816d95b1d6">getaddrinfo</a>



<a href="https://msdn.microsoft.com/303023e1-a486-4457-80f6-8aa80f6b2c79">gethostbyaddr</a>



<a href="https://msdn.microsoft.com/7d1fb0ed-cc32-4b38-8ff5-88c2cca4f375">getnameinfo</a>



<a href="https://msdn.microsoft.com/f194b9d5-dfaf-4a02-95c6-6d06015aad1d">hostent</a>
 

 

