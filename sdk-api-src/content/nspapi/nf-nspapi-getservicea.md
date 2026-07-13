---
UID: NF:nspapi.GetServiceA
title: GetServiceA function (nspapi.h)
description: The GetService function retrieves information about a network service in the context of a set of default namespaces or a specified namespace. (ANSI)
helpviewer_keywords: ["GetServiceA", "NS_DEFAULT", "NS_DNS", "NS_NETBT", "NS_SAP", "NS_TCPIP_HOSTS", "NS_TCPIP_LOCAL", "PROP_ADDRESSES", "PROP_ALL", "PROP_COMMENT", "PROP_DISPLAY_HINT", "PROP_LOCALE", "PROP_MACHINE", "PROP_SD", "PROP_START_TIME", "PROP_VERSION", "nspapi/GetServiceA"]
old-location: winsock\getservice_2.htm
tech.root: WinSock
ms.assetid: d09ffe2d-33c3-4ca3-bc99-d7d78fd83620
ms.date: 12/05/2018
ms.keywords: GetService, GetService function [Winsock], GetServiceA, GetServiceW, NS_DEFAULT, NS_DNS, NS_NETBT, NS_SAP, NS_TCPIP_HOSTS, NS_TCPIP_LOCAL, PROP_ADDRESSES, PROP_ALL, PROP_COMMENT, PROP_DISPLAY_HINT, PROP_LOCALE, PROP_MACHINE, PROP_SD, PROP_START_TIME, PROP_VERSION, _win32_getservice_2, nspapi/GetService, nspapi/GetServiceA, nspapi/GetServiceW, winsock.getservice_2
req.header: nspapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetServiceW (Unicode) and GetServiceA (ANSI)
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
 - GetServiceA
 - nspapi/GetServiceA
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
 - GetService
 - GetServiceA
 - GetServiceW
---

# GetServiceA function


## -description

The 
<b>GetService</b> function retrieves information about a network service in the context of a set of default namespaces or a specified namespace. The network service is specified by its type and name. The information about the service is obtained as a set of 
<a href="/windows/desktop/api/nspapi/ns-nspapi-ns_service_infoa">NS_SERVICE_INFO</a> data structures.


<div class="alert"><b>Note</b>  The 
<b>GetService</b> function is a Microsoft-specific extension to the Windows Sockets 1.1 specification. This function is obsolete. For the convenience of Windows Sockets 1.1 developers, this reference material is included.</div>
<div> </div>



<div class="alert"><b>Note</b>  The functions detailed in 
<a href="/windows/desktop/WinSock/protocol-independent-name-resolution-2">Protocol-Independent Name Resolution</a> provide equivalent functionality in Windows Sockets 2.</div>
<div> </div>

## -parameters

### -param dwNameSpace [in]

The namespace, or a set of default namespaces, that the operating system should query for information about the specified network service.

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
A set of default namespaces. The operating system queries each namespace within this set. The set of default namespaces typically includes all the namespaces installed on the system. System administrators, however, can exclude particular namespaces from the set. NS_DEFAULT is the value that most applications should use for <i>dwNameSpace</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_DNS"></a><a id="ns_dns"></a><dl>
<dt><b>NS_DNS</b></dt>
</dl>
</td>
<td width="60%">
The Domain Name System used in the Internet for host name resolution.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_NETBT"></a><a id="ns_netbt"></a><dl>
<dt><b>NS_NETBT</b></dt>
</dl>
</td>
<td width="60%">
The NetBIOS over TCP/IP layer. All operating systems register their computer names with NetBIOS. This namespace is used to resolve a computer name into an IP address using this registration. Note that NS_NETBT can access a WINS server to perform the resolution.

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
Looks up host names and IP addresses in the &lt;systemroot&gt;\system32\drivers\etc\hosts file.

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
<b>GetService</b> should use the special value NS_DEFAULT. This lets a client get by without knowing available namespaces on an internetwork. The system administrator determines namespace access. Namespaces can come and go without the client having to be aware of the changes.

### -param lpGuid [in]

A pointer to a globally unique identifier (GUID) that specifies the type of the network service. The <i>Svcguid.h</i> header file includes GUID service types from many well-known services within the DNS and SAP namespaces.

The <i>Svcguid.h</i> header file is not automatically included by the <i>Winsock2.h</i> header file.

### -param lpServiceName [in]

A pointer to a zero-terminated string that uniquely represents the service name. For example, "MY SNA SERVER."

### -param dwProperties [in]

A set of bit flags that specify the service information that the function retrieves. Each of these bit flag constants, other than PROP_ALL, corresponds to a particular member of the 
<a href="/windows/desktop/api/nspapi/ns-nspapi-service_infoa">SERVICE_INFO</a> data structure. If the flag is set, the function puts information into the corresponding member of the data structures stored in *<i>lpBuffer</i>. The following bit flags are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PROP_COMMENT"></a><a id="prop_comment"></a><dl>
<dt><b>PROP_COMMENT</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the function stores data in the <b>lpComment</b> member of the data structures stored in *<i>lpBuffer</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="PROP_LOCALE"></a><a id="prop_locale"></a><dl>
<dt><b>PROP_LOCALE</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the function stores data in the <b>lpLocale</b> member of the data structures stored in *<i>lpBuffer</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="PROP_DISPLAY_HINT"></a><a id="prop_display_hint"></a><dl>
<dt><b>PROP_DISPLAY_HINT</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the function stores data in the <b>dwDisplayHint</b> member of the data structures stored in *<i>lpBuffer</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="PROP_VERSION"></a><a id="prop_version"></a><dl>
<dt><b>PROP_VERSION</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the function stores data in the <b>dwVersion</b> member of the data structures stored in *<i>lpBuffer</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="PROP_START_TIME"></a><a id="prop_start_time"></a><dl>
<dt><b>PROP_START_TIME</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the function stores data in the <b>dwTime</b> member of the data structures stored in *<i>lpBuffer</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="PROP_MACHINE"></a><a id="prop_machine"></a><dl>
<dt><b>PROP_MACHINE</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the function stores data in the <b>lpMachineName</b> member of the data structures stored in *<i>lpBuffer</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="PROP_ADDRESSES"></a><a id="prop_addresses"></a><dl>
<dt><b>PROP_ADDRESSES</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the function stores data in the <b>lpServiceAddress</b> member of the data structures stored in *<i>lpBuffer</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="PROP_SD"></a><a id="prop_sd"></a><dl>
<dt><b>PROP_SD</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the function stores data in the <b>ServiceSpecificInfo</b> member of the data structures stored in *<i>lpBuffer</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="PROP_ALL"></a><a id="prop_all"></a><dl>
<dt><b>PROP_ALL</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the function stores data in all of the members of the data structures stored in *<i>lpBuffer</i>.

</td>
</tr>
</table>

### -param lpBuffer [out]

A pointer to a buffer to receive an array of 
<a href="/windows/desktop/api/nspapi/ns-nspapi-ns_service_infoa">NS_SERVICE_INFO</a> structures and associated service information. Each 
<b>NS_SERVICE_INFO</b> structure contains service information in the context of a particular namespace. Note that if <i>dwNameSpace</i> is NS_DEFAULT, the function stores more than one structure into the buffer; otherwise, just one structure is stored.

Each 
<a href="/windows/desktop/api/nspapi/ns-nspapi-ns_service_infoa">NS_SERVICE_INFO</a> structure contains a 
<a href="/windows/desktop/api/nspapi/ns-nspapi-service_infoa">SERVICE_INFO</a> structure. The members of these 
<b>SERVICE_INFO</b> structures will contain valid data based on the bit flags that are set in the <i>dwProperties</i> parameter. If a member's corresponding bit flag is not set in <i>dwProperties</i>, the member's value is undefined.

The function stores the 
<a href="/windows/desktop/api/nspapi/ns-nspapi-ns_service_infoa">NS_SERVICE_INFO</a> structures in a consecutive array, starting at the beginning of the buffer. The pointers in the contained 
<a href="/windows/desktop/api/nspapi/ns-nspapi-service_infoa">SERVICE_INFO</a> structures point to information that is stored in the buffer between the end of the 
<b>NS_SERVICE_INFO</b> structures and the end of the buffer.

### -param lpdwBufferSize [in, out]

A pointer to a variable that, on input, contains the size, in bytes, of the buffer pointed to by <i>lpBuffer</i>. On output, this variable contains the number of bytes required to store the requested information. If this output value is greater than the input value, the function has failed due to insufficient buffer size.

### -param lpServiceAsyncInfo [in, optional]

Reserved for future use. Must be set to <b>NULL</b>.

## -returns

If the function succeeds, the return value is the number of 
<a href="/windows/desktop/api/nspapi/ns-nspapi-ns_service_infoa">NS_SERVICE_INFO</a> structures stored in *<i>lpBuffer</i>. Zero indicates that no structures were stored.

If the function fails, the return value is SOCKET_ERROR ( – 1). To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which returns one of the following extended error values.

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
The buffer pointed to by <i>lpBuffer</i> is too small to receive all of the requested information. Call the function with a buffer at least as large as the value returned in *<i>lpdwBufferSize</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SERVICE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified service was not found, or the specified namespace is not in use. The function return value is zero in this case.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/nspapi/ns-nspapi-ns_service_infoa">NS_SERVICE_INFO</a>



<a href="/windows/desktop/api/nspapi/ns-nspapi-service_infoa">SERVICE_INFO</a>



<a href="/previous-versions/windows/desktop/qos/qos-structures">SetService</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>

## -remarks

> [!NOTE]
> The nspapi.h header defines GetService as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
