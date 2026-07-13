---
UID: NF:winsock2.WSALookupServiceBeginA
title: WSALookupServiceBeginA function (winsock2.h)
description: The WSALookupServiceBegin function initiates a client query that is constrained by the information contained within a WSAQUERYSET structure. (ANSI)
helpviewer_keywords: ["LUP_CONTAINERS", "LUP_DEEP", "LUP_FLUSHCACHE", "LUP_FLUSHPREVIOUS", "LUP_NEAREST", "LUP_NOCONTAINERS", "LUP_RES_SERVICE", "LUP_RETURN_ADDR", "LUP_RETURN_ALIASES", "LUP_RETURN_ALL", "LUP_RETURN_BLOB", "LUP_RETURN_COMMENT", "LUP_RETURN_NAME", "LUP_RETURN_QUERY_STRING", "LUP_RETURN_TYPE", "LUP_RETURN_VERSION", "WSALookupServiceBeginA", "winsock2/WSALookupServiceBeginA"]
old-location: winsock\wsalookupservicebegin_2.htm
tech.root: WinSock
ms.assetid: 448309ef-b9dd-4960-8016-d26691df59ec
ms.date: 12/05/2018
ms.keywords: LUP_CONTAINERS, LUP_DEEP, LUP_FLUSHCACHE, LUP_FLUSHPREVIOUS, LUP_NEAREST, LUP_NOCONTAINERS, LUP_RES_SERVICE, LUP_RETURN_ADDR, LUP_RETURN_ALIASES, LUP_RETURN_ALL, LUP_RETURN_BLOB, LUP_RETURN_COMMENT, LUP_RETURN_NAME, LUP_RETURN_QUERY_STRING, LUP_RETURN_TYPE, LUP_RETURN_VERSION, WSALookupServiceBegin, WSALookupServiceBegin function [Winsock], WSALookupServiceBeginA, WSALookupServiceBeginW, _win32_wsalookupservicebegin_2, winsock.wsalookupservicebegin_2, winsock2/WSALookupServiceBegin, winsock2/WSALookupServiceBeginA, winsock2/WSALookupServiceBeginW
req.header: winsock2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WSALookupServiceBeginW (Unicode) and WSALookupServiceBeginA (ANSI)
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
 - WSALookupServiceBeginA
 - winsock2/WSALookupServiceBeginA
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
 - WSALookupServiceBegin
 - WSALookupServiceBeginA
 - WSALookupServiceBeginW
---

# WSALookupServiceBeginA function


## -description

The 
<b>WSALookupServiceBegin</b> function initiates a client query that is constrained by the information contained within a 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw">WSAQUERYSET</a> structure. 
<b>WSALookupServiceBegin</b> only returns a handle, which should be used by subsequent calls to 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta">WSALookupServiceNext</a> to get the actual results.

## -parameters

### -param lpqsRestrictions [in]

A pointer to the search criteria. See the Remarks for details.

### -param dwControlFlags [in]

A set of flags that controls the depth of the search.

Supported values for the <i>dwControlFlags</i> parameter are defined in the <i>Winsock2.h</i> header file and can be a combination of the following options.



<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LUP_DEEP"></a><a id="lup_deep"></a><dl>
<dt><b>LUP_DEEP</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Queries deep as opposed to just the first level.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_CONTAINERS"></a><a id="lup_containers"></a><dl>
<dt><b>LUP_CONTAINERS</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Returns containers only.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_NOCONTAINERS"></a><a id="lup_nocontainers"></a><dl>
<dt><b>LUP_NOCONTAINERS</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
Do not return containers.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_NEAREST"></a><a id="lup_nearest"></a><dl>
<dt><b>LUP_NEAREST</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
If possible, returns results in the order of distance. The measure of distance is provider specific.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_RETURN_NAME"></a><a id="lup_return_name"></a><dl>
<dt><b>LUP_RETURN_NAME</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
Retrieves the name as <i>lpszServiceInstanceName</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_RETURN_TYPE"></a><a id="lup_return_type"></a><dl>
<dt><b>LUP_RETURN_TYPE</b></dt>
<dt>0x0020</dt>
</dl>
</td>
<td width="60%">
Retrieves the type as <i>lpServiceClassId</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_RETURN_VERSION"></a><a id="lup_return_version"></a><dl>
<dt><b>LUP_RETURN_VERSION</b></dt>
<dt>0x0040</dt>
</dl>
</td>
<td width="60%">
Retrieves the version as <i>lpVersion</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_RETURN_COMMENT"></a><a id="lup_return_comment"></a><dl>
<dt><b>LUP_RETURN_COMMENT</b></dt>
<dt>0x0080</dt>
</dl>
</td>
<td width="60%">
Retrieves the comment as <i>lpszComment</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_RETURN_ADDR"></a><a id="lup_return_addr"></a><dl>
<dt><b>LUP_RETURN_ADDR</b></dt>
<dt>0x0100</dt>
</dl>
</td>
<td width="60%">
Retrieves the addresses as <i>lpcsaBuffer</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_RETURN_BLOB"></a><a id="lup_return_blob"></a><dl>
<dt><b>LUP_RETURN_BLOB</b></dt>
<dt>0x0200</dt>
</dl>
</td>
<td width="60%">
Retrieves the private data as <i>lpBlob</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_RETURN_ALIASES"></a><a id="lup_return_aliases"></a><dl>
<dt><b>LUP_RETURN_ALIASES</b></dt>
<dt>0x0400</dt>
</dl>
</td>
<td width="60%">
Any available alias information is to be returned in successive calls to 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta">WSALookupServiceNext</a>, and each alias returned will have the RESULT_IS_ALIAS flag set.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_RETURN_QUERY_STRING"></a><a id="lup_return_query_string"></a><dl>
<dt><b>LUP_RETURN_QUERY_STRING</b></dt>
<dt>0x0800</dt>
</dl>
</td>
<td width="60%">
Retrieves the query string used for the request.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_RETURN_ALL"></a><a id="lup_return_all"></a><dl>
<dt><b>LUP_RETURN_ALL</b></dt>
<dt>0x0FF0</dt>
</dl>
</td>
<td width="60%">
A set of flags that retrieves all of the LUP_RETURN_* values.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_FLUSHPREVIOUS"></a><a id="lup_flushprevious"></a><dl>
<dt><b>LUP_FLUSHPREVIOUS</b></dt>
<dt>0x1000</dt>
</dl>
</td>
<td width="60%">
Used as a value for the <i>dwControlFlags</i> parameter in 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta">WSALookupServiceNext</a>. Setting this flag instructs the provider to discard the last result set, which was too large for the specified buffer, and move on to the next result set.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_FLUSHCACHE"></a><a id="lup_flushcache"></a><dl>
<dt><b>LUP_FLUSHCACHE</b></dt>
<dt>0x2000</dt>
</dl>
</td>
<td width="60%">
If the provider has been caching information, ignores the cache, and queries the namespace itself.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_RES_SERVICE"></a><a id="lup_res_service"></a><dl>
<dt><b>LUP_RES_SERVICE</b></dt>
<dt>0x8000</dt>
</dl>
</td>
<td width="60%">
This indicates whether prime response is in the remote or local part of 
<a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info">CSADDR_INFO</a> structure. The other part needs to be usable in either case.

</td>
</tr>
</table>

### -param lphLookup [out]

A  handle to be used when calling 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta">WSALookupServiceNext</a> in order to start retrieving the results set.

## -returns

The return value is zero if the operation was successful. Otherwise, the value SOCKET_ERROR is returned, and a specific error number can be retrieved by calling 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>.

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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
One or more parameters were missing or invalid for this provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANO_DATA</a></b></dt>
</dl>
</td>
<td width="60%">
The name was found in the database but no data matching the given restrictions was located.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
The WS2_32.DLL has not been initialized. The application must first call 
<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a> before calling any Windows Sockets functions.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSASERVICE_NOT_FOUND</a></b></dt>
</dl>
</td>
<td width="60%">
No such service is known. The service cannot be found in the specified name space.

This error is returned for a bluetooth service discovery request if no remote bluetooth devices were found.

</td>
</tr>
</table>

## -remarks

The <i>lpqsRestrictions</i> parameter points to a buffer containing a <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw">WSAQUERYSET</a> structure. At a minimum, the <b>dwSize</b> member of the <b>WSAQUERYSET</b> must be set to the length of the buffer before calling the 
<b>WSALookupServiceBegin</b> function. Applications can restrict the query by specifying other members in the <b>WSAQUERYSET</b>. 

In most instances, applications interested in only a particular transport protocol should constrain their query by address family and protocol using the <b>dwNumberOfProtocols</b> and <b>lpafpProtocols</b> members of the <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw">WSAQUERYSET</a> rather than by specifiying the namespace in the <b>dwNameSpace</b> member. 

Information on supported network transport protocols can be retreived using the <a href="/windows/desktop/api/nspapi/nf-nspapi-enumprotocolsa">EnumProtocols</a>, <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumprotocolsa">WSAEnumProtocols</a>, <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumprotocols">WSCEnumProtocols</a>, or  <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumprotocols32">WSCEnumProtocols32</a> function.

It is also possible to constrain the query to a single namespace. For example, a query that only wants results from DNS (not results from the local hosts file and other naming services) would set the <b>dwNameSpace</b> member to NS_DNS. For example, a bluetooth device discovery would set the <b>dwNameSpace</b> member to NS_BTH. 

Applications can also restrict the query to a specific namespace provider by specifying a pointer to the GUID for the provider in the <b>lpNSProviderId</b> member. 

Information on namespace providers on the local computer can be retrieved using the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersa">WSAEnumNameSpaceProviders</a>, <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersexa">WSAEnumNameSpaceProvidersEx</a>, <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumnamespaceproviders32">WSCEnumNameSpaceProviders32</a>, or <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumnamespaceprovidersex32">WSCEnumNameSpaceProvidersEx32</a> function. 

If LUP_CONTAINERS is specified in a call, other restriction values should be avoided. If any are specified, it is up to the name service provider to decide if it can support this restriction over the containers. If it cannot, it should return an error.

Some name service providers can have other means of finding containers. For example, containers might all be of some well-known type, or of a set of well-known types, and therefore a query restriction can be created for finding them. No matter what other means the name service provider has for locating containers, LUP_CONTAINERS and LUP_NOCONTAINERS take precedence. Hence, if a query restriction is given that includes containers, specifying LUP_NOCONTAINERS will prevent the container items from being returned. Similarly, no matter the query restriction, if LUP_CONTAINERS is given, only containers should be returned. If a namespace does not support containers, and LUP_CONTAINERS is specified, it should simply return <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANO_DATA</a>.

The preferred method of obtaining the containers within another container, is the call:


```cpp
dwStatus = WSALookupServiceBegin(
      lpqsRestrictions,
      LUP_CONTAINERS,
      lphLookup);

```


This call is followed by the requisite number of 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta">WSALookupServiceNext</a> calls. This will return all containers contained immediately within the starting context; that is, it is not a deep query. With this, one can map the address space structure by walking the hierarchy, perhaps enumerating the content of selected containers. Subsequent uses of 
<b>WSALookupServiceBegin</b> use the containers returned from a previous call.

As mentioned above, a 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw">WSAQUERYSET</a> structure is used as an input parameter to <b>WSALookupBegin</b> in order to qualify the query. The following table indicates how the 
<b>WSAQUERYSET</b> is used to construct a query. When a parameter is marked as (Optional) a <b>NULL</b> pointer can be specified, indicating that the parameter will not be used as a search criteria. See section 
<a href="/windows/desktop/WinSock/name-resolution-data-structures-2">Query-Related Data Structures</a> for additional information.

<table>
<tr>
<th>WSAQUERYSET member</th>
<th>Query interpretation</th>
</tr>
<tr>
<td><b>dwSize</b></td>
<td>Must be set to sizeof(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw">WSAQUERYSET</a>). This is a versioning mechanism.</td>
</tr>
<tr>
<td><b>dwOutputFlags</b></td>
<td>Ignored for queries.</td>
</tr>
<tr>
<td><b>lpszServiceInstanceName</b></td>
<td>(Optional) Referenced string contains service name. The semantics for wildcarding within the string are not defined, but can be supported by certain namespace providers.</td>
</tr>
<tr>
<td><b>lpServiceClassId</b></td>
<td>(Required) The GUID corresponding to the service class.</td>
</tr>
<tr>
<td><b>lpVersion</b></td>
<td>(Optional) References desired version number and provides version comparison semantics (that is, version must match exactly, or version must be not less than the value specified).</td>
</tr>
<tr>
<td><b>lpszComment</b></td>
<td>Ignored for queries.</td>
</tr>
<tr>
<td>
<b>dwNameSpace</b>

See the Important note that follows.

</td>
<td>Identifier of a single namespace in which to constrain the search, or NS_ALL to include all namespaces.</td>
</tr>
<tr>
<td><b>lpNSProviderId</b></td>
<td>(Optional) References the GUID of a specific namespace provider, and limits the query to this provider only.</td>
</tr>
<tr>
<td><b>lpszContext</b></td>
<td>(Optional) Specifies the starting point of the query in a hierarchical namespace.</td>
</tr>
<tr>
<td><b>dwNumberOfProtocols</b></td>
<td>Size of the protocol constraint array, can be zero.</td>
</tr>
<tr>
<td><b>lpafpProtocols</b></td>
<td>(Optional) References an array of 
<a href="/windows/desktop/api/winsock2/ns-winsock2-afprotocols">AFPROTOCOLS</a> structure. Only services that utilize these protocols will be returned.</td>
</tr>
<tr>
<td><b>lpszQueryString</b></td>
<td>(Optional) Some namespaces (such as whois++) support enriched SQL-like queries that are contained in a simple text string. This parameter is used to specify that string.</td>
</tr>
<tr>
<td><b>dwNumberOfCsAddrs</b></td>
<td>Ignored for queries.</td>
</tr>
<tr>
<td><b>lpcsaBuffer</b></td>
<td>Ignored for queries.</td>
</tr>
<tr>
<td><b>lpBlob</b></td>
<td>(Optional) This is a pointer to a provider-specific entity.</td>
</tr>
</table>
 

<div class="alert"><b>Important</b>  In most instances, applications interested in only a particular transport protocol should constrain their query by address family and protocol rather than by namespace. This would allow an application that needs to locate a TCP/IP service, for example, to have its query processed by all available namespaces such as the local hosts file, DNS, and NIS.</div>
<div> </div>
<b>Windows Phone 8:</b> The <b>WSALookupServiceBeginW</b> function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: The <b>WSALookupServiceBeginW</b> function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.





> [!NOTE]
> The winsock2.h header defines WSALookupServiceBegin as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Bluetooth/bluetooth-and-wsalookupservicebegin-for-service-discovery">Bluetooth and WSALookupServiceBegin</a>



<a href="/windows/desktop/api/nspapi/nf-nspapi-enumprotocolsa">EnumProtocols</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersa">WSAEnumNameSpaceProviders</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersexa">WSAEnumNameSpaceProvidersEx</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumprotocolsa">WSAEnumProtocols</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend">WSALookupServiceEnd</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta">WSALookupServiceNext</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw">WSAQUERYSET</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumnamespaceproviders32">WSCEnumNameSpaceProviders32</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumnamespaceprovidersex32">WSCEnumNameSpaceProvidersEx32</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumprotocols">WSCEnumProtocols</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumprotocols32">WSCEnumProtocols32</a>
