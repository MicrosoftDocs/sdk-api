---
UID: NF:ws2tcpip.GetAddrInfoExA
title: GetAddrInfoExA function (ws2tcpip.h)
description: Provides protocol-independent name resolution with additional parameters to qualify which namespace providers should handle the request. (ANSI)
helpviewer_keywords: ["GetAddrInfoExA", "NS_ALL", "NS_BTH", "NS_DNS", "NS_EMAIL", "NS_NETBT", "NS_NLA", "NS_NTDS", "NS_PNRPCLOUD", "NS_PNRPNAME", "NS_WINS", "ws2tcpip/GetAddrInfoExA"]
old-location: winsock\getaddrinfoex.htm
tech.root: WinSock
ms.assetid: cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39
ms.date: 12/05/2018
ms.keywords: GetAddrInfoEx, GetAddrInfoEx function [Winsock], GetAddrInfoExA, GetAddrInfoExW, NS_ALL, NS_BTH, NS_DNS, NS_EMAIL, NS_NETBT, NS_NLA, NS_NTDS, NS_PNRPCLOUD, NS_PNRPNAME, NS_WINS, winsock.getaddrinfoex, ws2tcpip/GetAddrInfoEx, ws2tcpip/GetAddrInfoExA, ws2tcpip/GetAddrInfoExW
req.header: ws2tcpip.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetAddrInfoExW (Unicode) and GetAddrInfoExA (ANSI)
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
 - GetAddrInfoExA
 - ws2tcpip/GetAddrInfoExA
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
 - GetAddrInfoEx
 - GetAddrInfoExA
 - GetAddrInfoExW
---

# GetAddrInfoExA function


## -description

The 
<b>GetAddrInfoEx</b> function provides protocol-independent name resolution with additional parameters to qualify which namespace providers should handle the request.

## -parameters

### -param pName [in, optional]

A pointer to a <b>NULL</b>-terminated string containing a host (node) name or a numeric host address string. For the Internet protocol, the numeric host address string is a dotted-decimal IPv4 address or an IPv6 hex address.

### -param pServiceName [in, optional]

A pointer to an optional <b>NULL</b>-terminated string that contains either a service name or port number represented as a string.

A service name is a string alias for a port number. For example, “http” is an alias for port 80 defined by the Internet Engineering Task Force (IETF) as the default port used by web servers for the HTTP protocol. Possible values for the <i>pServiceName</i> parameter when a port number is not specified are listed in the following file: 

<code>%WINDIR%\system32\drivers\etc\services</code>

### -param dwNameSpace [in]

An optional namespace identifier that determines which namespace providers are queried.  Passing a specific namespace identifier will result in only namespace providers that support the specified namespace being queried. Specifying <b>NS_ALL</b> will result in all installed and active namespace providers being queried. 


Options for the <i>dwNameSpace</i> parameter are listed in the <i>Winsock2.h</i> include file. Several namespace providers are added on Windows Vista and later. Other namespace providers can be installed, so the following possible values  are only those commonly available. Many other values are possible.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NS_ALL"></a><a id="ns_all"></a><dl>
<dt><b>NS_ALL</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
All installed and active namespaces.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_DNS"></a><a id="ns_dns"></a><dl>
<dt><b>NS_DNS</b></dt>
<dt>12</dt>
</dl>
</td>
<td width="60%">
The domain name system (DNS) namespace.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_NETBT"></a><a id="ns_netbt"></a><dl>
<dt><b>NS_NETBT</b></dt>
<dt>13</dt>
</dl>
</td>
<td width="60%">
The NetBIOS over TCP/IP (NETBT) namespace.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_WINS"></a><a id="ns_wins"></a><dl>
<dt><b>NS_WINS</b></dt>
<dt>14</dt>
</dl>
</td>
<td width="60%">
The Windows Internet Naming Service (NS_WINS) namespace.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_NLA"></a><a id="ns_nla"></a><dl>
<dt><b>NS_NLA</b></dt>
<dt>15</dt>
</dl>
</td>
<td width="60%">
The network location awareness (NLA) namespace. 

This namespace identifier is supported on Windows XP and later.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_BTH"></a><a id="ns_bth"></a><dl>
<dt><b>NS_BTH</b></dt>
<dt>16</dt>
</dl>
</td>
<td width="60%">
The Bluetooth namespace. 

This namespace identifier is supported on Windows Vista and later.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_NTDS"></a><a id="ns_ntds"></a><dl>
<dt><b>NS_NTDS</b></dt>
<dt>32</dt>
</dl>
</td>
<td width="60%">
The Windows NT Directory Services (NS_NTDS) namespace. 

</td>
</tr>
<tr>
<td width="40%"><a id="NS_EMAIL"></a><a id="ns_email"></a><dl>
<dt><b>NS_EMAIL</b></dt>
<dt>37</dt>
</dl>
</td>
<td width="60%">
The email namespace. 

This namespace identifier is supported on Windows Vista and later.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_PNRPNAME"></a><a id="ns_pnrpname"></a><dl>
<dt><b>NS_PNRPNAME</b></dt>
<dt>38</dt>
</dl>
</td>
<td width="60%">
The peer-to-peer namespace for a specific peer name. 

This namespace identifier is supported on Windows Vista and later.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_PNRPCLOUD"></a><a id="ns_pnrpcloud"></a><dl>
<dt><b>NS_PNRPCLOUD</b></dt>
<dt>39</dt>
</dl>
</td>
<td width="60%">
The peer-to-peer namespace for a collection of peer names. 

This namespace identifier is supported on Windows Vista and later.

</td>
</tr>
</table>

### -param lpNspId [in, optional]

A pointer to an optional GUID of a specific namespace provider to query in the case where  multiple namespace providers are registered under a single namespace such as <b>NS_DNS</b>. Passing the GUID for specific namespace provider will result in only the specified namespace provider being queried. The <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersa">WSAEnumNameSpaceProviders</a> function can be called to retrieve the GUID for a namespace provider.

### -param hints [in, optional]

A pointer to an 
<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoexw">addrinfoex</a> structure that provides hints about the type of socket the caller supports. 

The <b>ai_addrlen</b>, <b>ai_canonname</b>, <b>ai_addr</b>, and <b>ai_next</b> members of the <a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoexw">addrinfoex</a> structure pointed to by the <i>pHints</i> parameter must be zero or <b>NULL</b>. Otherwise the <b>GetAddrInfoEx</b> function will fail with <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANO_RECOVERY</a>.

See the Remarks for more details.

### -param ppResult [out]

A pointer to a linked list of one or more 
<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoexw">addrinfoex</a> structures that contains response information about the host.

### -param timeout [in, optional]

An optional parameter indicating the time, in milliseconds, to wait for a response from the namespace provider before aborting the call. 

This parameter is only supported when the <b>UNICODE</b> or <b>_UNICODE</b> macro has been defined in the sources before calling the <b>GetAddrInfoEx</b> function. Otherwise, this parameter is currently reserved and must be set to <b>NULL</b> since a <i>timeout</i> option is not supported.

### -param lpOverlapped [in, optional]

An optional pointer to an overlapped structure used for asynchronous operation. 

This parameter is only supported when the <b>UNICODE</b> or <b>_UNICODE</b> macro has been defined in the sources before calling the <b>GetAddrInfoEx</b> function.

On Windows 8 and Windows Server 2012, if no <i>lpCompletionRoutine</i> parameter is specified, the <b>hEvent</b> member of the <b>OVERLAPPED</b> structure must be set to a manual-reset event to be called upon completion of an asynchronous call. If a completion routine has been specified, the <b>hEvent</b> member must be NULL. When the event specified by <b>hEvent</b> has been set, the result of the operation can be retrieved by calling <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexoverlappedresult">GetAddrInfoExOverlappedResult</a> function.

On Windows 8 and Windows Server 2012 whenever the <b>UNICODE</b> or <b>_UNICODE</b> macro is not defined,  this parameter is currently reserved and must be set to <b>NULL</b>. 

On Windows 7 and Windows Server 2008 R2 or earlier, this parameter is currently reserved and must be set to <b>NULL</b> since asynchronous operations are not supported.

### -param lpCompletionRoutine [in, optional]

An optional pointer to a function to be invoked upon successful completion for asynchronous operations. 

This parameter is only supported when the <b>UNICODE</b> or <b>_UNICODE</b> macro has been defined in the sources before calling the <b>GetAddrInfoEx</b> function.

If this parameter is specified, it must be a pointer to a function with the following signature:


```cpp
typedef   
void   
(CALLBACK * LPLOOKUPSERVICE_COMPLETION_ROUTINE)(   
    __in      DWORD    dwError,   
    __in      DWORD    dwBytes,   
    __in      LPWSAOVERLAPPED lpOverlapped   
    );   

```


When the asynchronous operation has completed, the completion routine will be invoked with <i>lpOverlapped</i> parameter set to the value of <i>lpOverlapped</i> parameter passed to <b>GetAddrInfoEx</b>. The <b>Pointer</b> member of the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure will be set to the value of the <i>ppResult</i> parameter of the original call. If the <b>Pointer</b> member points to a non-NULL pointer to the <a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoexw">addrinfoex</a> structure, it is the caller’s responsibility to call <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-freeaddrinfoex">FreeAddrInfoEx</a> to free the <b>addrinfoex</b>  structure. The <i>dwError</i> parameter passed to the completion routine will be set to a Winsock error code. The <i>dwBytes</i> parameter is reserved for future use and must be ignored.

On Windows 8 and Windows Server 2012 whenever the <b>UNICODE</b> or <b>_UNICODE</b> macro is not defined,  this parameter is currently reserved and must be set to <b>NULL</b>. 

On Windows 7 and Windows Server 2008 R2 or earlier, this parameter is currently reserved and must be set to <b>NULL</b> since asynchronous operations are not supported.

### -param lpNameHandle [out, optional]

An optional pointer used only for asynchronous operations.  

This parameter is only supported when the <b>UNICODE</b> or <b>_UNICODE</b> macro has been defined in the sources before calling the <b>GetAddrInfoEx</b> function.

On Windows 8 and Windows Server 2012, if the <b>GetAddrInfoEx</b> function will complete asynchronously, the pointer returned in this field may be used with the <b>GetAddrInfoExCancel</b> function. The handle returned is valid when <b>GetAddrInfoEx</b> returns until the completion routine is called, the event is triggered, or <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexcancel">GetAddrInfoExCancel</a> function is called with this handle.

On Windows 8 and Windows Server 2012 whenever the <b>UNICODE</b> or <b>_UNICODE</b> macro is not defined,  this parameter is currently reserved and must be set to <b>NULL</b>. 

On Windows 7 and Windows Server 2008 R2 or earlier, this parameter is currently reserved and must be set to <b>NULL</b> since asynchronous operations are not supported.

## -returns

On success,  <b>GetAddrInfoEx</b> returns <b>NO_ERROR</b> (0). Failure returns a nonzero Windows Sockets error code, as found in the 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">Windows Sockets Error Codes</a>.

Most nonzero error codes returned by the 
<b>GetAddrInfoEx</b> function map to the set of errors outlined by Internet Engineering Task Force (IETF) recommendations. The following table shows these error codes and their WSA equivalents. It is recommended that the WSA error codes be used, as they offer familiar and comprehensive error information for Winsock programmers.

<table>
<tr>
<th>Error value</th>
<th>WSA equivalent</th>
<th>Description</th>
</tr>
<tr>
<td>EAI_AGAIN</td>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSATRY_AGAIN</a></td>
<td>A temporary failure in name resolution occurred.</td>
</tr>
<tr>
<td>EAI_BADFLAGS</td>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></td>
<td>An invalid parameter was provided. This error is returned if any of the reserved parameters are not <b>NULL</b>. This error is also returned if an invalid value was provided for the <b>ai_flags</b> member of the <i>pHints</i> parameter.</td>
</tr>
<tr>
<td>EAI_FAIL</td>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANO_RECOVERY</a></td>
<td>A nonrecoverable failure in name resolution occurred.</td>
</tr>
<tr>
<td>EAI_FAMILY</td>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEAFNOSUPPORT</a></td>
<td>The <b>ai_family</b> member  of the <i>pHints</i> parameter is not supported.</td>
</tr>
<tr>
<td>EAI_MEMORY</td>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_NOT_ENOUGH_MEMORY</a></td>
<td>A memory allocation failure occurred.</td>
</tr>
<tr>
<td>EAI_NONAME</td>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAHOST_NOT_FOUND</a></td>
<td>The name does not resolve for the supplied parameters or the <i>pName</i> and <i>pServiceName</i> parameters were not provided.</td>
</tr>
<tr>
<td>EAI_SERVICE</td>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSATYPE_NOT_FOUND</a></td>
<td>The <i>pServiceName</i> parameter is not supported for the specified <b>ai_socktype</b> member of the <i>pHints</i> parameter.</td>
</tr>
<tr>
<td>EAI_SOCKTYPE</td>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAESOCKTNOSUPPORT</a></td>
<td>The <b>ai_socktype</b> member of the <i>pHints</i> parameter is not supported.</td>
</tr>
</table>
 

Use the 
<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-gai_strerrora">gai_strerror</a> function to print error messages based on the EAI codes returned by the 
<b>GetAddrInfoEx</b> function. The 
<b>gai_strerror</b> function is provided for compliance with IETF recommendations, but it is not thread safe. Therefore, use of traditional Windows Sockets functions such as 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a> is recommended.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEAFNOSUPPORT</a></b></dt>
</dl>
</td>
<td width="60%">
An address incompatible with the requested protocol was used. This error is returned if the <b>ai_family</b> member of the 
			<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoexw">addrinfoex</a> structure pointed to by the <i>pHints</i> parameter is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
An invalid argument was supplied.  This error is returned if an invalid value was provided for the <b>ai_flags</b> member of the 
			<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoexw">addrinfoex</a> structure pointed to by the <i>pHints</i> parameter.  This error is also returned when the <i>dwNameSpace</i> parameter is NS_PNRPNAME or NS_PNRPCLOUD and the peer-to-peer name service is not operating.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAESOCKTNOSUPPORT</a></b></dt>
</dl>
</td>
<td width="60%">
The support for the specified socket type does not exist in this address family. This error is returned if the <b>ai_socktype</b> member of the 
			<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoexw">addrinfoex</a> structure pointed to by the <i>pHints</i> parameter is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAHOST_NOT_FOUND</a></b></dt>
</dl>
</td>
<td width="60%">
No such host is known. This error is returned if the name does not resolve for the supplied parameters or the <i>pName</i> and <i>pServiceName</i> parameters were not provided.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANO_DATA</a></b></dt>
</dl>
</td>
<td width="60%">
The requested name is valid, but no data of the requested type was found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANO_RECOVERY</a></b></dt>
</dl>
</td>
<td width="60%">
A nonrecoverable error occurred during a database lookup. This error is returned if nonrecoverable error in name resolution occurred.

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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSASERVICE_NOT_FOUND</a></b></dt>
</dl>
</td>
<td width="60%">
No such service is known. The service cannot be found in the specified name space. This error is returned if the <i>pName</i> or <i>pServiceName</i> parameter is not found for the namespace specified in the <i>dwNameSpace</i> parameter or the namespace specified in the <i>dwNameSpace</i> parameter is not installed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSATRY_AGAIN</a></b></dt>
</dl>
</td>
<td width="60%">
This is usually a temporary error during hostname resolution and means that the local server did not receive a response from an authoritative server. This error is returned when a temporary failure in name resolution occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSATYPE_NOT_FOUND</a></b></dt>
</dl>
</td>
<td width="60%">
The specified class was not found. The <i>pServiceName</i> parameter is not supported for the specified <b>ai_socktype</b> member of the 
			<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoexw">addrinfoex</a> structure pointed to by the <i>pHints</i> parameter.

</td>
</tr>
</table>

## -remarks

The <b>GetAddrInfoEx</b>  function provides protocol-independent translation from host name to address and from service name to port number. The <b>GetAddrInfoEx</b>  function is an enhanced version of the <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo">getaddrinfo</a> and <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfow">GetAddrInfoW</a> functions. The <b>GetAddrInfoEx</b>  function allows specifying the namespace provider to resolve the query. 

The <b>GetAddrInfoEx</b>  function aggregates and returns results from multiple namespace providers, unless a specific namespace provider is specified. For use with the IPv6 and IPv4 protocol, name resolution can be by the Domain Name System (DNS), a local <i>hosts</i> file, an email provider (the <b>NS_EMAIL</b> namespace), or by other naming mechanisms.

When UNICODE or _UNICODE is defined, <b>GetAddrInfoEx</b> is defined to <b>GetAddrInfoExW</b>, the Unicode version of this function. The string parameters are defined to the <b>PWSTR</b> data type and the <b>ADDRINFOEXW</b> structure is used. On Windows 8 and Windows Server 2012, the <i>timeout</i>, <i>lpOverlapped</i>, <i>lpCompletionRoutine</i>, and <i>lpNameHandle</i> parameters may be used to call the <b>GetAddrInfoEx</b> function so that it can complete asynchronously. 

When UNICODE or _UNICODE is not defined, <b>GetAddrInfoEx</b> is defined to <b>GetAddrInfoExA</b>, the ANSI version of this function. The string parameters are of the <b>PCSTR</b> data type and the <b>ADDRINFOEXA</b> structure is used. The <i>timeout</i>, <i>lpOverlapped</i>, <i>lpCompletionRoutine</i>, and <i>lpNameHandle</i> parameters must be set to <b>NULL</b>.

One or both of the <i>pName</i> or <i>pServiceName</i> parameters must point to a <b>NULL</b>-terminated string. Generally both are provided.

Upon success, a linked list of 
<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoexw">addrinfoex</a> structures is returned in the <i>ppResult</i> parameter. The list can be processed by following the pointer provided in the <b>ai_next</b> member of each returned 
<b>addrinfoex</b> structure until a <b>NULL</b> pointer is encountered. In each returned 
<b>addrinfoex</b> structure, the <b>ai_family</b>, <b>ai_socktype</b>, and <b>ai_protocol</b> members correspond to respective arguments in a 
<a href="/windows/desktop/api/winsock2/nf-winsock2-socket">socket</a> or <a href="/windows/desktop/api/winsock2/nf-winsock2-wsasocketa">WSASocket</a> function call. Also, the <b>ai_addr</b> member in each returned 
<b>addrinfoex</b> structure points to a filled-in socket address structure, the length of which is specified in its <b>ai_addrlen</b> member.

If the <i>pName</i> parameter points to a computer name, all permanent addresses for the computer that can be used as a source address are returned. On Windows Vista and later, these addresses would include all unicast IP addresses returned by the  <a href="/windows/desktop/api/netioapi/nf-netioapi-getunicastipaddresstable">GetUnicastIpAddressTable</a> or <a href="/windows/desktop/api/netioapi/nf-netioapi-getunicastipaddressentry">GetUnicastIpAddressEntry</a> functions in which the <b>SkipAsSource</b> member is set to false in the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> structure. 

If the <i>pName</i> parameter points to a string equal to "localhost", all loopback addresses on the local computer are returned. 

If the <i>pName</i> parameter contains an empty string, all registered addresses on the local computer are returned. 

On Windows Server 2003 and later if the <i>pName</i> parameter points to a string equal to "..localmachine", all registered addresses on the local computer are returned. 

If the <i>pName</i> parameter refers to a cluster virtual server name, only virtual server addresses are returned. On Windows Vista and later, these addresses would include all unicast IP addresses returned by the  <a href="/windows/desktop/api/netioapi/nf-netioapi-getunicastipaddresstable">GetUnicastIpAddressTable</a> or <a href="/windows/desktop/api/netioapi/nf-netioapi-getunicastipaddressentry">GetUnicastIpAddressEntry</a> functions in which the <b>SkipAsSource</b> member is set to true in the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> structure. See <a href="/previous-versions/windows/desktop/mscs/windows-clustering">Windows Clustering</a> for more information about clustering.

Windows 7 with Service Pack 1 (SP1) and Windows Server 2008 R2 with Service Pack 1 (SP1) add support to Netsh.exe for setting the SkipAsSource attribute on an IP address. This also changes the behavior such that if the <b>SkipAsSource</b> member in the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> structure is set to false, the IP address will be registered in DNS. If the <b>SkipAsSource</b> member is set to true, the IP address is not registered in DNS.  

A hotfix is available for Windows 7 and Windows Server 2008 R2 that adds support to Netsh.exe for setting the SkipAsSource attribute on an IP address.  This hotfix also changes behavior such that if the <b>SkipAsSource</b> member in the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> structure is set to false, the IP address will be registered in DNS. If the <b>SkipAsSource</b> member is set to true, the IP address is not registered in DNS.  For more information, see <a href="https://support.microsoft.com/kb/2386184">Knowledge Base (KB) 2386184</a>.   

A similar hotfix is also available for Windows Vista with Service Pack 2 (SP2) and Windows Server 2008 with Service Pack 2 (SP2) that adds support to Netsh.exe for setting the SkipAsSource attribute on an IP address. This hotfix also changes behavior such that if the <b>SkipAsSource</b> member in the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> structure is set to false, the IP address will be registered in DNS. If the <b>SkipAsSource</b> member is set to true, the IP address is not registered in DNS. 

Callers of the 
<b>GetAddrInfoEx</b> function can provide hints about the type of socket supported through an 
<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoexw">addrinfoex</a> structure pointed to by the <i>pHints</i> parameter. When the <i>pHints</i> parameter is used, the following rules apply to its associated 
<b>addrinfoex</b> structure:

<ul>
<li>A value of <b>AF_UNSPEC</b> for <b>ai_family</b> indicates the caller will accept only the <b>AF_INET</b> and <b>AF_INET6</b> address families. Note that <b>AF_UNSPEC</b> and <b>PF_UNSPEC</b> are the same.</li>
<li>A value of zero for <b>ai_socktype</b> indicates the caller will accept any socket type. </li>
<li>A value of zero for <b>ai_protocol</b> indicates the caller will accept any protocol.</li>
<li>The <b>ai_addrlen</b> member must be set to zero.</li>
<li>The <b>ai_canonname</b> member must be set to <b>NULL</b>.</li>
<li>The <b>ai_addr</b> member must be set to <b>NULL</b>.</li>
<li>The <b>ai_next</b> member must be set to <b>NULL</b>.</li>
</ul>


Other values in the 
<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoexw">addrinfoex</a> structure provided in the <i>pHints</i> parameter indicate specific requirements. For example, if the caller handles only IPv4 and does not handle IPv6, the <b>ai_family</b> member should be set to <b>AF_INET</b>. For another example, if the caller handles only TCP and does not handle UDP, the <b>ai_socktype</b> member should be set to <b>SOCK_STREAM</b>. 

If the <i>pHints</i> parameter is a <b>NULL</b> pointer, the 
<b>GetAddrInfoEx</b> function treats it as if the 
<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoexw">addrinfoex</a> structure in <i>pHints</i> were initialized with its <b>ai_family</b> member set to <b>AF_UNSPEC</b> and all other members set to <b>NULL</b> or zero.

When <b>GetAddrInfoEx</b> is called from a service, if the operation is the result of a user process calling the service, the service should impersonate the user.  This is to allow security to be properly enforced.


The 
<b>GetAddrInfoEx</b> function can be used to convert a text string representation of an IP address to an <a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoexw">addrinfoex</a> structure that contains a   <a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure for the IP address and other information. To be used in this way, the string pointed to by the <i>pName</i> parameter must contain a text representation of an IP address and the <b>addrinfoex</b> structure pointed to by the <i>pHints</i> parameter must have the AI_NUMERICHOST flag set in the <b>ai_flags</b> member. The string pointed to by the <i>pName</i> parameter may contain a text representation of either an IPv4 or an IPv6 address. The text IP address is converted to an <b>addrinfoex</b> structure pointed to by the <i>ppResult</i> parameter. The returned <b>addrinfoex</b> structure contains a <b>sockaddr</b> structure for the IP address along with additional information about the IP address. 

Multiple namespace providers may be installed on a local computer for the same namespace. For example, the base Windows TCP/IP networking software registers for the NS_DNS namespace. The Microsoft Forefront Threat Management Gateway (TMG) and the older Microsoft Internet Security and Acceleration (ISA) Server include Firewall Client software that also registers for the NS_DNS namespace. When the <i>dwNameSpace</i> parameter is set to a value (NS_DNS, for example) and the <i>lpNspId</i> parameter is <b>NULL</b>, the results returned by the <b>GetAddrInfoEx</b> function are the merged results from all namespace providers that register for the specified namespace with duplicate results eliminated. The <i>lpNspId</i> parameter should be set to the GUID of the specific namespace provider if only a single namespace provider is to be queried. 

If the <i>pNameSpace</i> parameter is set to NS_ALL, then the results from querying all namespace providers is merged and returned. In this case, duplicate responses may be returned in the results pointed to by the <i>ppResult</i> parameter if multiple namespace providers return the same information.

On Windows 8 and Windows Server 2012, if the <b>GetAddrInfoEx</b> function will complete asynchronously, the pointer returned in the <i>lpNameHandle</i> parameter may be used with the <b>GetAddrInfoExCancel</b> function. The handle returned is valid when <b>GetAddrInfoEx</b> returns until the completion routine is called, the event is triggered, or <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexcancel">GetAddrInfoExCancel</a> function is called with this handle.

<h3><a id="Freeing_Address_Information_from_Dynamic_Allocation"></a><a id="freeing_address_information_from_dynamic_allocation"></a><a id="FREEING_ADDRESS_INFORMATION_FROM_DYNAMIC_ALLOCATION"></a>Freeing Address Information from Dynamic Allocation</h3>
All information returned by the 
<b>GetAddrInfoEx</b> function pointed to by the <i>ppResult</i> parameter is dynamically allocated, including all 
<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoexw">addrinfoex</a> structures, socket address structures, and canonical host name strings pointed to by 
<b>addrinfoex</b> structures. Memory allocated by a successful call to this function must be released with a subsequent call to <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-freeaddrinfoex">FreeAddrInfoEx</a>.

<h3><a id="Example_Code"></a><a id="example_code"></a><a id="EXAMPLE_CODE"></a>Example Code</h3>
The following example demonstrates the use of the <b>GetAddrInfoEx</b> function.


```cpp
#ifndef UNICODE
#define UNICODE
#endif

#include <winsock2.h>
#include <ws2tcpip.h>
#include <objbase.h>
#include <stdio.h>

// Need to link with Ws2_32.lib
#pragma comment(lib, "ws2_32.lib")

// Need to link with Ole32.lib to print GUID
#pragma comment(lib, "ole32.lib")

int __cdecl wmain(int argc, wchar_t ** argv)
{

    //-----------------------------------------
    // Declare and initialize variables
    WSADATA wsaData;
    int iResult;

    DWORD dwRetval;

    int i = 1;

    DWORD dwNamespace = NS_ALL;
    LPGUID lpNspid = NULL;

    ADDRINFOEX *result = NULL;
    ADDRINFOEX *ptr = NULL;
    ADDRINFOEX hints;

    // LPSOCKADDR sockaddr_ip;
    struct sockaddr_in *sockaddr_ipv4;
    struct sockaddr_in6 *sockaddr_ipv6;

    // DWORD ipbufferlength = 46;
    wchar_t ipstringbuffer[46];

    // variables needed to print namespace provider GUID
    int iRet = 0;
    WCHAR GuidString[40] = { 0 };

    // Validate the parameters
    if (argc != 4) {
        wprintf(L"usage: %ws <hostname> <servicename> <namespace>\n", argv[0]);
        wprintf(L"getaddrinfoex provides protocol-independent translation\n");
        wprintf(L"   from a host name to an IP address\n");
        wprintf(L"%ws example usage\n", argv[0]);
        wprintf(L"   %ws www.contoso.com 0 12\n", argv[0]);
        wprintf(L"   looks up the www.contoso.com in the NS_DNS namespace\n",
                argv[0]);
        return 1;
    }
    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed: %d\n", iResult);
        return 1;
    }
    //--------------------------------
    // Setup the hints address info structure
    // which is passed to the getaddrinfo() function
    ZeroMemory(&hints, sizeof (hints));
    hints.ai_family = AF_UNSPEC;
    hints.ai_socktype = SOCK_STREAM;
    hints.ai_protocol = IPPROTO_TCP;

    dwNamespace = (DWORD) _wtoi(argv[3]);

    wprintf(L"Calling GetAddrInfoEx with following parameters:\n");
    wprintf(L"\tName = %ws\n", argv[1]);
    wprintf(L"\tServiceName (or port) = %ws\n", argv[2]);
    wprintf(L"\tNamespace = %s (", argv[3]);
    switch (dwNamespace) {
    case NS_ALL:
        wprintf(L"(NS_ALL)\n");
        break;
    case NS_DNS:
        wprintf(L"(NS_DNS)\n");
        break;
    case NS_NETBT:
        wprintf(L"NS_NETBT");
        break;
    case NS_WINS:
        wprintf(L"NS_WINS");
        break;
    case NS_NLA:
        wprintf(L"NS_NLA");
        break;
    case NS_BTH:
        wprintf(L"NS_BTH");
        break;
    case NS_NTDS:
        wprintf(L"NS_NTDS");
        break;
    case NS_EMAIL:
        wprintf(L"NS_EMAIL");
        break;
    case NS_PNRPNAME:
        wprintf(L"NS_PNRPNAME");
        break;
    case NS_PNRPCLOUD:
        wprintf(L"NS_PNRPCLOUD");
        break;
    default:
        wprintf(L"Other");
        break;
    }
    wprintf(L")\n\n");

//--------------------------------
// Call getaddrinfoex(). If the call succeeds,
// the result variable will hold a linked list
// of addrinfo structures containing response
// information
    dwRetval =
        GetAddrInfoEx(argv[1], argv[2], dwNamespace, lpNspid, &hints, &result,
                      NULL, NULL, NULL, NULL);
    if (dwRetval != 0) {
        wprintf(L"GetAddrInfoEx failed with error: %d\n", dwRetval);
        WSACleanup();
        return 1;
    }

    wprintf(L"GetAddrInfoEx returned success\n");

    // Retrieve each address and print out the hex bytes
    for (ptr = result; ptr != NULL; ptr = ptr->ai_next) {

        wprintf(L"GetAddrInfoEx response %d\n", i++);
        wprintf(L"\tFlags: 0x%x\n", ptr->ai_flags);
        wprintf(L"\tFamily: ");
        switch (ptr->ai_family) {
        case AF_UNSPEC:
            wprintf(L"Unspecified\n");
            break;
        case AF_INET:
            wprintf(L"AF_INET (IPv4)\n");
            // the InetNtop function is available on Windows Vista and later
            sockaddr_ipv4 = (struct sockaddr_in *) ptr->ai_addr;
            wprintf(L"\tIPv4 address %ws\n",
                    InetNtop(AF_INET, &sockaddr_ipv4->sin_addr, ipstringbuffer,
                             46));

            // We could also use the WSAAddressToString function
            // sockaddr_ip = (LPSOCKADDR) ptr->ai_addr;
            // The buffer length is changed by each call to WSAAddresstoString
            // So we need to set it for each iteration through the loop for safety
            // ipbufferlength = 46;
            // iRetval = WSAAddressToString(sockaddr_ip, (DWORD) ptr->ai_addrlen, NULL, 
            //    ipstringbuffer, &ipbufferlength );
            // if (iRetval)
            //    wprintf(L"WSAAddressToString failed with %u\n", WSAGetLastError() );
            // else    
            //    wprintf(L"\tIPv4 address %ws\n", ipstringbuffer);
            break;
        case AF_INET6:
            wprintf(L"AF_INET6 (IPv6)\n");
            // the InetNtop function is available on Windows Vista and later
            sockaddr_ipv6 = (struct sockaddr_in6 *) ptr->ai_addr;
            wprintf(L"\tIPv6 address %ws\n",
                    InetNtop(AF_INET6, &sockaddr_ipv6->sin6_addr,
                             ipstringbuffer, 46));

            // We could also use WSAAddressToString which also returns the scope ID
            // sockaddr_ip = (LPSOCKADDR) ptr->ai_addr;
            // The buffer length is changed by each call to WSAAddresstoString
            // So we need to set it for each iteration through the loop for safety
            // ipbufferlength = 46;
            //iRetval = WSAAddressToString(sockaddr_ip, (DWORD) ptr->ai_addrlen, NULL, 
            //    ipstringbuffer, &ipbufferlength );
            //if (iRetval)
            //    wprintf(L"WSAAddressToString failed with %u\n", WSAGetLastError() );
            //else    
            //    wprintf(L"\tIPv6 address %ws\n", ipstringbuffer);
            break;
        default:
            wprintf(L"Other %ld\n", ptr->ai_family);
            break;
        }
        wprintf(L"\tSocket type: ");
        switch (ptr->ai_socktype) {
        case 0:
            wprintf(L"Unspecified\n");
            break;
        case SOCK_STREAM:
            wprintf(L"SOCK_STREAM (stream)\n");
            break;
        case SOCK_DGRAM:
            wprintf(L"SOCK_DGRAM (datagram) \n");
            break;
        case SOCK_RAW:
            wprintf(L"SOCK_RAW (raw) \n");
            break;
        case SOCK_RDM:
            wprintf(L"SOCK_RDM (reliable message datagram)\n");
            break;
        case SOCK_SEQPACKET:
            wprintf(L"SOCK_SEQPACKET (pseudo-stream packet)\n");
            break;
        default:
            wprintf(L"Other %ld\n", ptr->ai_socktype);
            break;
        }
        wprintf(L"\tProtocol: ");
        switch (ptr->ai_protocol) {
        case 0:
            wprintf(L"Unspecified\n");
            break;
        case IPPROTO_TCP:
            wprintf(L"IPPROTO_TCP (TCP)\n");
            break;
        case IPPROTO_UDP:
            wprintf(L"IPPROTO_UDP (UDP) \n");
            break;
        default:
            wprintf(L"Other %ld\n", ptr->ai_protocol);
            break;
        }
        wprintf(L"\tLength of this sockaddr: %d\n", ptr->ai_addrlen);
        wprintf(L"\tCanonical name: %s\n", ptr->ai_canonname);

        if (ptr->ai_blob == NULL)
            wprintf(L"\tBlob: (null)\n");
        else    
            wprintf(L"\tLength of the blob: %u\n",
                    (DWORD) ptr->ai_bloblen);

        if (ptr->ai_provider == NULL)
            wprintf(L"\tNamespace provider GUID: (null)\n");
        else {
            iRet =
                StringFromGUID2(*(ptr->ai_provider), (LPOLESTR) & GuidString,
                                39);
            // For c rather than C++ source code, the above line needs to be
            // iRet = StringFromGUID2(&ptr.ai_provider, (LPOLESTR) &GuidString, 39); 
            if (iRet == 0)
                wprintf(L"StringFromGUID2 failed\n");
            else {
                wprintf(L"\tNamespace provider: %ws\n", GuidString);
            }
        }
    }

    FreeAddrInfoEx(result);
    WSACleanup();

    return 0;
}


```


The following example demonstrates how to use the <b>GetAddrInfoEx</b> function asynchronous to
resolve a name to an IP address..


```cpp
//
//    This sample demonstrates how to use asynchronous GetAddrInfoEx to
//    resolve a name to an IP address.
//
//    ResolveName <QueryName>
//

#ifndef UNICODE
#define UNICODE
#endif

#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>
#include <stdlib.h>

// Need to link with Ws2_32.lib
#pragma comment(lib, "ws2_32.lib")

#define MAX_ADDRESS_STRING_LENGTH   64

//
//  Asynchronous query context structure.
//

typedef struct _QueryContext
{
    OVERLAPPED      QueryOverlapped;
    PADDRINFOEX     QueryResults;
    HANDLE          CompleteEvent;
}QUERY_CONTEXT, *PQUERY_CONTEXT;

VOID
WINAPI
QueryCompleteCallback(
    _In_ DWORD Error,
    _In_ DWORD Bytes,
    _In_ LPOVERLAPPED Overlapped
    );

int
__cdecl
wmain(
    _In_ int Argc, PWCHAR Argv[]
    )
{
    INT                 Error = ERROR_SUCCESS;
    WSADATA             wsaData;
    BOOL                IsWSAStartupCalled = FALSE;
    ADDRINFOEX          Hints;
    QUERY_CONTEXT       QueryContext;
    HANDLE              CancelHandle = NULL;
    DWORD               QueryTimeout = 5 * 1000; // 5 seconds

    ZeroMemory(&QueryContext, sizeof(QueryContext));

    //
    //  Validate the parameters
    //

    if (Argc != 2)
    {
        wprintf(L"Usage: ResolveName <QueryName>\n");
        goto exit;
    }

    //
    //  All Winsock functions require WSAStartup() to be called first
    //

    Error = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (Error != 0)
    {
        wprintf(L"WSAStartup failed with %d\n", Error);
        goto exit;
    }

    IsWSAStartupCalled = TRUE;

    ZeroMemory(&Hints, sizeof(Hints));
    Hints.ai_family = AF_UNSPEC;

    //
    //  Note that this is a simple sample that waits/cancels a single
    //  asynchronous query. The reader may extend this to support
    //  multiple asynchronous queries.
    //

    QueryContext.CompleteEvent = CreateEvent(NULL, TRUE, FALSE, NULL);

    if (QueryContext.CompleteEvent == NULL)
    {
        Error = GetLastError();
        wprintf(L"Failed to create completion event: Error %d\n",  Error);
        goto exit;
    }

    //
    //  Initiate asynchronous GetAddrInfoExW.
    //
    //  Note GetAddrInfoEx can also be invoked asynchronously using an event
    //  in the overlapped object (Just set hEvent in the Overlapped object
    //  and set NULL as completion callback.)
    //
    //  This sample uses the completion callback method.
    //

    Error = GetAddrInfoExW(Argv[1],
                           NULL,
                           NS_DNS,
                           NULL,
                           &Hints,
                           &QueryContext.QueryResults,
                           NULL,
                           &QueryContext.QueryOverlapped,
                           QueryCompleteCallback,
                           &CancelHandle);

    //
    //  If GetAddrInfoExW() returns  WSA_IO_PENDING, GetAddrInfoExW will invoke
    //  the completion routine. If GetAddrInfoExW returned anything else we must
    //  invoke the completion directly.
    //

    if (Error != WSA_IO_PENDING)
    {
        QueryCompleteCallback(Error, 0, &QueryContext.QueryOverlapped);
        goto exit;
    }

    //
    //  Wait for query completion for 5 seconds and cancel the query if it has
    //  not yet completed.
    //

    if (WaitForSingleObject(QueryContext.CompleteEvent,
                            QueryTimeout)  == WAIT_TIMEOUT )
    {

        //
        //  Cancel the query: Note that the GetAddrInfoExCancelcancel call does
        //  not block, so we must wait for the completion routine to be invoked.
        //  If we fail to wait, WSACleanup() could be called while an
        //  asynchronous query is still in progress, possibly causing a crash.
        //

        wprintf(L"The query took longer than %d seconds to complete; "
                L"cancelling the query...\n", QueryTimeout/1000);

        GetAddrInfoExCancel(&CancelHandle);

        WaitForSingleObject(QueryContext.CompleteEvent,
                            INFINITE);
    }

exit:

    if (IsWSAStartupCalled)
    {
        WSACleanup();
    }

    if (QueryContext.CompleteEvent)
    {
        CloseHandle(QueryContext.CompleteEvent);
    }

    return Error;
}

//
// Callback function called by Winsock as part of asynchronous query complete
//

VOID
WINAPI
QueryCompleteCallback(
    _In_ DWORD Error,
    _In_ DWORD Bytes,
    _In_ LPOVERLAPPED Overlapped
    )
{
    PQUERY_CONTEXT  QueryContext = NULL;
    PADDRINFOEX     QueryResults = NULL;
    WCHAR           AddrString[MAX_ADDRESS_STRING_LENGTH];
    DWORD           AddressStringLength;

    UNREFERENCED_PARAMETER(Bytes);

    QueryContext = CONTAINING_RECORD(Overlapped,
                                     QUERY_CONTEXT,
                                     QueryOverlapped);

    if (Error != ERROR_SUCCESS)
    {
        wprintf(L"ResolveName failed with %d\n", Error);
        goto exit;
    }

    wprintf(L"ResolveName succeeded. Query Results:\n");

    QueryResults = QueryContext->QueryResults;

    while(QueryResults)
    {
        AddressStringLength = MAX_ADDRESS_STRING_LENGTH;

        WSAAddressToString(QueryResults->ai_addr,
                           (DWORD)QueryResults->ai_addrlen,
                           NULL,
                           AddrString,
                           &AddressStringLength);

        wprintf(L"Ip Address: %s\n", AddrString);
        QueryResults = QueryResults->ai_next;
    }

exit:

    if (QueryContext->QueryResults)
    {
        FreeAddrInfoEx(QueryContext->QueryResults);
    }

    //
    //  Notify caller that the query completed
    //

    SetEvent(QueryContext->CompleteEvent);
    return;
}

```



<div class="alert"><b>Note</b>  Ensure that the development environment targets the newest version of <i>Ws2tcpip.h</i> which includes structure and function definitions for <a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoexw">addrinfoex</a> and <b>GetAddrInfoEx</b>, respectively.</div>
<div> </div>


<h3><a id="IDNs"></a><a id="idns"></a><a id="IDNS"></a>Internationalized Domain Names</h3>
Internet host names typically consist of a very restricted set of characters: 



<ul>
<li>Upper and lower case ASCII letters from the English alphabet.
</li>
<li>Digits from 0 to 9.</li>
<li>ASCII hyphen characters.
</li>
</ul>


With the growth of the Internet, there is a growing need to identify Internet host names for other languages not represented by the ASCII character set. Identifiers which facilitate this need and allow non-ASCII characters (Unicode) to be represented as special ASCII character strings are known as Internationalized Domain Names (IDNs). A  mechanism called
   Internationalizing Domain Names in Applications (IDNA) is used to handle
   IDNs in a standard fashion.  The specifications for IDNs and IDNA are documented in <a href="http://tools.ietf.org/html/rfc3490">RFC 3490</a>, <a href="http://tools.ietf.org/html/rfc5890">RTF 5890</a>, and <a href="http://tools.ietf.org/html/rfc6365">RFC 6365</a> published by the Internet Engineering Task Force (IETF).


On Windows 8 and Windows Server 2012, the <b>GetAddrInfoEx</b> function provides support for Internationalized Domain Name (IDN) parsing applied to the name passed in the <i>pName</i> parameter. Winsock performs Punycode/IDN encoding and conversion. This behavior can be disabled using the <b>AI_DISABLE_IDN_ENCODING</b> flag discussed below. 

On Windows 7 and Windows Server 2008 R2 or earlier, the <b>GetAddrInfoEx</b> function does not currently provide support for  IDN parsing applied to the name passed in the <i>pName</i> parameter. The wide character version of the <b>GetAddrInfoEx</b> function does not use Punycode to convert an IDN Punycode format as per <a href="http://tools.ietf.org/html/rfc3490">RFC 3490</a>. The wide character version of the <b>GetAddrInfoEx</b>  function when querying DNS encodes the Unicode name in UTF-8 format, the format used by Microsoft DNS servers in an enterprise environment.

Several functions on Windows Vista and later support conversion between Unicode labels in an IDN to their ASCII equivalents. The resulting representation of each  Unicode label contains only ASCII characters and starts with the xn-- prefix if the Unicode label contained any non-ASCII characters. The reason for this is to support existing DNS servers on the Internet, since some DNS tools and servers only support ASCII characters (see <a href="http://tools.ietf.org/html/rfc3490">RFC 3490</a>). 

 

The <a href="/windows/desktop/api/winnls/nf-winnls-idntoascii">IdnToAscii</a> function uses Punycode to convert an IDN to the ASCII  representation of the original Unicode string using the standard algorithm defined in <a href="http://tools.ietf.org/html/rfc3490">RFC 3490</a>. The <a href="/windows/desktop/api/winnls/nf-winnls-idntounicode">IdnToUnicode</a> function converts the ASCII form of an IDN to the normal Unicode UTF-16 encoding syntax. For more information and links to related draft standards, see <a href="/windows/desktop/Intl/handling-internationalized-domain-names--idns">Handling Internationalized Domain Names (IDNs)</a>.



The <a href="/windows/desktop/api/winnls/nf-winnls-idntoascii">IdnToAscii</a> function can be used to convert an IDN name to an ASCII form that then can be passed in the <i>pName</i> parameter to the <b>GetAddrInfoEx</b> function when the ASCII version of this function is used (when UNICODE and _UNICODE are not  defined). To pass this IDN name to the  <b>GetAddrInfoEx</b> function when the wide character version of this function is used (when UNICODE or _UNICODE is defined), you can use the <a href="/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar">MultiByteToWideChar</a> function to convert the <b>CHAR</b> string into a <b>WCHAR</b> string. 

<h3><a id="ai_flags"></a><a id="AI_FLAGS"></a>Use of ai_flags in the hints parameter</h3>


Flags in the <b>ai_flags</b> member of the optional 
<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoexw">addrinfoex</a> structure provided in the <i>hints</i> parameter modify the behavior of the function. 

These flag bits are defined in the <i>Ws2def.h</i> header file on the Microsoft Windows Software Development Kit (SDK) for Windows 7. These flag bits are defined in the <i>Ws2tcpip.h</i> header file on the Windows SDK for Windows Server 2008 and Windows Vista.  These flag bits are defined in the <i>Ws2tcpip.h</i> header file on the Platform Software Development Kit (SDK) for   Windows Server 2003, and Windows XP. 

The flag bits can be a combination of the following: 



<table>
<tr>
<th>Flag Bits</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="AI_PASSIVE"></a><a id="ai_passive"></a><b>AI_PASSIVE</b>

</td>
<td width="60%">
Setting the <b>AI_PASSIVE</b> flag indicates the caller intends to use the returned socket address structure in a call to the 
<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a> function. When the <b>AI_PASSIVE</b> flag is set and <i>pName</i> is a <b>NULL</b> pointer, the IP address portion of the socket address structure is set to <b>INADDR_ANY</b> for IPv4 addresses and <b>IN6ADDR_ANY_INIT</b> for IPv6 addresses.

When the <b>AI_PASSIVE</b> flag is not set, the returned socket address structure is ready for a call to the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a> function for a connection-oriented protocol, or ready for a call to either the 
<b>connect</b>, 
<a href="/windows/desktop/api/winsock/nf-winsock-sendto">sendto</a>, or 
<a href="/windows/desktop/api/winsock2/nf-winsock2-send">send</a> functions for a connectionless protocol. If the <i>pName</i> parameter is a <b>NULL</b> pointer in this case, the IP address portion of the socket address structure is set to the loopback address.

</td>
</tr>
<tr>
<td width="40%">
<a id="AI_CANONNAME"></a><a id="ai_canonname"></a><b>AI_CANONNAME</b>

</td>
<td width="60%">
If neither <b>AI_CANONNAME</b> nor <b>AI_NUMERICHOST</b> is used, the 
<b>GetAddrInfoEx</b> function attempts resolution. If a literal string is passed 
<b>GetAddrInfoEx</b> attempts to convert the string, and if a host name is passed the 
<b>GetAddrInfoEx</b> function attempts to resolve the name to an address or multiple addresses.

When the <b>AI_CANONNAME</b> bit is set, the <i>pName</i> parameter cannot be <b>NULL</b>. Otherwise the 
<b>GetAddrInfoEx</b> function will  fail with <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANO_RECOVERY</a>.

When the <b>AI_CANONNAME</b> bit is set and the 
<b>GetAddrInfoEx</b> function returns success, the <b>ai_canonname</b> member in the <i>ppResult</i> parameter points to a <b>NULL</b>-terminated string that contains the canonical name of the specified node.

<div class="alert"><b>Note</b>  The <b>GetAddrInfoEx</b> function can return success when the <b>AI_CANONNAME</b> flag is set, yet the <b>ai_canonname</b> member in the associated 
<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoa">addrinfo</a> structure is <b>NULL</b>. Therefore, the recommended use of the <b>AI_CANONNAME</b> flag includes testing whether the <b>ai_canonname</b> member in the associated 
<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoexw">addrinfoex</a> structure is <b>NULL</b>.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%">
<a id="AI_NUMERICHOST"></a><a id="ai_numerichost"></a><b>AI_NUMERICHOST</b>

</td>
<td width="60%">
When the <b>AI_NUMERICHOST</b> bit is set, the <i>pName</i> parameter must contain a non-<b>NULL</b> numeric host address string, otherwise the <b>EAI_NONAME</b> error is returned. This flag prevents a name resolution service from being called. 

</td>
</tr>
<tr>
<td width="40%">
<a id="AI_NUMERICSERV"></a><a id="ai_numericserv"></a><b>AI_NUMERICSERV</b>

</td>
<td width="60%">
When the <b>AI_NUMERICSERV</b> bit is set, the <i>pServiceName</i> parameter must contain a non-<b>NULL</b> numeric port number, otherwise the <b>EAI_NONAME</b> error is returned. This flag prevents a name resolution service from being called. 

The <b>AI_NUMERICSERV</b> flag is defined on Windows SDK for Windows Vista and later.  The <b>AI_NUMERICSERV</b> flag is not supported by Microsoft providers. 

</td>
</tr>
<tr>
<td width="40%">
<a id="AI_ALL"></a><a id="ai_all"></a><b>AI_ALL</b>

</td>
<td width="60%">
If the  <b>AI_ALL</b> bit is set, a request is made for IPv6 addresses and IPv4 addresses with <b>AI_V4MAPPED</b>. 

The <b>AI_ALL</b> flag is defined on the Windows SDK for Windows Vista and later. The <b>AI_ALL</b> flag is supported on   Windows Vista and later. 

</td>
</tr>
<tr>
<td width="40%">
<a id="AI_ADDRCONFIG"></a><a id="ai_addrconfig"></a><b>AI_ADDRCONFIG</b>

</td>
<td width="60%">
If the <b>AI_ADDRCONFIG</b> bit is set, <b>GetAddrInfoEx</b> will resolve only if a global address is configured. If <b>AI_ADDRCONFIG</b> flag is specified, IPv4 addresses shall be
   returned only if an IPv4 address is configured on the local system,
   and IPv6 addresses shall be returned only if an IPv6 address is
   configured on the local system.  The IPv4 or IPv6 loopback address is not
   considered a valid global address.

The <b>AI_ADDRCONFIG</b> flag is defined on the Windows SDK for  Windows Vista and later.    The <b>AI_ADDRCONFIG</b> flag is supported on   Windows Vista and later. 

</td>
</tr>
<tr>
<td width="40%">
<a id="AI_V4MAPPED"></a><a id="ai_v4mapped"></a><b>AI_V4MAPPED</b>

</td>
<td width="60%">
If the  <b>AI_V4MAPPED</b> bit is set and a request for IPv6 addresses fails, a name service request is made for IPv4 addresses and these addresses are converted to IPv4-mapped IPv6 address format.

The <b>AI_V4MAPPED</b> flag is defined on the Windows SDK for  Windows Vista and later.    The <b>AI_V4MAPPED</b> flag is supported on   Windows Vista and later. 

</td>
</tr>
<tr>
<td width="40%">
<a id="AI_NON_AUTHORITATIVE"></a><a id="ai_non_authoritative"></a><b>AI_NON_AUTHORITATIVE</b>

</td>
<td width="60%">
If the  <b>AI_NON_AUTHORITATIVE</b> bit is set, the <b>NS_EMAIL</b> namespace provider returns both authoritative and non-authoritative results. If the  <b>AI_NON_AUTHORITATIVE</b> bit is not set, the <b>NS_EMAIL</b> namespace provider returns only authoritative results. 

The <b>AI_NON_AUTHORITATIVE</b> flag is defined on the Windows SDK for  Windows Vista and later.    The <b>AI_NON_AUTHORITATIVE</b> flag is supported on Windows Vista and later and applies only to the <b>NS_EMAIL</b> namespace. 

</td>
</tr>
<tr>
<td width="40%">
<a id="AI_SECURE"></a><a id="ai_secure"></a><b>AI_SECURE</b>

</td>
<td width="60%">
If the  <b>AI_SECURE</b> bit is set, the <b>NS_EMAIL</b> namespace provider will return results that were obtained with enhanced security to minimize possible spoofing.

The <b>AI_SECURE</b> flag is defined on the Windows SDK for  Windows Vista and later.    The <b>AI_SECURE</b> flag is supported on Windows Vista and later and applies only to the <b>NS_EMAIL</b> namespace. 



</td>
</tr>
<tr>
<td width="40%">
<a id="AI_RETURN_PREFERRED_NAMES"></a><a id="ai_return_preferred_names"></a><b>AI_RETURN_PREFERRED_NAMES</b>

</td>
<td width="60%">
If the  <b>AI_RETURN_PREFERRED_NAMES</b> is set, then no name should be provided in the <i>pName</i> parameter. The <b>NS_EMAIL</b> namespace provider will return preferred names for publication.

The <b>AI_RETURN_PREFERRED_NAMES</b> flag is defined on the Windows SDK for  Windows Vista and later.    The <b>AI_RETURN_PREFERRED_NAMES</b> flag is supported on Windows Vista and later and applies only to the <b>NS_EMAIL</b> namespace. 

</td>
</tr>
<tr>
<td width="40%">
<a id="AI_FQDN"></a><a id="ai_fqdn"></a><b>AI_FQDN</b>

</td>
<td width="60%">
If the  <b>AI_FQDN</b> is set and a flat name (single label) is specified,  <b>GetAddrInfoEx</b> will return the fully qualified domain name that the name eventually resolved to. The fully qualified domain name is returned in the <b>ai_canonname</b> member in the associated 
<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoexw">addrinfoex</a> structure. This is different than <b>AI_CANONNAME</b> bit flag that returns the canonical name registered in DNS which may be different than the fully qualified domain name  that the flat name resolved to. 

When the <b>AI_FQDN</b> bit is set, the <i>pName</i> parameter cannot be <b>NULL</b>. Otherwise the 
<b>GetAddrInfoEx</b> function will  fail with <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANO_RECOVERY</a>.

On Windows 8 and Windows Server 2012, both the <b>AI_FQDN</b> and <b>AI_CANONNAME</b> bits can be set. If the <b>GetAddrInfoEx</b> function is called with both the <b>AI_FQDN</b> and <b>AI_CANONNAME</b> bits, the <i>ppResult</i> parameter returns a pointer to an <a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoex2w">addrinfoex2</a> structure, not an <a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoexw">addrinfoex</a> structure.


On Windows 7 and Windows Server 2008 R2, only one of the <b>AI_FQDN</b> and <b>AI_CANONNAME</b> bits can be set. The <b>GetAddrInfoEx</b> function will fail if both flags are present with <b>EAI_BADFLAGS</b>.


<b>Windows 7:  </b>The <b>AI_FQDN</b> flag is defined on the Windows SDK for  Windows 7 and later.    The <b>AI_FQDN</b> flag is supported on Windows 7 and later. 

</td>
</tr>
<tr>
<td width="40%">
<a id="AI_FILESERVER"></a><a id="ai_fileserver"></a><b>AI_FILESERVER</b>

</td>
<td width="60%">
If the  <b>AI_FILESERVER</b> is set, this is a  hint to the namespace provider that the hostname being queried is being used in file share scenario. The namespace provider may ignore this hint.


<b>Windows 7:  </b>The <b>AI_FILESERVER</b> flag is defined on the Windows SDK for  Windows 7 and later.    The <b>AI_FILESERVER</b> flag is supported on Windows 7 and later. 

</td>
</tr>
<tr>
<td width="40%">
<a id="AI_DISABLE_IDN_ENCODING"></a><a id="ai_disable_idn_encoding"></a><b>AI_DISABLE_IDN_ENCODING</b>

</td>
<td width="60%">
If the  <b>AI_DISABLE_IDN_ENCODING</b> is set, this disables the automatic International Domain Name encoding using Punycode in the name resolution functions called by the <b>GetAddrInfoEx</b> function. 

<b>Windows 8:  </b>The <b>AI_DISABLE_IDN_ENCODING</b> flag is defined on the Windows SDK for  Windows 8 and later.    The <b>AI_DISABLE_IDN_ENCODING</b> flag is supported on Windows 8 and later. 

</td>
</tr>
</table>
 







> [!NOTE]
> The ws2tcpip.h header defines GetAddrInfoEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-freeaddrinfoex">FreeAddrInfoEx</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexcancel">GetAddrInfoExCancel</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexoverlappedresult">GetAddrInfoExOverlappedResult</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfow">GetAddrInfoW</a>



<a href="/windows/desktop/api/winnls/nf-winnls-idntoascii">IdnToAscii</a>



<a href="/windows/desktop/api/winnls/nf-winnls-idntounicode">IdnToUnicode</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersa">WSAEnumNameSpaceProviders</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>



<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">Windows Sockets Error Codes</a>



<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoexw">addrinfoex</a>



<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoex2w">addrinfoex2</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-gai_strerrora">gai_strerror</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo">getaddrinfo</a>
