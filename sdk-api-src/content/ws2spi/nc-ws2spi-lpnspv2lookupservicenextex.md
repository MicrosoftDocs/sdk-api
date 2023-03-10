---
UID: NC:ws2spi.LPNSPV2LOOKUPSERVICENEXTEX
title: LPNSPV2LOOKUPSERVICENEXTEX (ws2spi.h)
description: Called after obtaining a handle from a previous call to NSPv2LookupServiceBegin in order to retrieve the requested information from a namespace version-2 service provider.
helpviewer_keywords: ["LPNSPV2LOOKUPSERVICENEXTEX","NSPv2LookupServiceNextEx","NSPv2LookupServiceNextEx function [Winsock]","winsock.nspv2lookupservicenextex","ws2spi/NSPv2LookupServiceNextEx"]
old-location: winsock\nspv2lookupservicenextex.htm
tech.root: WinSock
ms.assetid: 957fe544-9a3f-47f4-a98c-0624747650f4
ms.date: 12/05/2018
ms.keywords: LPNSPV2LOOKUPSERVICENEXTEX, NSPv2LookupServiceNextEx, NSPv2LookupServiceNextEx function [Winsock], winsock.nspv2lookupservicenextex, ws2spi/NSPv2LookupServiceNextEx
req.header: ws2spi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - LPNSPV2LOOKUPSERVICENEXTEX
 - ws2spi/LPNSPV2LOOKUPSERVICENEXTEX
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
 - NSPv2LookupServiceNextEx
---

# LPNSPV2LOOKUPSERVICENEXTEX callback function


## -description

The 
**NSPv2LookupServiceNextEx** function is called after obtaining a handle from a previous call to 
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicebegin">NSPv2LookupServiceBegin</a> in order to retrieve the requested information from a namespace version-2 service provider.

## -parameters

### -param hAsyncCall [in]

A handle returned from the previous call to 
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicebegin">NSPv2LookupServiceBegin</a> used for asynchronous calls.

### -param hLookup [in]

A handle returned from the previous call to 
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicebegin">NSPv2LookupServiceBegin</a>.

### -param dwControlFlags [in]

The flags used to control the next operation. Currently, only **LUP_FLUSHPREVIOUS** is defined as a means to handle a result set that is too large. If an application cannot supply a large enough buffer, setting **LUP_FLUSHPREVIOUS** instructs the provider to discard the last result set, which was too large, and move to the next set for this call.

### -param lpdwBufferLength [in, out]

The size, in bytes, on input, that is contained in the buffer pointed to by <i>lpqsResults</i>. On output, if the function fails and the error is WSAEFAULT, then it contains the minimum size, in bytes to pass for the <i>lpqsResults</i> to retrieve the record.

### -param lpqsResults [out]

A pointer to a memory block that will contain, on return, one result set in a 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaqueryset2w">WSAQUERYSET2</a> structure.

## -returns

The function should return **NO_ERROR** (zero) if the routine succeeds. It should return **SOCKET_ERROR** (that is, 1) if the routine fails and it must set the appropriate error code using 
<a href="/windows/desktop/api/winsock/nf-winsock-wsasetlasterror">WSASetLastError</a>.



<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_E_CANCELLED</a></b></dl>
</dl>
</td>
<td width="60%">
A call to 
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2lookupserviceend">NSPv2LookupServiceEnd</a> was made while this call was still processing. The call has been canceled. The data in the <i>lpqsResults</i> buffer is undefined. 




In Windows Sockets 2, conflicting error codes are defined for **WSAECANCELLED** (10103) and **WSA_E_CANCELLED** (10111).The error code **WSAECANCELLED** will be removed in a future version and only WSA_E_CANCELLED will remain. Namespace providers should use the **WSA_E_CANCELLED** error code to maintain compatibility with the widest possible range of applications.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_E_NO_MORE</a></b></dl>
</dl>
</td>
<td width="60%">
There is no more data available. 

In Windows Sockets 2, conflicting error codes are defined for **WSAENOMORE** (10102) and **WSA_E_NO_MORE** (10110).The error code **WSAENOMORE** will be removed in a future version and only WSA_E_NO_MORE will remain. Namespace providers should use the **WSA_E_NO_MORE** error code to maintain compatibility with the widest possible range of applications.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dl>
</dl>
</td>
<td width="60%">
The <i>lpqsResults</i> buffer was too small to contain a 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw">WSAQUERYSET</a> set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dl>
</dl>
</td>
<td width="60%">
One or more parameters are invalid, or missing, for this provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_INVALID_HANDLE</a></b></dl>
</dl>
</td>
<td width="60%">
The specified lookup handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANO_DATA</a></b></dl>
</dl>
</td>
<td width="60%">
The name was found in the database, but no data, matching the given restrictions, was located.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSASERVICE_NOT_FOUND</a></b></dl>
</dl>
</td>
<td width="60%">
The service is unknown. The service cannot be found in the specified namespace.

</td>
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
</table>

## -remarks

The 
**NSPv2LookupServiceNextEx** function is used as part of the namespace service provider version-2 (NSPv2) architecture available on Windows Vista and later. 

On Windows Vista and Windows Server 2008, the **NSPv2LookupServiceNextEx** function can only be used for operations on NS_EMAIL namespace providers.

The provider will pass a 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaqueryset2w">WSAQUERYSET2</a> structure in the <i>lpqsResults</i> buffer. The client should call the **NSPv2LookupServiceNextEx** function until it returns **WSA_E_NOMORE**, indicating that all the 
**WSAQUERYSET2** structures have been returned.

The <i>dwControlFlags</i> specified in this function and the ones specified at the time of 
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicebegin">NSPv2LookupServiceBegin</a> are handled as "restrictions" for the purpose of combination. The restrictions are combined between the ones at 
**NSPv2LookupServiceBegin** time and the ones at 
**NSPv2LookupServiceNextEx** time. Therefore, the flags at 
**NSPv2LookupServiceNextEx** can never increase the amount of data returned beyond what was requested at 
**NSPv2LookupServiceBegin**, although it is not an error to specify more or less flags. The flags specified at a given 
**NSPv2LookupServiceNextEx** apply only to that call.

The <i>dwControlFlags</i> **LUP_FLUSHPREVIOUS** and **LUP_RES_SERVICE** are exceptions to the combined restrictions rule (because they are behavior flags instead of "restriction" flags). If either flag is used in 
**NSPv2LookupServiceNextEx**, they have their defined effect regardless of the setting of the same flags at 
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicebegin">NSPv2LookupServiceBegin</a>.

For example, if **LUP_RETURN_VERSION** is specified at 
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicebegin">NSPv2LookupServiceBegin</a>, the service provider retrieves records including the version. If **LUP_RETURN_VERSION** is not specified at 
**NSPv2LookupServiceNextEx**, the returned information does not include the version, even though it was available. No error is generated.

Also for example, if **LUP_RETURN_BLOB** is not specified at 
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicebegin">NSPv2LookupServiceBegin</a>, but is specified at 
**NSPv2LookupServiceNextEx**, the returned information does not include the private data. No error is generated.

The **NSPv2LookupServiceNextEx** function is typically called at least twice. The first time to get the size of the needed buffer to receive the <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaqueryset2w">WSAQUERYSET2</a> pointed to by the <i>lpqsResults</i> parameter, and the second time to get the actual query result set. On the first call, the NSPv2 provider should return the size necessary for the **WSAQUERYSET2** results.  



The <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaqueryset2w">WSAQUERYSET2</a> structure pointed to by the <i>lpqsResults</i> parameter that is returned is only useful in the same process context, since several of the members in the **WSAQUERYSET2** structure contains pointers to the actual data returned. If the query result needs to be passed to another process (using RPC, for example), then it will be necessary to serialize and marshal the data returned in the **WSAQUERYSET2** structure pointed to by the <i>lpqsResults</i> parameter including the data pointed to by members in the **WSAQUERYSET2** structure. The data needs to be serialized in a form that can be passed across process boundaries. Just passing a copy of the **WSAQUERYSET2** structure  is insufficient, since only pointers to data will be passed and the actual data will be unavailable to other processes.

<h3><a id="Query_Results"></a><a id="query_results"></a><a id="QUERY_RESULTS"></a>Query Results</h3>
The following table lists <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaqueryset2w">WSAQUERYSET2</a> and describes how query results are represented in the 
**WSAQUERYSET2** structure. For more information, see <a href="/windows/desktop/WinSock/name-resolution-data-structures-2">Query-Related Data Structures</a>.

<table>
<tr>
<th>WSAQUERYSET2 member name</th>
<th>Result interpretation</th>
</tr>
<tr>
<td>**dwSize**</td>
<td>The  size, in bytes, of <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaqueryset2w">WSAQUERYSET2</a> structure. This is used as a versioning mechanism.</td>
</tr>
<tr>
<td>**lpszServiceInstanceName**</td>
<td>A string that contains the service name.</td>
</tr>
<tr>
<td>**lpVersion**</td>
<td>References version number of the particular service instance.</td>
</tr>
<tr>
<td>**lpszComment**</td>
<td>A comment string supplied by service instance. This member is optional, dependent on the requirements of the NSPv2 service provider.

</td>
</tr>
<tr>
<td>**dwNameSpace**</td>
<td>The namespace identifier in which the name or service instance was found.</td>
</tr>
<tr>
<td>**lpNSProviderId**</td>
<td>The specific namespace provider that supplied this query result.</td>
</tr>
<tr>
<td>**lpszContext**</td>
<td>The context point in a hierarchical namespace at which the service is located.</td>
</tr>
<tr>
<td>**dwNumberOfProtocols**</td>
<td>This member is undefined for results.</td>
</tr>
<tr>
<td>**lpafpProtocols**</td>
<td>This member is undefined for results. All needed protocol information is in the 
<a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info">CSADDR_INFO</a> structures.</td>
</tr>
<tr>
<td>**lpszQueryString**</td>
<td>When <i>dwControlFlags</i> includes **LUP_RETURN_QUERY_STRING**, this member returns the unparsed remainder of the **lpszServiceInstanceName** specified in the original query. For example, in a namespace that identifies services by hierarchical names that specify a host name and a file path within that host, the address returned might be the host address and the unparsed remainder might be the file path. If the **lpszServiceInstanceName** is fully parsed and **LUP_RETURN_QUERY_STRING** is used, this member is null or points to a zero-length string.</td>
</tr>
<tr>
<td>**dwNumberOfCsAddrs**</td>
<td>The number of elements in the array of 
<a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info">CSADDR_INFO</a> structures.</td>
</tr>
<tr>
<td>**lpcsaBuffer**</td>
<td>A pointer to an array of 
<a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info">CSADDR_INFO</a> structures, with one complete transport address contained within each element.</td>
</tr>
<tr>
<td>**dwOutputFlags**</td>
<td>The **RESULT_IS_ALIAS** flag indicates this is an alias result.</td>
</tr>
<tr>
<td>**lpBlob**</td>
<td>A pointer to a provider-specific entity. This member is optional, dependent on the requirements of the NSPv2 service provider.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info">CSADDR_INFO</a>



<a href="/windows/desktop/api/ws2spi/ns-ws2spi-nspv2_routine">NSPV2_ROUTINE</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2cleanup">NSPv2Cleanup</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2clientsessionrundown">NSPv2ClientSessionRundown</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicebegin">NSPv2LookupServiceBegin</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2lookupserviceend">NSPv2LookupServiceEnd</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2setserviceex">NSPv2SetServiceEx</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2startup">NSPv2Startup</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaqueryset2w">WSAQUERYSET2</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsasetlasterror">WSASetLastError</a>

