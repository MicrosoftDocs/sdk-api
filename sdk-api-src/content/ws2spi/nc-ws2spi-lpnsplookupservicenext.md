---
UID: NC:ws2spi.LPNSPLOOKUPSERVICENEXT
title: LPNSPLOOKUPSERVICENEXT
author: windows-sdk-content
description: Called after obtaining a handle from a previous call to NSPLookupServiceBegin in order to retrieve the requested service information.
old-location: winsock\nsplookupservicenext_2.htm
old-project: winsock
ms.assetid: 321732e4-5d48-48f4-8795-ffac208852dc
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: LPNSPLOOKUPSERVICENEXT, NSPLookupServiceNext, NSPLookupServiceNext function [Winsock], _win32_nsplookupservicenext_2, winsock.nsplookupservicenext_2, ws2spi/NSPLookupServiceNext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
tech.root: 
req.typenames: SOCKADDR_INET, *PSOCKADDR_INET
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ws2spi.h
api_name:
 - NSPLookupServiceNext
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# LPNSPLOOKUPSERVICENEXT callback function


## -description


The 
<b>NSPLookupServiceNext</b> function is called after obtaining a handle from a previous call to 
<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPLookupServiceBegin</a> in order to retrieve the requested service information.

The provider will pass a 
<a href="https://msdn.microsoft.com/6c81fbba-aaf4-49ca-ab79-b6fe5dfb0076">WSAQUERYSET</a> structure in the <i>lpqsResults</i> buffer. The client should call this function until it returns <b>WSA_E_NOMORE</b>, indicating that all the 
<b>WSAQUERYSET</b> have been returned.


## -parameters




### -param hLookup [in]

A handle returned from the previous call to 
<a href="https://msdn.microsoft.com/448309ef-b9dd-4960-8016-d26691df59ec">WSALookupServiceBegin</a>.


### -param dwControlFlags [in]

The flags used to control the next operation. Currently, only <b>LUP_FLUSHPREVIOUS</b> is defined as a means to handle a result set that is too large. If an application cannot supply a large enough buffer, setting <b>LUP_FLUSHPREVIOUS</b> instructs the provider to discard the last result set, which was too large, and move to the next set for this call.


### -param lpdwBufferLength [in, out]

The size, in bytes, on input, that is contained in the buffer pointed to by <i>lpqsResults</i>. On output, if the function fails and the error is WSAEFAULT, then it contains the minimum size, in bytes to pass for the <i>lpqsResults</i> to retrieve the record.


### -param lpqsResults [out]

A pointer to a memory block that will contain, on return, one result set in a 
<a href="https://msdn.microsoft.com/6c81fbba-aaf4-49ca-ab79-b6fe5dfb0076">WSAQUERYSET</a> structure.


## -returns



The function should return <b>NO_ERROR</b> (zero) if the routine succeeds. It should return <b>SOCKET_ERROR</b> (–1) if the routine fails and it must set the appropriate error code using 
<a href="https://msdn.microsoft.com/596155ee-3dcc-4ae3-97ab-0653e019cbee">WSASetLastError</a>.



<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSA_E_CANCELLED</a></b></dt>
</dl>
</td>
<td width="60%">
A call to 
<a href="https://msdn.microsoft.com/ec72c89a-a74b-449c-996a-02057dff9137">NSPLookupServiceEnd</a> was made while this call was still processing. The call has been canceled. The data in the <i>lpqsResults</i> buffer is undefined. 




In Windows Sockets 2, conflicting error codes are defined for <b>WSAECANCELLED</b> (10103) and <b>WSA_E_CANCELLED</b> (10111).The error code <b>WSAECANCELLED</b> will be removed in a future version and only WSA_E_CANCELLED will remain. Namespace providers should use the <b>WSA_E_CANCELLED</b> error code to maintain compatibility with the widest possible range of applications.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSA_E_NO_MORE</a></b></dt>
</dl>
</td>
<td width="60%">
There is no more data available. 

In Windows Sockets 2, conflicting error codes are defined for <b>WSAENOMORE</b> (10102) and <b>WSA_E_NO_MORE</b> (10110).The error code <b>WSAENOMORE</b> will be removed in a future version and only WSA_E_NO_MORE will remain. Namespace providers should use the <b>WSA_E_NO_MORE</b> error code to maintain compatibility with the widest possible range of applications.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSA_INVALID_HANDLE</a></b></dt>
</dl>
</td>
<td width="60%">
The specified lookup handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory available to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>lpqsResults</i> buffer was too small to contain a 
<a href="https://msdn.microsoft.com/6c81fbba-aaf4-49ca-ab79-b6fe5dfb0076">WSAQUERYSET</a> set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid, or missing, for this provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEOPNOTSUPP</a></b></dt>
</dl>
</td>
<td width="60%">
The operation is not supported. This error is returned if the namespace provider does not implement this function. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSANO_DATA</a></b></dt>
</dl>
</td>
<td width="60%">
The name was found in the database, but no data, matching the given restrictions, was located.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSASERVICE_NOT_FOUND</a></b></dt>
</dl>
</td>
<td width="60%">
The service is unknown. The service cannot be found in the specified namespace.

</td>
</tr>
</table>
 




## -remarks



The <i>dwControlFlags</i> specified in this function and the ones specified at the time of 
<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPLookupServiceBegin</a> are handled as "restrictions" for the purpose of combination. The restrictions are combined between the ones at 
<b>NSPLookupServiceBegin</b> time and the ones at 
<b>NSPLookupServiceNext</b> time. Therefore, the flags at 
<b>NSPLookupServiceNext</b> can never increase the amount of data returned beyond what was requested at 
<b>NSPLookupServiceBegin</b>, although it is not an error to specify more or less flags. The flags specified at a given 
<b>NSPLookupServiceNext</b> apply only to that call.

The <i>dwControlFlags</i> <b>LUP_FLUSHPREVIOUS</b> and <b>LUP_RES_SERVICE</b> are exceptions to the combined restrictions rule (because they are behavior flags instead of "restriction" flags). If either flag is used in 
<b>NSPLookupServiceNext</b>, they have their defined effect regardless of the setting of the same flags at 
<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPLookupServiceBegin</a>.

For example, if <b>LUP_RETURN_VERSION</b> is specified at 
<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPLookupServiceBegin</a>, the service provider retrieves records including the version. If <b>LUP_RETURN_VERSION</b> is not specified at 
<b>NSPLookupServiceNext</b>, the returned information does not include the version, even though it was available. No error is generated.

Also for example, if <b>LUP_RETURN_BLOB</b> is not specified at 
<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPLookupServiceBegin</a>, but is specified at 
<b>NSPLookupServiceNext</b>, the returned information does not include the private data. No error is generated.

<h3><a id="Query_Results"></a><a id="query_results"></a><a id="QUERY_RESULTS"></a>Query Results</h3>
The following table lists <a href="https://msdn.microsoft.com/6c81fbba-aaf4-49ca-ab79-b6fe5dfb0076">WSAQUERYSET</a> and describes how query results are represented in the 
<a href="https://msdn.microsoft.com/6c81fbba-aaf4-49ca-ab79-b6fe5dfb0076">WSAQUERYSET</a> structure. For more information, see <a href="name_resolution_data_structures_2.htm">Query-Related Data Structures</a>.

<table>
<tr>
<th>WSAQUERYSET member name</th>
<th>Result interpretation</th>
</tr>
<tr>
<td><b>dwSize</b></td>
<td>Will be set to sizeof(<a href="https://msdn.microsoft.com/6c81fbba-aaf4-49ca-ab79-b6fe5dfb0076">WSAQUERYSET</a>). This is used as a versioning mechanism.</td>
</tr>
<tr>
<td><b>dwOutputFlags</b></td>
<td><b>RESULT_IS_ALIAS</b> flag indicates this is an alias result.</td>
</tr>
<tr>
<td><b>lpszServiceInstanceName</b></td>
<td>References the string that contains the service name.</td>
</tr>
<tr>
<td><b>lpServiceClassId</b></td>
<td>GUID corresponding to the service class.</td>
</tr>
<tr>
<td><b>lpVersion</b></td>
<td>References version number of the particular service instance.</td>
</tr>
<tr>
<td><b>lpszComment</b></td>
<td>Optional. Comment string supplied by service instance.</td>
</tr>
<tr>
<td><b>dwNameSpace</b></td>
<td>Namespace in which the service instance was found.</td>
</tr>
<tr>
<td><b>lpNSProviderId</b></td>
<td>Identifies the specific namespace provider that supplied this query result.</td>
</tr>
<tr>
<td><b>lpszContext</b></td>
<td>Specifies the context point in a hierarchical namespace at which the service is located.</td>
</tr>
<tr>
<td><b>dwNumberOfProtocols</b></td>
<td>Undefined for results.</td>
</tr>
<tr>
<td><b>lpafpProtocols</b></td>
<td>Undefined for results, all needed protocol information is in the 
<a href="https://msdn.microsoft.com/9cad3586-e315-4f6f-9045-7c95502bb768">CSADDR_INFO</a> structures.</td>
</tr>
<tr>
<td><b>lpszQueryString</b></td>
<td>When <i>dwControlFlags</i> includes <b>LUP_RETURN_QUERY_STRING</b>, this member returns the unparsed remainder of the <b>lpszServiceInstanceName</b> specified in the original query. For example, in a namespace that identifies services by hierarchical names that specify a host name and a file path within that host, the address returned might be the host address and the unparsed remainder might be the file path. If the <b>lpszServiceInstanceName</b> is fully parsed and <b>LUP_RETURN_QUERY_STRING</b> is used, this member is null or points to a zero-length string.</td>
</tr>
<tr>
<td><b>dwNumberOfCsAddrs</b></td>
<td>Indicates the number of elements in the array of 
<a href="https://msdn.microsoft.com/9cad3586-e315-4f6f-9045-7c95502bb768">CSADDR_INFO</a> structures.</td>
</tr>
<tr>
<td><b>lpcsaBuffer</b></td>
<td>A pointer to an array of 
<a href="https://msdn.microsoft.com/9cad3586-e315-4f6f-9045-7c95502bb768">CSADDR_INFO</a> structures, with one complete transport address contained within each element.</td>
</tr>
<tr>
<td><b>lpBlob</b></td>
<td>Optional. A pointer to a provider-specific entity.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9cad3586-e315-4f6f-9045-7c95502bb768">CSADDR_INFO</a>



<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPLookupServiceBegin</a>



<a href="https://msdn.microsoft.com/ec72c89a-a74b-449c-996a-02057dff9137">NSPLookupServiceEnd</a>



<a href="https://msdn.microsoft.com/8f7736d5-ea77-472a-a94f-e422398fae3f">NSP_ROUTINE</a>



<a href="https://msdn.microsoft.com/6c81fbba-aaf4-49ca-ab79-b6fe5dfb0076">WSAQUERYSET</a>



<a href="https://msdn.microsoft.com/596155ee-3dcc-4ae3-97ab-0653e019cbee">WSASetLastError</a>
 

 

