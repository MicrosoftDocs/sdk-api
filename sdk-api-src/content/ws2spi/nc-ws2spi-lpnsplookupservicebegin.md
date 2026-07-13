---
UID: NC:ws2spi.LPNSPLOOKUPSERVICEBEGIN
title: LPNSPLOOKUPSERVICEBEGIN (ws2spi.h)
description: Initiates a client query that is constrained by the information contained within a WSAQUERYSET structure.
helpviewer_keywords: ["LPNSPLOOKUPSERVICEBEGIN","LUP_ADDRCONFIG","LUP_CONTAINERS","LUP_DEEP","LUP_DUAL_ADDR","LUP_FLUSHCACHE","LUP_FLUSHPREVIOUS","LUP_NEAREST","LUP_NOCONTAINERS","LUP_NON_AUTHORITATIVE","LUP_RES_RESERVICE","LUP_RETURN_ADDR","LUP_RETURN_ALIASES","LUP_RETURN_ALL","LUP_RETURN_BLOB","LUP_RETURN_COMMENT","LUP_RETURN_NAME","LUP_RETURN_PREFERRED_NAMES","LUP_RETURN_QUERY_STRING","LUP_RETURN_TYPE","LUP_RETURN_VERSION","LUP_SECURE","NSPLookupServiceBegin","NSPLookupServiceBegin function [Winsock]","_win32_nsplookupservicebegin_2","winsock.nsplookupservicebegin_2","ws2spi/NSPLookupServiceBegin"]
old-location: winsock\nsplookupservicebegin_2.htm
tech.root: WinSock
ms.assetid: a0b71821-4434-470f-b729-370d7e1722ec
ms.date: 12/05/2018
ms.keywords: LPNSPLOOKUPSERVICEBEGIN, LUP_ADDRCONFIG, LUP_CONTAINERS, LUP_DEEP, LUP_DUAL_ADDR, LUP_FLUSHCACHE, LUP_FLUSHPREVIOUS, LUP_NEAREST, LUP_NOCONTAINERS, LUP_NON_AUTHORITATIVE, LUP_RES_RESERVICE, LUP_RETURN_ADDR, LUP_RETURN_ALIASES, LUP_RETURN_ALL, LUP_RETURN_BLOB, LUP_RETURN_COMMENT, LUP_RETURN_NAME, LUP_RETURN_PREFERRED_NAMES, LUP_RETURN_QUERY_STRING, LUP_RETURN_TYPE, LUP_RETURN_VERSION, LUP_SECURE, NSPLookupServiceBegin, NSPLookupServiceBegin function [Winsock], _win32_nsplookupservicebegin_2, winsock.nsplookupservicebegin_2, ws2spi/NSPLookupServiceBegin
req.header: ws2spi.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPNSPLOOKUPSERVICEBEGIN
 - ws2spi/LPNSPLOOKUPSERVICEBEGIN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ws2spi.h
api_name:
 - NSPLookupServiceBegin
---

# LPNSPLOOKUPSERVICEBEGIN callback function


## -description

The 
**NSPLookupServiceBegin** function initiates a client query of a name service provider that is constrained by the information contained within a 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw">WSAQUERYSET</a> structure.

**NSPLookupServiceBegin** only returns a handle, which should be used by subsequent calls to 
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicenext">NSPLookupServiceNext</a> to get the actual results. Because this operation cannot be canceled, it should be implemented to execute quickly. While it is acceptable to initiate a network query, this function should not require a response  to return successfully.

## -parameters

### -param lpProviderId [in]

A pointer to the name service provider identifier to query.

### -param lpqsRestrictions [in]

A pointer to the search criteria. See Remarks.

### -param lpServiceClassInfo [in]

A pointer to the  <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaserviceclassinfow">WSASERVICECLASSINFO</a> structure that contains schema information for the service.

### -param dwControlFlags [in]

A value that controls the depth of the search.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LUP_DEEP"></a><a id="lup_deep"></a><dl>
<dt><b>LUP_DEEP</b></dl>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Queries down the hierarchy of a provider as opposed to just the first level.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_CONTAINERS"></a><a id="lup_containers"></a><dl>
<dt><b>LUP_CONTAINERS</b></dl>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Returns containers only.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_NOCONTAINERS"></a><a id="lup_nocontainers"></a><dl>
<dt><b>LUP_NOCONTAINERS</b></dl>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
Returns no containers.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_NEAREST"></a><a id="lup_nearest"></a><dl>
<dt><b>LUP_NEAREST</b></dl>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
If possible, returns results in the order of distance. The measure of distance is provider specific.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_RETURN_NAME"></a><a id="lup_return_name"></a><dl>
<dt><b>LUP_RETURN_NAME</b></dl>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
Retrieves the name as **lpszServiceInstanceName**.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_RETURN_TYPE"></a><a id="lup_return_type"></a><dl>
<dt><b>LUP_RETURN_TYPE</b></dl>
<dt>0x0020</dt>
</dl>
</td>
<td width="60%">
Retrieves the type as **lpServiceClassId**.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_RETURN_VERSION"></a><a id="lup_return_version"></a><dl>
<dt><b>LUP_RETURN_VERSION</b></dl>
<dt>0x0040</dt>
</dl>
</td>
<td width="60%">
Retrieves the version as **lpVersion**.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_RETURN_COMMENT"></a><a id="lup_return_comment"></a><dl>
<dt><b>LUP_RETURN_COMMENT</b></dl>
<dt>0x0080</dt>
</dl>
</td>
<td width="60%">
Retrieves the comment as **lpszComment**.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_RETURN_ADDR"></a><a id="lup_return_addr"></a><dl>
<dt><b>LUP_RETURN_ADDR</b></dl>
<dt>0x0100</dt>
</dl>
</td>
<td width="60%">
Retrieves the addresses as **lpcsaBuffer**.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_RETURN_BLOB"></a><a id="lup_return_blob"></a><dl>
<dt><b>LUP_RETURN_BLOB</b></dl>
<dt>0x0200</dt>
</dl>
</td>
<td width="60%">
Retrieves the private data as **lpBlob**.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_RETURN_ALIASES"></a><a id="lup_return_aliases"></a><dl>
<dt><b>LUP_RETURN_ALIASES</b></dl>
<dt>0x0400</dt>
</dl>
</td>
<td width="60%">
Any available alias information is to be returned in successive calls to 
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicenext">NSPLookupServiceNext</a>, and each alias returned will have the **RESULT_IS_ALIAS** flag set.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_RETURN_QUERY_STRING"></a><a id="lup_return_query_string"></a><dl>
<dt><b>LUP_RETURN_QUERY_STRING</b></dl>
<dt>0x0800</dt>
</dl>
</td>
<td width="60%">
Retrieves the query string as **lpszQueryString**.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_RETURN_ALL"></a><a id="lup_return_all"></a><dl>
<dt><b>LUP_RETURN_ALL</b></dl>
<dt>0x0ff0</dt>
</dl>
</td>
<td width="60%">
Retrieves information including the name, type, version, comment, address, blob, aliases, and query string.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_FLUSHCACHE"></a><a id="lup_flushcache"></a><dl>
<dt><b>LUP_FLUSHCACHE</b></dl>
<dt>0x1000</dt>
</dl>
</td>
<td width="60%">
If the provider has cached information, ignore the cache and query the namespace itself.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_FLUSHPREVIOUS"></a><a id="lup_flushprevious"></a><dl>
<dt><b>LUP_FLUSHPREVIOUS</b></dl>
<dt>0x2000</dt>
</dl>
</td>
<td width="60%">
Used as a value for the <i>dwControlFlags</i> parameter in 
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicenext">NSPLookupServiceNext</a>. Setting this flag instructs the provider to discard the last result set, which was too large for the supplied buffer, and move on to the next result set.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_NON_AUTHORITATIVE"></a><a id="lup_non_authoritative"></a><dl>
<dt><b>LUP_NON_AUTHORITATIVE</b></dl>
<dt>0x4000</dt>
</dl>
</td>
<td width="60%">
Indicates that the namespace provider should included non-authoritative results for names. 

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_RES_RESERVICE"></a><a id="lup_res_reservice"></a><dl>
<dt><b>LUP_RES_RESERVICE</b></dl>
<dt>0x8000</dt>
</dl>
</td>
<td width="60%">
Indicates whether prime response is in the remote or local part of 
<a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info">CSADDR_INFO</a> structure. The other part must be usable in either case. This option applies only to service instance requests.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_SECURE"></a><a id="lup_secure"></a><dl>
<dt><b>LUP_SECURE</b></dl>
<dt>0x8000</dt>
</dl>
</td>
<td width="60%">
Indicates that the namespace provider should use a secure query. This option only applies to name query requests. 

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_RETURN_PREFERRED_NAMES"></a><a id="lup_return_preferred_names"></a><dl>
<dt><b>LUP_RETURN_PREFERRED_NAMES</b></dl>
<dt>0x10000</dt>
</dl>
</td>
<td width="60%">
Indicates that the namespace provider should return only preferred names. 

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_ADDRCONFIG"></a><a id="lup_addrconfig"></a><dl>
<dt><b>LUP_ADDRCONFIG</b></dl>
<dt>0x100000</dt>
</dl>
</td>
<td width="60%">
Indicates that the namespace provider should return the address configuration. 

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_DUAL_ADDR"></a><a id="lup_dual_addr"></a><dl>
<dt><b>LUP_DUAL_ADDR</b></dl>
<dt>0x200000</dt>
</dl>
</td>
<td width="60%">
Indicates that the namespace provider should return the dual addresses. This option only applies to dual-mode sockets (IPv6 and IPv4 mapped addresses).

</td>
</tr>
</table>

### -param lphLookup [out]

A pointer to the handle to be used in subsequent calls to 
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicenext">NSPLookupServiceNext</a> in order to retrieve the results set.

## -returns

The function should return **NO_ERROR** (zero) if the routine succeeds. It should return **SOCKET_ERROR** (–1) if the routine fails and it must set the appropriate error code using 
<a href="/windows/desktop/api/winsock/nf-winsock-wsasetlasterror">WSASetLastError</a>.



<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_NOT_ENOUGH_MEMORY</a></b></dl>
</dl>
</td>
<td width="60%">
There is not enough memory available to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dl>
</dl>
</td>
<td width="60%">
One or more parameters were invalid, or missing, for this provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2#WSAEOPNOTSUPP">WSAEOPNOTSUPP</a></b></dl>
</dl>
</td>
<td width="60%">
The operation is not supported. This error is returned if the namespace provider does not implement this function. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANO_DATA</a></b></dl>
</dl>
</td>
<td width="60%">
The name was found in the database, but it does not have the correct associated data that is resolved for.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSASERVICE_NOT_FOUND</a></b></dl>
</dl>
</td>
<td width="60%">
Service is unknown. The service cannot be found in the specified namespace.

</td>
</tr>
</table>

## -remarks

If **LUP_CONTAINERS** is specified in a call, avoid all other restriction values. If any are supplied, the name service provider must decide if it can support this restriction over the containers. If not, it should return an error.

Some name service providers may have other means of finding containers. For example, containers can all be of some well-known type, or of a set of well-known types, and therefore a query restriction could be created for finding them. No matter what other means the name service provider has for locating containers, **LUP_CONTAINERS** and **LUP_NOCONTAINERS** take precedence. Therefore, if a query restriction is given that includes containers, specifying **LUP_NOCONTAINERS** will prevent the container items from being returned. Similarly, no matter what the query restriction, if **LUP_CONTAINERS** is given, only containers should be returned. If a namespace does not support containers and **LUP_CONTAINERS** is specified, it should return <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANO_DATA</a>.

The preferred method of obtaining the containers within another container, is the call:


```cpp
dwStatus = NSPLookupServiceBegin(
    lpqsRestrictions,
    LUP_CONTAINERS,
    lphLookup);

```


followed by the requisite number of 
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicenext">NSPLookupServiceNext</a> calls. This will return all containers contained immediately within the starting context; that is, it is not a deep query. With this, one can map the address space structure by walking the hierarchy, perhaps enumerating the content of selected containers. Subsequent uses of 
**NSPLookupServiceBegin** use the containers returned from a previous call.

<h3><a id="Forming_Queries"></a><a id="forming_queries"></a><a id="FORMING_QUERIES"></a>Forming Queries</h3>


As mentioned, a 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw">WSAQUERYSET</a> structure is used as an input parameter to 
**NSPLookupServiceBegin** to qualify the query. The following table lists **WSAQUERYSET** member names and describes how the 
**WSAQUERYSET** is used to construct a query. When a member is marked as (Optional) a null pointer can be supplied, indicating that the parameter will not be used as a search criteria. For more information, see <a href="/windows/desktop/WinSock/name-resolution-data-structures-2">Query-Related Data Structures</a>.

<table>
<tr>
<th>WSAQUERYSET member name</th>
<th>Query interpretation</th>
</tr>
<tr>
<td>**dwSize**</td>
<td>Will be set to sizeof(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw">WSAQUERYSET</a>). This is a versioning mechanism.</td>
</tr>
<tr>
<td>**dwOutputFlags**</td>
<td>Ignored for queries.</td>
</tr>
<tr>
<td>**lpszServiceInstanceName**</td>
<td>Optional. Referenced string contains service name. The semantics for wildcarding within the string are not defined, but can be supported by certain namespace providers.</td>
</tr>
<tr>
<td>**lpServiceClassId**</td>
<td>Required. GUID corresponding to the service class.</td>
</tr>
<tr>
<td>**lpVersion**</td>
<td>Optional. References desired version number and provides version comparison semantics (that is, version must match exactly, or version must be not less than the value supplied).</td>
</tr>
<tr>
<td>**lpszComment**</td>
<td>Ignored for queries.</td>
</tr>
<tr>
<td>**dwNameSpace**</td>
<td>Identifier of a single namespace in which to constrain the search, or **NS_ALL** to include all namespaces.</td>
</tr>
<tr>
<td>**lpNSProviderId**</td>
<td>Optional. References the GUID of a specific namespace provider and limits the query to this provider only.</td>
</tr>
<tr>
<td>**lpszContext**</td>
<td>Optional. Specifies the starting point of the query in a hierarchical namespace.</td>
</tr>
<tr>
<td>**dwNumberOfProtocols**</td>
<td>Size, in bytes, of the number of entries in the protocol constraint array, can be zero.</td>
</tr>
<tr>
<td>**lpafpProtocols**</td>
<td>Optional. A references to an array of 
<a href="/windows/desktop/api/winsock2/ns-winsock2-afprotocols">AFPROTOCOLS</a> structures. Only services that use these protocols will be returned. It is permissible for the value **AF_UNSPEC** to appear as a protocol family value, signifying a wildcard. Namespace providers may supply information about any service that uses the corresponding protocol, regardless of address family.</td>
</tr>
<tr>
<td>**lpszQueryString**</td>
<td>Optional. Some namespaces (such as whois++) support rich SQL-like queries contained in a simple text string. This parameter is used to specify that string.</td>
</tr>
<tr>
<td>**dwNumberOfCsAddrs**</td>
<td>Ignored for queries.</td>
</tr>
<tr>
<td>**lpcsaBuffer**</td>
<td>Ignored for queries.</td>
</tr>
<tr>
<td>**lpBlob**</td>
<td>Optional. A pointer to a provider-specific entity.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winsock2/ns-winsock2-afprotocols">AFPROTOCOLS</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupserviceend">NSPLookupServiceEnd</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicenext">NSPLookupServiceNext</a>



<a href="/windows/desktop/api/ws2spi/ns-ws2spi-nsp_routine">NSP_ROUTINE</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw">WSAQUERYSET</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaserviceclassinfow">WSASERVICECLASSINFO</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsasetlasterror">WSASetLastError</a>

