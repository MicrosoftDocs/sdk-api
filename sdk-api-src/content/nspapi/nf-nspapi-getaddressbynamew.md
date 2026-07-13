---
UID: NF:nspapi.GetAddressByNameW
title: GetAddressByNameW function (nspapi.h)
description: GetAddressByName is no longer available for use as of Windows Sockets 2. (Unicode)
helpviewer_keywords: ["GetAddressByName", "GetAddressByName function [Winsock]", "GetAddressByNameW", "NS_DEFAULT", "NS_DNS", "NS_NETBT", "NS_SAP", "NS_TCPIP_HOSTS", "NS_TCPIP_LOCAL", "RES_FIND_MULTIPLE", "RES_SERVICE", "RES_SOFT_SEARCH", "_win32_getaddressbyname_2", "nspapi/GetAddressByName", "nspapi/GetAddressByNameW", "winsock.getaddressbyname_2"]
old-location: winsock\getaddressbyname_2.htm
tech.root: WinSock
ms.assetid: ea257b9e-5c5b-41fb-bcf0-7ac10b563b8c
ms.date: 12/05/2018
ms.keywords: GetAddressByName, GetAddressByName function [Winsock], GetAddressByNameA, GetAddressByNameW, NS_DEFAULT, NS_DNS, NS_NETBT, NS_SAP, NS_TCPIP_HOSTS, NS_TCPIP_LOCAL, RES_FIND_MULTIPLE, RES_SERVICE, RES_SOFT_SEARCH, _win32_getaddressbyname_2, nspapi/GetAddressByName, nspapi/GetAddressByNameA, nspapi/GetAddressByNameW, winsock.getaddressbyname_2
req.header: nspapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetAddressByNameW (Unicode) and GetAddressByNameA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mswsock.lib
req.dll: Mswsock.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetAddressByNameW
 - nspapi/GetAddressByNameW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mswsock.dll
api_name:
 - GetAddressByName
 - GetAddressByNameA
 - GetAddressByNameW
---

# GetAddressByNameW function


## -description

<p class="CCE_Message">[<b>GetAddressByName</b> is no longer available for use as of Windows Sockets 2. Instead, use the functions detailed in 
<a href="/windows/desktop/WinSock/protocol-independent-name-resolution-2">Protocol-Independent Name Resolution</a>.]

The 
<b>GetAddressByName</b> function queries a namespace, or a set of default namespaces, to retrieve network address information for a specified network service. This process is known as service name resolution. A network service can also use the function to obtain local address information that it can use with the 
<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a> function.

## -parameters

### -param dwNameSpace [in]

The namespace, or set of default namespaces, that the operating system should query for network address information.

Use one of the following constants to specify a namespace.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NS_DEFAULT"></a><a id="ns_default"></a><dl>
<dt><b>NS_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
A set of default namespaces. The function queries each namespace within this set. The set of default namespaces typically includes all the namespaces installed on the system. System administrators, however, can exclude particular namespaces from the set. This is the value that most applications should use for <i>dwNameSpace</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_DNS"></a><a id="ns_dns"></a><dl>
<dt><b>NS_DNS</b></dt>
</dl>
</td>
<td width="60%">
The Domain Name System (DNS) used in the Internet for host name resolution.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_NETBT"></a><a id="ns_netbt"></a><dl>
<dt><b>NS_NETBT</b></dt>
</dl>
</td>
<td width="60%">
The NetBIOS over TCP/IP layer. All operating systems register their computer names with NetBIOS. This namespace is used to convert a computer name to an IP address that uses this registration. Note that NS_NETBT can access a WINS server to perform the resolution.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_SAP"></a><a id="ns_sap"></a><dl>
<dt><b>NS_SAP</b></dt>
</dl>
</td>
<td width="60%">
The NetWare Service Advertising Protocol. This can access the NetWare bindery if appropriate. NS_SAP is a dynamic namespace that allows registration of services.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_TCPIP_HOSTS"></a><a id="ns_tcpip_hosts"></a><dl>
<dt><b>NS_TCPIP_HOSTS</b></dt>
</dl>
</td>
<td width="60%">
Lookup value in the &lt;systemroot&gt;\system32\drivers\etc\hosts file.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_TCPIP_LOCAL"></a><a id="ns_tcpip_local"></a><dl>
<dt><b>NS_TCPIP_LOCAL</b></dt>
</dl>
</td>
<td width="60%">
Local TCP/IP name resolution mechanisms, including comparisons against the local host name and looks up host names and IP addresses in cache of host to IP address mappings.

</td>
</tr>
</table>
 

Most calls to 
<b>GetAddressByName</b> should use the special value NS_DEFAULT. This lets a client get by with no knowledge of which namespaces are available on an internetwork. The system administrator determines namespace access. Namespaces can come and go without the client having to be aware of the changes.

### -param lpServiceType [in]

A pointer to a globally unique identifier (GUID) that specifies the type of the network service. The Svcguid.h header file includes definitions of several GUID service types, and macros for working with them.

The Svcguid.h header file is not automatically included by the Winsock2.h header file.

### -param lpServiceName [in, optional]

A pointer to a zero-terminated string that uniquely represents the service name. For example, "MY SNA SERVER".

Setting <i>lpServiceName</i> to <b>NULL</b> is the equivalent of setting <i>dwResolution</i> to RES_SERVICE. The function operates in its second mode, obtaining the local address to which a service of the specified type should bind. The function stores the local address within the <b>LocalAddr</b> member of the 
<a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info">CSADDR_INFO</a> structures stored into *<i>lpCsaddrBuffer</i>.

If <i>dwResolution</i> is set to RES_SERVICE, the function ignores the <i>lpServiceName</i> parameter.

If <i>dwNameSpace</i> is set to NS_DNS, *<i>lpServiceName</i> is the name of the host.

### -param lpiProtocols [in, optional]

A pointer to a zero-terminated array of protocol identifiers. The function restricts a name resolution attempt to namespace providers that offer these protocols. This lets the caller limit the scope of the search.

If <i>lpiProtocols</i> is set to <b>NULL</b>, the function retrieves information on all available protocols.

### -param dwResolution [in]

A set of bit flags that specify aspects of the service name resolution process. The following bit flags are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RES_SERVICE"></a><a id="res_service"></a><dl>
<dt><b>RES_SERVICE</b></dt>
</dl>
</td>
<td width="60%">
If set, the function retrieves the address to which a service of the specified type should bind. This is the equivalent to setting the <i>lpServiceName</i> parameter to <b>NULL</b>.

If this flag is clear, normal name resolution occurs.

</td>
</tr>
<tr>
<td width="40%"><a id="RES_FIND_MULTIPLE"></a><a id="res_find_multiple"></a><dl>
<dt><b>RES_FIND_MULTIPLE</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the operating system performs an extensive search of all namespaces for the service. It asks every appropriate namespace to resolve the service name. If this flag is clear, the operating system stops looking for service addresses as soon as one is found.

</td>
</tr>
<tr>
<td width="40%"><a id="RES_SOFT_SEARCH"></a><a id="res_soft_search"></a><dl>
<dt><b>RES_SOFT_SEARCH</b></dt>
</dl>
</td>
<td width="60%">
This flag is valid if the namespace supports multiple levels of searching.

If this flag is valid and set, the operating system performs a simple and quick search of the namespace. This is useful if an application only needs to obtain easy-to-find addresses for the service.

If this flag is valid and clear, the operating system performs a more extensive search of the namespace.

</td>
</tr>
</table>

### -param lpServiceAsyncInfo [in, optional]

Reserved for future use; must be set to <b>NULL</b>.

### -param lpCsaddrBuffer [out]

A pointer to a buffer to receive one or more 
<a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info">CSADDR_INFO</a> data structures. The number of structures written to the buffer depends on the amount of information found in the resolution attempt. You should assume that multiple structures will be written, although in many cases there will only be one.

### -param lpdwBufferLength [in, out]

A pointer to a variable that, upon input, specifies the size, in bytes, of the buffer pointed to by <i>lpCsaddrBuffer</i>.

Upon output, this variable contains the total number of bytes required to store the array of 
<a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info">CSADDR_INFO</a> structures. If this value is less than or equal to the input value of *<i>lpdwBufferLength</i>, and the function is successful, this is the number of bytes actually stored in the buffer. If this value is greater than the input value of *<i>lpdwBufferLength</i>, the buffer was too small, and the output value of *<i>lpdwBufferLength</i> is the minimal required buffer size.

### -param lpAliasBuffer [in, out]

A pointer to a buffer to receive alias information for the network service.

If a namespace supports aliases, the function stores an array of zero-terminated name strings into the buffer pointed to by <i>lpAliasBuffer</i>. There is a double zero-terminator at the end of the list. The first name in the array is the service's primary name. Names that follow are aliases. An example of a namespace that supports aliases is DNS.

If a namespace does not support aliases, it stores a double zero-terminator into the buffer.

This parameter is optional, and can be set to <b>NULL</b>.

### -param lpdwAliasBufferLength [in, out]

A pointer to a variable that, upon input, specifies the size, in elements (characters), of the buffer pointed to by <i>lpAliasBuffer</i>.

Upon output, this variable contains the total number of elements (characters) required to store the array of name strings. If this value is less than or equal to the input value of *<i>lpdwAliasBufferLength</i>, and the function is successful, this is the number of elements actually stored in the buffer. If this value is greater than the input value of *<i>lpdwAliasBufferLength</i>, the buffer was too small, and the output value of *<i>lpdwAliasBufferLength</i> is the minimal required buffer size.

If <i>lpAliasBuffer</i> is <b>NULL</b>, <i>lpdwAliasBufferLength</i> is meaningless and can also be <b>NULL</b>.

## -returns

If the function succeeds, the return value is the number of 
<a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info">CSADDR_INFO</a> data structures written to the buffer pointed to by <i>lpCsaddrBuffer</i>.

If the function fails, the return value is SOCKET_ERROR( –1). To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which returns the following extended error value.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by <i>lpCsaddrBuffer</i> was too small to receive all of the relevant 
<a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info">CSADDR_INFO</a> structures. Call the function with a buffer at least as large as the value returned in *<i>lpdwBufferLength</i>.

</td>
</tr>
</table>

## -remarks

This function is a more powerful version of the 
<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname">gethostbyname</a> function. The 
<b>GetAddressByName</b> function works with multiple name services.


<div class="alert"><b>Note</b>  The 
<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname">gethostbyname</a> function has been deprecated by the introduction of the 
<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo">getaddrinfo</a> function. Developers creating Windows Sockets 2 applications are urged to use the 
<b>getaddrinfo</b> function instead of 
<b>gethostbyname</b>.</div>
<div> </div>


The 
<b>GetAddressByName</b> function lets a client obtain a Windows Sockets address for a network service. The client specifies the service of interest by its service type and service name.

Many name services support a default prefix or suffix that the name service provider considers when resolving service names. For example, in the DNS namespace, if a domain is named "nt.microsoft.com", and "ftp millikan" is provided as input, the DNS software fails to resolve "millikan", but successfully resolves "millikan.nt.microsoft.com".

Note that the 
<b>GetAddressByName</b> function can search for a service address in two ways: within a particular namespace, or within a set of default namespaces. Using a default namespace, an administrator can specify that certain namespaces will be searched for service addresses only if specified by name. An administrator or namespace—setup program can also control the ordering of namespace searches.





> [!NOTE]
> The nspapi.h header defines GetAddressByName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info">CSADDR_INFO</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo">getaddrinfo</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname">gethostbyname</a>
