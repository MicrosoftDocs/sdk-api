---
UID: NF:winsock.gethostname
title: gethostname function (winsock.h)
description: The gethostname function (winsock.h) retrieves the standard host name for the local computer.
helpviewer_keywords: ["_win32_gethostname_2","gethostname","gethostname function [Winsock]","winsock.gethostname_2","winsock/gethostname"]
old-location: winsock\gethostname_2.htm
tech.root: WinSock
ms.assetid: 8fa40b60-0e93-493b-aee1-cea6cf595707
ms.date: 08/15/2022
ms.keywords: _win32_gethostname_2, gethostname, gethostname function [Winsock], winsock.gethostname_2, winsock/gethostname
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
 - gethostname
 - winsock/gethostname
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
 - gethostname
---

# gethostname function


## -description

The 
<b>gethostname</b> function retrieves the standard host name for the local computer.

## -parameters

### -param name [out]

A pointer to a buffer that receives the local host name.

### -param namelen [in]

The length, in bytes, of the buffer pointed to by the <i>name</i> parameter.

## -returns

If no error occurs, 
<b>gethostname</b> returns zero. Otherwise, it returns SOCKET_ERROR and a specific error code can be retrieved by calling 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>name</i> parameter is a <b>NULL</b> pointer or is not a valid part of the user address space. This error is also returned if the buffer size specified by <i>namelen</i> parameter is too small to hold the complete host name.

</td>
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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINPROGRESS</a></b></dt>
</dl>
</td>
<td width="60%">
A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.

</td>
</tr>
</table>

## -remarks

The 
<b>gethostname</b> function returns the name of the local host into the buffer specified by the <i>name</i> parameter. The host name is returned as a <b>null</b>-terminated string. The form of the host name is dependent on the Windows Sockets provider—it can be a simple host name, or it can be a fully qualified domain name. However, it is guaranteed that the name returned will be successfully parsed by 
<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname">gethostbyname</a> and 
<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-wsaasyncgethostbyname">WSAAsyncGetHostByName</a>.

The maximum length of the name returned in the buffer pointed to by the <i>name</i> parameter is dependent on the namespace provider.

If the 
<b>gethostname</b> function is used on a cluster resource on Windows Server 2008, Windows Server 2003, or 
  Windows 2000 Server and the _CLUSTER_NETWORK_NAME_ environment variable is defined, then the value in this environment variable overrides the actual hostname and is returned. On a cluster resource, the _CLUSTER_NETWORK_NAME_ environment variable contains the name of the cluster.

The 
<b>gethostname</b> function queries namespace providers to determine the local host name using the SVCID_HOSTNAME GUID defined in the <i>Svgguid.h</i> header file. If no namespace provider responds, then the 
<b>gethostname</b> function returns the NetBIOS name of the local computer.

The maximum length, in bytes, of the string returned in the buffer pointed to by the <i>name</i> parameter is dependent on the namespace provider, but this string must be 256 bytes or less. So if a buffer of 256 bytes is passed in the <i>name</i> parameter and the <i>namelen</i> parameter is set to 256, the buffer size will always be adequate.


<div class="alert"><b>Note</b>  If no local host name has been configured, 
<b>gethostname</b> must succeed and return a token host name that 
<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname">gethostbyname</a> or 
<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-wsaasyncgethostbyname">WSAAsyncGetHostByName</a> can resolve.</div>
<div> </div>


<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfow">GetAddrInfoW</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-wsaasyncgethostbyname">WSAAsyncGetHostByName</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname">gethostbyname</a>
