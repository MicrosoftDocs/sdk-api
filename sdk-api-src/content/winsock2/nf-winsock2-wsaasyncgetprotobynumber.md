---
UID: NF:winsock2.WSAAsyncGetProtoByNumber
title: WSAAsyncGetProtoByNumber function
author: windows-sdk-content
description: The WSAAsyncGetProtoByNumber function asynchronously retrieves protocol information that corresponds to a protocol number.
old-location: winsock\wsaasyncgetprotobynumber_2.htm
tech.root: winsock
ms.assetid: 10f28345-c178-47c0-9d0f-87f6743131d9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WSAAsyncGetProtoByNumber, WSAAsyncGetProtoByNumber function [Winsock], _win32_wsaasyncgetprotobynumber_2, winsock.wsaasyncgetprotobynumber_2, winsock/WSAAsyncGetProtoByNumber
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - WSAAsyncGetProtoByNumber
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WSAAsyncGetProtoByNumber function


## -description


The 
<b>WSAAsyncGetProtoByNumber</b> function asynchronously retrieves protocol information that corresponds to a protocol number.


## -parameters




### -param hWnd [in]

Handle of the window that will receive a message when the asynchronous request completes.


### -param wMsg [in]

Message to be received when the asynchronous request completes.


### -param number [in]

Protocol number to be resolved, in host byte order.


### -param buf [out]

Pointer to the data area to receive the 
<a href="https://msdn.microsoft.com/8fc729dd-5a73-42a1-9c3f-adc68d83d863">protoent</a> data. The data area must be larger than the size of a 
<b>protoent</b> structure because the data area is used by Windows Sockets to contain a 
<b>protoent</b> structure and all of the data that is referenced by members of the 
<b>protoent</b> structure. A buffer of MAXGETHOSTSTRUCT bytes is recommended.


### -param buflen [in]

Size of data area for the <i>buf</i> parameter, in bytes.


## -returns



The return value specifies whether or not the asynchronous operation was successfully initiated. It does not imply success or failure of the operation itself.

If no error occurs, 
<b>WSAAsyncGetProtoByNumber</b> returns a nonzero value of type <b>HANDLE</b> that is the asynchronous task handle for the request (not to be confused with a Windows HTASK). This value can be used in two ways. It can be used to cancel the operation using 
<a href="https://msdn.microsoft.com/0e53eccf-ef85-43ec-a02c-12896471a7a9">WSACancelAsyncRequest</a>, or it can be used to match up asynchronous operations and completion messages, by examining the <i>wParam</i> message parameter.

If the asynchronous operation could not be initiated, 
<b>WSAAsyncGetProtoByNumber</b> returns a zero value, and a specific error number can be retrieved by calling 
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
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAENETDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
The network subsystem has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAENOBUFS</a></b></dt>
</dl>
</td>
<td width="60%">
Insufficient buffer space is available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>buf</i> parameter is not in a valid part of the process address space.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAHOST_NOT_FOUND</a></b></dt>
</dl>
</td>
<td width="60%">
Authoritative answer protocol not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSATRY_AGAIN</a></b></dt>
</dl>
</td>
<td width="60%">
Nonauthoritative protocol not found, or server failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSANO_RECOVERY</a></b></dt>
</dl>
</td>
<td width="60%">
Nonrecoverable errors, the protocols database is not accessible.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSANO_DATA</a></b></dt>
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
<td><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSANOTINITIALISED</a></td>
<td>A successful 
<a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a> call must occur before using this function.</td>
</tr>
<tr>
<td><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAENETDOWN</a></td>
<td>The network subsystem has failed.</td>
</tr>
<tr>
<td><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEINPROGRESS</a></td>
<td>A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.</td>
</tr>
<tr>
<td><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEWOULDBLOCK</a></td>
<td>The asynchronous operation cannot be scheduled at this time due to resource or other constraints within the Windows Sockets implementation.</td>
</tr>
</table>
 




## -remarks



The 
<b>WSAAsyncGetProtoByNumber</b> function is an asynchronous version of 
<a href="https://msdn.microsoft.com/f1f55ab7-01ca-4ed7-b8f9-e7ddbaa95855">getprotobynumber</a>, and is used to retrieve the protocol name and number corresponding to a protocol number. Windows Sockets initiates the operation and returns to the caller immediately, passing back an opaque, asynchronous task handle that the application can use to identify the operation. When the operation is completed, the results (if any) are copied into the buffer provided by the caller and a message is sent to the application's window.

When the asynchronous operation has completed, the application window indicated by the <i>hWnd</i> parameter receives message in the <i>wMsg</i> parameter. The <i>wParam</i> parameter contains the asynchronous task handle as returned by the original function call. The high 16 bits of <i>lParam</i> contain any error code. The error code can be any error as defined in Winsock2.h. An error code of zero indicates successful completion of the asynchronous operation.

On successful completion, the buffer specified to the original function call contains a 
<a href="https://msdn.microsoft.com/8fc729dd-5a73-42a1-9c3f-adc68d83d863">protoent</a> structure. To access the members of this structure, the original buffer address is cast to a 
<b>protoent</b> structure pointer and accessed as appropriate.

If the error code is 
<a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAENOBUFS</a>, the size of the buffer specified by <i>buflen</i> in the original call was too small to contain all the resulting information. In this case, the low 16 bits of <i>lParam</i> contain the size of buffer required to supply all the requisite information. If the application decides that the partial data is inadequate, it can reissue the 
<b>WSAAsyncGetProtoByNumber</b> function call with a buffer large enough to receive all the desired information (that is, no smaller than the low 16 bits of <i>lParam</i>).

The buffer specified to this function is used by Windows Sockets to construct a 
<a href="https://msdn.microsoft.com/8fc729dd-5a73-42a1-9c3f-adc68d83d863">protoent</a> structure together with the contents of data areas referenced by members of the same 
<b>protoent</b> structure. To avoid the WSAENOBUFS error noted above, the application should provide a buffer of at least MAXGETHOSTSTRUCT bytes (as defined in Winsock2.h).

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



<a href="https://msdn.microsoft.com/f1f55ab7-01ca-4ed7-b8f9-e7ddbaa95855">getprotobynumber</a>
 

 

