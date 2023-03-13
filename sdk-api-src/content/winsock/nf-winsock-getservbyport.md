---
UID: NF:winsock.getservbyport
title: getservbyport function (winsock.h)
description: The getservbyport function (winsock.h) retrieves service information corresponding to a port and protocol.
helpviewer_keywords: ["_win32_getservbyport_2","getservbyport","getservbyport function [Winsock]","winsock.getservbyport_2","winsock/getservbyport"]
old-location: winsock\getservbyport_2.htm
tech.root: WinSock
ms.assetid: afd63c2d-4f77-49df-aeff-bfe56598fcbf
ms.date: 08/15/2022
ms.keywords: _win32_getservbyport_2, getservbyport, getservbyport function [Winsock], winsock.getservbyport_2, winsock/getservbyport
req.header: winsock.h
req.include-header: Winsock2.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - getservbyport
 - winsock/getservbyport
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
 - getservbyport
---

# getservbyport function


## -description

The 
<b>getservbyport</b> function retrieves service information corresponding to a port and protocol.

## -parameters

### -param port [in]

Port for a service, in network byte order.

### -param proto [in]

Optional pointer to a protocol name. If this is null, 
<b>getservbyport</b> returns the first service entry for which the <i>port</i> matches the <b>s_port</b> of the 
<a href="/windows/desktop/api/winsock/ns-winsock-servent">servent</a> structure. Otherwise, 
<b>getservbyport</b> matches both the <i>port</i> and the <i>proto</i> parameters.

## -returns

If no error occurs, 
<b>getservbyport</b> returns a pointer to the 
<a href="/windows/desktop/api/winsock/ns-winsock-servent">servent</a> structure. Otherwise, it returns a null pointer and a specific error number can be retrieved by calling 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
A successful 
<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a> call must occur before using this function.

</td>
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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAHOST_NOT_FOUND</a></b></dt>
</dl>
</td>
<td width="60%">
Authoritative Answer Service not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSATRY_AGAIN</a></b></dt>
</dl>
</td>
<td width="60%">
A nonauthoritative Service not found, or server failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANO_RECOVERY</a></b></dt>
</dl>
</td>
<td width="60%">
Nonrecoverable errors, the services database is not accessible.

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
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINPROGRESS</a></b></dt>
</dl>
</td>
<td width="60%">
A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>proto</i> parameter is not a valid part of the user address space.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINTR</a></b></dt>
</dl>
</td>
<td width="60%">
A blocking Windows Socket 1.1 call was canceled through 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall">WSACancelBlockingCall</a>.

</td>
</tr>
</table>

## -remarks

The 
<b>getservbyport</b> function returns a pointer to a 
<a href="/windows/desktop/api/winsock/ns-winsock-servent">servent</a> structure as it does in the 
<a href="/windows/desktop/api/winsock/nf-winsock-getservbyname">getservbyname</a> function.

The 
<b>servent</b> structure is allocated by Windows Sockets. The application must never attempt to modify this structure or to free any of its components. Furthermore, only one copy of this structure is allocated per thread, so the application should copy any information it needs before issuing any other Windows Sockets function calls.

<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyport">WSAAsyncGetServByPort</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="/windows/desktop/api/winsock/nf-winsock-getservbyname">getservbyname</a>
