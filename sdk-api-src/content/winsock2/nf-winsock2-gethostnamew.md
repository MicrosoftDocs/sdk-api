---
UID: NF:winsock2.GetHostNameW
title: GetHostNameW function (winsock2.h)
description: The GetHostNameW function retrieves the standard host name for the local computer as a Unicode string.
helpviewer_keywords: ["GetHostNameW","GetHostNameW function [Winsock]","winsock.gethostnamew","winsock2/GetHostNameW"]
old-location: winsock\gethostnamew.htm
tech.root: WinSock
ms.assetid: 787EB209-5944-4F0A-8550-FE1115C2298A
ms.date: 12/05/2018
ms.keywords: GetHostNameW, GetHostNameW function [Winsock], winsock.gethostnamew, winsock2/GetHostNameW
req.header: winsock2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - GetHostNameW
 - winsock2/GetHostNameW
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
 - GetHostNameW
---

# GetHostNameW function


## -description

The 
<b>GetHostNameW</b> function retrieves the standard host name for the local computer as a Unicode string.

## -parameters

### -param name [out]

A pointer to a buffer that receives the local host name as a <b>null</b>-terminated Unicode string.

### -param namelen [in]

The length, in wide characters, of the buffer pointed to by the <i>name</i> parameter.

## -returns

If no error occurs, 
<b>GetHostNameW</b> returns zero. Otherwise, it returns <b>SOCKET_ERROR</b> and a specific error code can be retrieved by calling 
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
</table>

## -remarks

The 
<b>GetHostNameW</b> function returns the name of the local host into the buffer specified by the <i>name</i> parameter in Unicode (UTF-16). The host name is returned as a <b>null</b>-terminated Unicode string. The form of the host name is dependent on the Windows Sockets provider—it can be a simple host name, or it can be a fully qualified domain name. However, it is guaranteed that the name returned will be successfully parsed by 
<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfow">GetAddrInfoW</a>.

With the growth of the Internet, there is a growing need to identify Internet host names for other languages not represented by the ASCII character set. Identifiers which facilitate this need and allow non-ASCII characters (Unicode) to be represented as special ASCII character strings (Punycode) are known as Internationalized Domain Names (IDNs). A  mechanism called
   Internationalizing Domain Names in Applications (IDNA) is used to handle
   IDNs in a standard fashion. The <b>GetHostNameW</b> function does not convert the local hostname between Punycode and Unicode. The <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfow">GetAddrInfoW</a> function provides support for Internationalized Domain Name (IDN) parsing and performs Punycode/IDN encoding and conversion.  

If the 
<b>GetHostNameW</b> function is used on a cluster resource on Windows Server 2012 and the _CLUSTER_NETWORK_NAME_ environment variable is defined, then the value in this environment variable overrides the actual hostname and is returned. On a cluster resource, the _CLUSTER_NETWORK_NAME_ environment variable contains the name of the cluster.

The 
<b>GetHostNameW</b> function queries namespace providers to determine the local host name using the SVCID_HOSTNAME GUID defined in the <i>Svgguid.h</i> header file. If no namespace provider responds, then the 
<b>GetHostNameW</b> function returns the NetBIOS name of the local computer in Unicode.

The maximum length, in wide characters, of the string returned in the buffer pointed to by the <i>name</i> parameter is dependent on the namespace provider, but this string must be 256 wide characters or less. So if a buffer of 256 wide characters is passed in the <i>name</i> parameter and the <i>namelen</i> parameter is set to 256, the buffer size will always be adequate.


<div class="alert"><b>Note</b>  If no local host name has been configured, 
<b>GetHostNameW</b> must succeed and return a token host name that 
<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfow">GetAddrInfoW</a> can resolve.</div>
<div> </div>


<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfow">GetAddrInfoW</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="/windows/desktop/api/winsock/nf-winsock-gethostname">gethostname</a>