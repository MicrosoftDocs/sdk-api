---
UID: NC:ws2spi.LPNSPV2LOOKUPSERVICENEXTEX
title: LPNSPV2LOOKUPSERVICENEXTEX
author: windows-driver-content
description: Called after obtaining a handle from a previous call to NSPv2LookupServiceBegin in order to retrieve the requested information from a namespace version-2 service provider.
old-location: winsock\nspv2lookupservicenextex.htm
old-project: WinSock
ms.assetid: 957fe544-9a3f-47f4-a98c-0624747650f4
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: LPNSPV2LOOKUPSERVICENEXTEX, NSPv2LookupServiceNextEx, NSPv2LookupServiceNextEx function [Winsock], winsock.nspv2lookupservicenextex, ws2spi/NSPv2LookupServiceNextEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
req.typenames: SOCKADDR_INET, *PSOCKADDR_INET
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Ws2spi.h
api_name:
-	NSPv2LookupServiceNextEx
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# LPNSPV2LOOKUPSERVICENEXTEX callback


## -description


The 
<b>NSPv2LookupServiceNextEx</b> function is called after obtaining a handle from a previous call to 
<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPv2LookupServiceBegin</a> in order to retrieve the requested information from a namespace version-2 service provider.


## -parameters




### -param hAsyncCall [in]

A handle returned from the previous call to 
<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPv2LookupServiceBegin</a> used for asynchronous calls.


### -param hLookup [in]

A handle returned from the previous call to 
<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPv2LookupServiceBegin</a>.


### -param dwControlFlags [in]

The flags used to control the next operation. Currently, only <b>LUP_FLUSHPREVIOUS</b> is defined as a means to handle a result set that is too large. If an application cannot supply a large enough buffer, setting <b>LUP_FLUSHPREVIOUS</b> instructs the provider to discard the last result set, which was too large, and move to the next set for this call.


### -param lpdwBufferLength [in, out]

The size, in bytes, on input, that is contained in the buffer pointed to by <i>lpqsResults</i>. On output, if the function fails and the error is WSAEFAULT, then it contains the minimum size, in bytes to pass for the <i>lpqsResults</i> to retrieve the record.


### -param lpqsResults [out]

A pointer to a memory block that will contain, on return, one result set in a 
<a href="https://msdn.microsoft.com/ffe71de0-3561-481f-b81f-835c6c3a3ee4">WSAQUERYSET2</a> structure.


## -returns




						The function should return <b>NO_ERROR</b> (zero) if the routine succeeds. It should return <b>SOCKET_ERROR</b> (â€“1) if the routine fails and it must set the appropriate error code using 
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
<a href="https://msdn.microsoft.com/5f2b56c5-3a8e-4bf9-8f28-d2a06543227b">NSPv2LookupServiceEnd</a> was made while this call was still processing. The call has been canceled. The data in the <i>lpqsResults</i> buffer is undefined. 




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
</table>
 




## -remarks



The 
<b>NSPv2LookupServiceNextEx</b> function is used as part of the namespace service provider version-2 (NSPv2) architecture available on Windows Vista and later. 

On Windows Vista and Windows Server 2008, the <b>NSPv2LookupServiceNextEx</b> function can only be used for operations on NS_EMAIL namespace providers.

The provider will pass a 
<a href="https://msdn.microsoft.com/ffe71de0-3561-481f-b81f-835c6c3a3ee4">WSAQUERYSET2</a> structure in the <i>lpqsResults</i> buffer. The client should call the <b>NSPv2LookupServiceNextEx</b> function until it returns <b>WSA_E_NOMORE</b>, indicating that all the 
<b>WSAQUERYSET2</b> structures have been returned.

The <i>dwControlFlags</i> specified in this function and the ones specified at the time of 
<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPv2LookupServiceBegin</a> are handled as "restrictions" for the purpose of combination. The restrictions are combined between the ones at 
<b>NSPv2LookupServiceBegin</b> time and the ones at 
<b>NSPv2LookupServiceNextEx</b> time. Therefore, the flags at 
<b>NSPv2LookupServiceNextEx</b> can never increase the amount of data returned beyond what was requested at 
<b>NSPv2LookupServiceBegin</b>, although it is not an error to specify more or less flags. The flags specified at a given 
<b>NSPv2LookupServiceNextEx</b> apply only to that call.

The <i>dwControlFlags</i> <b>LUP_FLUSHPREVIOUS</b> and <b>LUP_RES_SERVICE</b> are exceptions to the combined restrictions rule (because they are behavior flags instead of "restriction" flags). If either flag is used in 
<b>NSPv2LookupServiceNextEx</b>, they have their defined effect regardless of the setting of the same flags at 
<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPv2LookupServiceBegin</a>.

For example, if <b>LUP_RETURN_VERSION</b> is specified at 
<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPv2LookupServiceBegin</a>, the service provider retrieves records including the version. If <b>LUP_RETURN_VERSION</b> is not specified at 
<b>NSPv2LookupServiceNextEx</b>, the returned information does not include the version, even though it was available. No error is generated.

Also for example, if <b>LUP_RETURN_BLOB</b> is not specified at 
<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPv2LookupServiceBegin</a>, but is specified at 
<b>NSPv2LookupServiceNextEx</b>, the returned information does not include the private data. No error is generated.

The <b>NSPv2LookupServiceNextEx</b> function is typically called at least twice. The first time to get the size of the needed buffer to receive the <a href="https://msdn.microsoft.com/ffe71de0-3561-481f-b81f-835c6c3a3ee4">WSAQUERYSET2</a> pointed to by the <i>lpqsResults</i> parameter, and the second time to get the actual query result set. On the first call, the NSPv2 provider should return the size necessary for the <b>WSAQUERYSET2</b> results.  



The <a href="https://msdn.microsoft.com/ffe71de0-3561-481f-b81f-835c6c3a3ee4">WSAQUERYSET2</a> structure pointed to by the <i>lpqsResults</i> parameter that is returned is only useful in the same process context, since several of the members in the <b>WSAQUERYSET2</b> structure contains pointers to the actual data returned. If the query result needs to be passed to another process (using RPC, for example), then it will be necessary to serialize and marshal the data returned in the <b>WSAQUERYSET2</b> structure pointed to by the <i>lpqsResults</i> parameter including the data pointed to by members in the <b>WSAQUERYSET2</b> structure. The data needs to be serialized in a form that can be passed across process boundaries. Just passing a copy of the <b>WSAQUERYSET2</b> structure  is insufficient, since only pointers to data will be passed and the actual data will be unavailable to other processes.

<h3><a id="Query_Results"></a><a id="query_results"></a><a id="QUERY_RESULTS"></a>Query Results</h3>
The following table lists <a href="https://msdn.microsoft.com/ffe71de0-3561-481f-b81f-835c6c3a3ee4">WSAQUERYSET2</a> and describes how query results are represented in the 
<b>WSAQUERYSET2</b> structure. For more information, see <a href="name_resolution_data_structures_2.htm">Query-Related Data Structures</a>.

<table>
<tr>
<th>WSAQUERYSET2 member name</th>
<th>Result interpretation</th>
</tr>
<tr>
<td><b>dwSize</b></td>
<td>The  size, in bytes, of <a href="https://msdn.microsoft.com/ffe71de0-3561-481f-b81f-835c6c3a3ee4">WSAQUERYSET2</a> structure. This is used as a versioning mechanism.</td>
</tr>
<tr>
<td><b>lpszServiceInstanceName</b></td>
<td>A string that contains the service name.</td>
</tr>
<tr>
<td><b>lpVersion</b></td>
<td>References version number of the particular service instance.</td>
</tr>
<tr>
<td><b>lpszComment</b></td>
<td>A comment string supplied by service instance. This member is optional, dependent on the requirements of the NSPv2 service provider.

</td>
</tr>
<tr>
<td><b>dwNameSpace</b></td>
<td>The namespace identifier in which the name or service instance was found.</td>
</tr>
<tr>
<td><b>lpNSProviderId</b></td>
<td>The specific namespace provider that supplied this query result.</td>
</tr>
<tr>
<td><b>lpszContext</b></td>
<td>The context point in a hierarchical namespace at which the service is located.</td>
</tr>
<tr>
<td><b>dwNumberOfProtocols</b></td>
<td>This member is undefined for results.</td>
</tr>
<tr>
<td><b>lpafpProtocols</b></td>
<td>This member is undefined for results. All needed protocol information is in the 
<a href="https://msdn.microsoft.com/9cad3586-e315-4f6f-9045-7c95502bb768">CSADDR_INFO</a> structures.</td>
</tr>
<tr>
<td><b>lpszQueryString</b></td>
<td>When <i>dwControlFlags</i> includes <b>LUP_RETURN_QUERY_STRING</b>, this member returns the unparsed remainder of the <b>lpszServiceInstanceName</b> specified in the original query. For example, in a namespace that identifies services by hierarchical names that specify a host name and a file path within that host, the address returned might be the host address and the unparsed remainder might be the file path. If the <b>lpszServiceInstanceName</b> is fully parsed and <b>LUP_RETURN_QUERY_STRING</b> is used, this member is null or points to a zero-length string.</td>
</tr>
<tr>
<td><b>dwNumberOfCsAddrs</b></td>
<td>The number of elements in the array of 
<a href="https://msdn.microsoft.com/9cad3586-e315-4f6f-9045-7c95502bb768">CSADDR_INFO</a> structures.</td>
</tr>
<tr>
<td><b>lpcsaBuffer</b></td>
<td>A pointer to an array of 
<a href="https://msdn.microsoft.com/9cad3586-e315-4f6f-9045-7c95502bb768">CSADDR_INFO</a> structures, with one complete transport address contained within each element.</td>
</tr>
<tr>
<td><b>dwOutputFlags</b></td>
<td>The <b>RESULT_IS_ALIAS</b> flag indicates this is an alias result.</td>
</tr>
<tr>
<td><b>lpBlob</b></td>
<td>A pointer to a provider-specific entity. This member is optional, dependent on the requirements of the NSPv2 service provider.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9cad3586-e315-4f6f-9045-7c95502bb768">CSADDR_INFO</a>



<a href="https://msdn.microsoft.com/22a4ee47-030b-4aee-b9b1-c9e33b3e4fce">NSPV2_ROUTINE</a>



<a href="https://msdn.microsoft.com/36064c0e-c83c-4819-a3e4-c89df50eb659">NSPv2Cleanup</a>



<a href="https://msdn.microsoft.com/7379b502-129a-4dac-b7eb-e6fae8fb23f8">NSPv2ClientSessionRundown</a>



<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPv2LookupServiceBegin</a>



<a href="https://msdn.microsoft.com/5f2b56c5-3a8e-4bf9-8f28-d2a06543227b">NSPv2LookupServiceEnd</a>



<a href="https://msdn.microsoft.com/596fe0bd-ec11-44f3-bffe-333758171ea6">NSPv2SetServiceEx</a>



<a href="https://msdn.microsoft.com/93224e66-9c94-4b5c-af11-ae988b74bc03">NSPv2Startup</a>



<a href="https://msdn.microsoft.com/ffe71de0-3561-481f-b81f-835c6c3a3ee4">WSAQUERYSET2</a>



<a href="https://msdn.microsoft.com/596155ee-3dcc-4ae3-97ab-0653e019cbee">WSASetLastError</a>
 

 

