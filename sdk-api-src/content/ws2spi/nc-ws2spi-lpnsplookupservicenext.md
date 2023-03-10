---
UID: NC:ws2spi.LPNSPLOOKUPSERVICENEXT
title: LPNSPLOOKUPSERVICENEXT (ws2spi.h)
description: Called after obtaining a handle from a previous call to NSPLookupServiceBegin in order to retrieve the requested service information.
helpviewer_keywords: ["LPNSPLOOKUPSERVICENEXT","NSPLookupServiceNext","NSPLookupServiceNext function [Winsock]","_win32_nsplookupservicenext_2","winsock.nsplookupservicenext_2","ws2spi/NSPLookupServiceNext"]
old-location: winsock\nsplookupservicenext_2.htm
tech.root: WinSock
ms.assetid: 321732e4-5d48-48f4-8795-ffac208852dc
ms.date: 12/05/2018
ms.keywords: LPNSPLOOKUPSERVICENEXT, NSPLookupServiceNext, NSPLookupServiceNext function [Winsock], _win32_nsplookupservicenext_2, winsock.nsplookupservicenext_2, ws2spi/NSPLookupServiceNext
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
 - LPNSPLOOKUPSERVICENEXT
 - ws2spi/LPNSPLOOKUPSERVICENEXT
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
 - NSPLookupServiceNext
---

# LPNSPLOOKUPSERVICENEXT callback function


## -description

The 
**NSPLookupServiceNext** function is called after obtaining a handle from a previous call to 
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicebegin">NSPLookupServiceBegin</a> in order to retrieve the requested service information.

The provider will pass a 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw">WSAQUERYSET</a> structure in the <i>lpqsResults</i> buffer. The client should call this function until it returns **WSA_E_NOMORE**, indicating that all the 
**WSAQUERYSET** have been returned.

## -parameters

### -param hLookup [in]

A handle returned from the previous call to 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina">WSALookupServiceBegin</a>.

### -param dwControlFlags [in]

The flags used to control the next operation. Currently, only **LUP_FLUSHPREVIOUS** is defined as a means to handle a result set that is too large. If an application cannot supply a large enough buffer, setting **LUP_FLUSHPREVIOUS** instructs the provider to discard the last result set, which was too large, and move to the next set for this call.

### -param lpdwBufferLength [in, out]

The size, in bytes, on input, that is contained in the buffer pointed to by <i>lpqsResults</i>. On output, if the function fails and the error is WSAEFAULT, then it contains the minimum size, in bytes to pass for the <i>lpqsResults</i> to retrieve the record.

### -param lpqsResults [out]

A pointer to a memory block that will contain, on return, one result set in a 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw">WSAQUERYSET</a> structure.

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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_E_CANCELLED</a></b></dl>
</dl>
</td>
<td width="60%">
A call to 
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupserviceend">NSPLookupServiceEnd</a> was made while this call was still processing. The call has been canceled. The data in the <i>lpqsResults</i> buffer is undefined. 




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
</table>

## -remarks

The <i>dwControlFlags</i> specified in this function and the ones specified at the time of 
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicebegin">NSPLookupServiceBegin</a> are handled as "restrictions" for the purpose of combination. The restrictions are combined between the ones at 
**NSPLookupServiceBegin** time and the ones at 
**NSPLookupServiceNext** time. Therefore, the flags at 
**NSPLookupServiceNext** can never increase the amount of data returned beyond what was requested at 
**NSPLookupServiceBegin**, although it is not an error to specify more or less flags. The flags specified at a given 
**NSPLookupServiceNext** apply only to that call.

The <i>dwControlFlags</i> **LUP_FLUSHPREVIOUS** and **LUP_RES_SERVICE** are exceptions to the combined restrictions rule (because they are behavior flags instead of "restriction" flags). If either flag is used in 
**NSPLookupServiceNext**, they have their defined effect regardless of the setting of the same flags at 
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicebegin">NSPLookupServiceBegin</a>.

For example, if **LUP_RETURN_VERSION** is specified at 
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicebegin">NSPLookupServiceBegin</a>, the service provider retrieves records including the version. If **LUP_RETURN_VERSION** is not specified at 
**NSPLookupServiceNext**, the returned information does not include the version, even though it was available. No error is generated.

Also for example, if **LUP_RETURN_BLOB** is not specified at 
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicebegin">NSPLookupServiceBegin</a>, but is specified at 
**NSPLookupServiceNext**, the returned information does not include the private data. No error is generated.

<h3><a id="Query_Results"></a><a id="query_results"></a><a id="QUERY_RESULTS"></a>Query Results</h3>
The following table lists <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw">WSAQUERYSET</a> and describes how query results are represented in the 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw">WSAQUERYSET</a> structure. For more information, see <a href="/windows/desktop/WinSock/name-resolution-data-structures-2">Query-Related Data Structures</a>.

<table>
<tr>
<th>WSAQUERYSET member name</th>
<th>Result interpretation</th>
</tr>
<tr>
<td>**dwSize**</td>
<td>Will be set to sizeof(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw">WSAQUERYSET</a>). This is used as a versioning mechanism.</td>
</tr>
<tr>
<td>**dwOutputFlags**</td>
<td>**RESULT_IS_ALIAS** flag indicates this is an alias result.</td>
</tr>
<tr>
<td>**lpszServiceInstanceName**</td>
<td>References the string that contains the service name.</td>
</tr>
<tr>
<td>**lpServiceClassId**</td>
<td>GUID corresponding to the service class.</td>
</tr>
<tr>
<td>**lpVersion**</td>
<td>References version number of the particular service instance.</td>
</tr>
<tr>
<td>**lpszComment**</td>
<td>Optional. Comment string supplied by service instance.</td>
</tr>
<tr>
<td>**dwNameSpace**</td>
<td>Namespace in which the service instance was found.</td>
</tr>
<tr>
<td>**lpNSProviderId**</td>
<td>Identifies the specific namespace provider that supplied this query result.</td>
</tr>
<tr>
<td>**lpszContext**</td>
<td>Specifies the context point in a hierarchical namespace at which the service is located.</td>
</tr>
<tr>
<td>**dwNumberOfProtocols**</td>
<td>Undefined for results.</td>
</tr>
<tr>
<td>**lpafpProtocols**</td>
<td>Undefined for results, all needed protocol information is in the 
<a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info">CSADDR_INFO</a> structures.</td>
</tr>
<tr>
<td>**lpszQueryString**</td>
<td>When <i>dwControlFlags</i> includes **LUP_RETURN_QUERY_STRING**, this member returns the unparsed remainder of the **lpszServiceInstanceName** specified in the original query. For example, in a namespace that identifies services by hierarchical names that specify a host name and a file path within that host, the address returned might be the host address and the unparsed remainder might be the file path. If the **lpszServiceInstanceName** is fully parsed and **LUP_RETURN_QUERY_STRING** is used, this member is null or points to a zero-length string.</td>
</tr>
<tr>
<td>**dwNumberOfCsAddrs**</td>
<td>Indicates the number of elements in the array of 
<a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info">CSADDR_INFO</a> structures.</td>
</tr>
<tr>
<td>**lpcsaBuffer**</td>
<td>A pointer to an array of 
<a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info">CSADDR_INFO</a> structures, with one complete transport address contained within each element.</td>
</tr>
<tr>
<td>**lpBlob**</td>
<td>Optional. A pointer to a provider-specific entity.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info">CSADDR_INFO</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicebegin">NSPLookupServiceBegin</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupserviceend">NSPLookupServiceEnd</a>



<a href="/windows/desktop/api/ws2spi/ns-ws2spi-nsp_routine">NSP_ROUTINE</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw">WSAQUERYSET</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsasetlasterror">WSASetLastError</a>

