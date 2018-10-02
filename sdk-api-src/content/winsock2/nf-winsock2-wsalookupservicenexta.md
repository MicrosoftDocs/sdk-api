---
UID: NF:winsock2.WSALookupServiceNextA
title: WSALookupServiceNextA function
author: windows-sdk-content
description: The WSALookupServiceNext function is called after obtaining a handle from a previous call to WSALookupServiceBegin in order to retrieve the requested service information.
old-location: winsock\wsalookupservicenext_2.htm
tech.root: WinSock
ms.assetid: ab4f1830-b38d-4224-a6a9-6d4512245ad6
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: LUP_CONTAINERS, LUP_DEEP, LUP_FLUSHCACHE, LUP_FLUSHPREVIOUS, LUP_NEAREST, LUP_NOCONTAINERS, LUP_RES_SERVICE, LUP_RETURN_ADDR, LUP_RETURN_ALIASES, LUP_RETURN_ALL, LUP_RETURN_BLOB, LUP_RETURN_COMMENT, LUP_RETURN_NAME, LUP_RETURN_QUERY_STRING, LUP_RETURN_TYPE, LUP_RETURN_VERSION, WSALookupServiceNext, WSALookupServiceNext function [Winsock], WSALookupServiceNextA, WSALookupServiceNextW, _win32_wsalookupservicenext_2, winsock.wsalookupservicenext_2, winsock2/WSALookupServiceNext, winsock2/WSALookupServiceNextA, winsock2/WSALookupServiceNextW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winsock2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WSALookupServiceNextW (Unicode) and WSALookupServiceNextA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - WSALookupServiceNext
 - WSALookupServiceNextA
 - WSALookupServiceNextW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WSALookupServiceNextA function


## -description


The 
<b>WSALookupServiceNext</b> function is called after obtaining a handle from a previous call to 
<a href="https://msdn.microsoft.com/448309ef-b9dd-4960-8016-d26691df59ec">WSALookupServiceBegin</a> in order to retrieve the requested service information.

The provider will pass back a 
<a href="https://msdn.microsoft.com/6c81fbba-aaf4-49ca-ab79-b6fe5dfb0076">WSAQUERYSET</a> structure in the <i>lpqsResults</i> buffer. The client should continue to call this function until it returns WSA_E_NO_MORE, indicating that all of 
<b>WSAQUERYSET</b> has been returned.


## -parameters




### -param hLookup [in]

A handle returned from the previous call to 
<a href="https://msdn.microsoft.com/448309ef-b9dd-4960-8016-d26691df59ec">WSALookupServiceBegin</a>.


### -param dwControlFlags [in]

A set of flags that controls the operation. The values passed in the <i>dwControlFlags</i> parameter to the <a href="https://msdn.microsoft.com/448309ef-b9dd-4960-8016-d26691df59ec">WSALookupServiceBegin</a>function determine the possible criteria. Any values passed in the <i>dwControlFlags</i> parameter to the <b>WSALookupServiceNext</b> function further restrict the criteria for the service lookup. 

Currently, LUP_FLUSHPREVIOUS is defined as a means to cope with a result set that is too large. If an application does not (or cannot) supply a large enough buffer, setting LUP_FLUSHPREVIOUS instructs the provider to discard the last result set—which was too large—and move on to the next set for this call.

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
<b>WSALookupServiceNext</b>, and each alias returned will have the RESULT_IS_ALIAS flag set.

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
<b>WSALookupServiceNext</b>. Setting this flag instructs the provider to discard the last result set, which was too large for the specified buffer, and move on to the next result set.

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
<a href="https://msdn.microsoft.com/9cad3586-e315-4f6f-9045-7c95502bb768">CSADDR_INFO</a> structure. The other part needs to be usable in either case.

</td>
</tr>
</table>
 


### -param lpdwBufferLength [in, out]

On input, the number of bytes contained in the buffer pointed to by <i>lpqsResults</i>. On output, if the function fails and the error is 
<a href="windows_sockets_error_codes_2.htm">WSAEFAULT</a>, then it contains the minimum number of bytes to pass for the <i>lpqsResults</i> to retrieve the record.


### -param lpqsResults [out]

A pointer to a block of memory, which will contain one result set in a 
<a href="https://msdn.microsoft.com/6c81fbba-aaf4-49ca-ab79-b6fe5dfb0076">WSAQUERYSET</a> structure on return.


## -returns



The return value is zero if the operation was successful. Otherwise, the value SOCKET_ERROR is returned, and a specific error number can be retrieved by calling 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>.

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
<a href="https://msdn.microsoft.com/f9d2ac54-a818-464d-918e-80ebb5b1b106">WSALookupServiceEnd</a> was made while this call was still processing. The call has been canceled. The data in the <i>lpqsResults</i> buffer is undefined. In Windows Sockets version 2, conflicting error codes are defined for <a href="windows_sockets_error_codes_2.htm">WSAECANCELLED</a> (10103) and <a href="windows_sockets_error_codes_2.htm">WSA_E_CANCELLED</a> (10111). The error code WSAECANCELLED will be removed in a future version and only WSA_E_CANCELLED will remain. For Windows Sockets version 2, however, applications should check for both WSAECANCELLED and WSA_E_CANCELLED for the widest possible compatibility with namespace providers that use either one.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSA_E_NO_MORE</a></b></dt>
</dl>
</td>
<td width="60%">
There is no more data available. In Windows Sockets version 2, conflicting error codes are defined for <a href="windows_sockets_error_codes_2.htm">WSAENOMORE</a> (10102) and <a href="windows_sockets_error_codes_2.htm">WSA_E_NO_MORE</a> (10110). The error code WSAENOMORE will be removed in a future version and only WSA_E_NO_MORE will remain. For Windows Sockets version 2, however, applications should check for both WSAENOMORE and WSA_E_NO_MORE for the widest possible compatibility with name-space providers that use either one.

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
One or more required parameters were invalid or missing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSA_INVALID_HANDLE</a></b></dt>
</dl>
</td>
<td width="60%">
The specified Lookup handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
The WS2_32.DLL has not been initialized. The application must first call 
<a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a> before calling any Windows Sockets functions.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSANO_DATA</a></b></dt>
</dl>
</td>
<td width="60%">
The name was found in the database, but no data matching the given restrictions was located.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory to perform the operation.

</td>
</tr>
</table>
 




## -remarks



The <i>dwControlFlags</i> parameter specified in this function and the ones specified at the time of 
<a href="https://msdn.microsoft.com/448309ef-b9dd-4960-8016-d26691df59ec">WSALookupServiceBegin</a> are treated as restrictions for the purpose of combination. The restrictions are combined between the ones at 
<b>WSALookupServiceBegin</b> time and the ones at 
<b>WSALookupServiceNext</b> time. Therefore the flags at 
<b>WSALookupServiceNext</b> can never increase the amount of data returned beyond what was requested at 
<b>WSALookupServiceBegin</b>, although it is not an error to specify more or fewer flags. The flags specified at a given 
<b>WSALookupServiceNext</b> apply only to that call.

The <i>dwControlFlags</i> LUP_FLUSHPREVIOUS and LUP_RES_SERVICE are exceptions to the combined restrictions rule (because they are behavior flags instead of restriction flags). If either of these flags are used in 
<b>WSALookupServiceNext</b> they have their defined effect regardless of the setting of the same flags at 
<a href="https://msdn.microsoft.com/448309ef-b9dd-4960-8016-d26691df59ec">WSALookupServiceBegin</a>.

For example, if LUP_RETURN_VERSION is specified at 
<a href="https://msdn.microsoft.com/448309ef-b9dd-4960-8016-d26691df59ec">WSALookupServiceBegin</a> the service provider retrieves records including the version. If LUP_RETURN_VERSION is NOT specified at 
<b>WSALookupServiceNext</b>, the returned information does not include the version, even though it was available. No error is generated.

Also for example, if LUP_RETURN_BLOB is NOT specified at 
<a href="https://msdn.microsoft.com/448309ef-b9dd-4960-8016-d26691df59ec">WSALookupServiceBegin</a> but is specified at 
<b>WSALookupServiceNext</b>, the returned information does not include the private data. No error is generated.

If the <b>WSALookupServiceNext</b> function fails with an error of 
								<a href="windows_sockets_error_codes_2.htm">WSAEFAULT</a>, this indicates that the buffer pointed to by the <i>lpqsResults</i> parameter was too small to contain the query results. A new buffer for a <a href="https://msdn.microsoft.com/6c81fbba-aaf4-49ca-ab79-b6fe5dfb0076">WSAQUERYSET</a> should be provided with a size specified by the value pointed to by  the <i>lpdwBufferLength</i> parameter. This new buffer for the <b>WSAQUERYSET</b> needs to have some of the members of the <b>WSAQUERYSET</b> specified before calling the <b>WSALookupServiceNext</b> function again. At a minimum, the <b>dwSize</b> member of the <b>WSAQUERYSET</b> must be set to the new size of the buffer.

<h3><a id="Query_Results"></a><a id="query_results"></a><a id="QUERY_RESULTS"></a>Query Results</h3>
The following table describes how the query results are represented in the 
<a href="https://msdn.microsoft.com/6c81fbba-aaf4-49ca-ab79-b6fe5dfb0076">WSAQUERYSET</a> structure.

<table>
<tr>
<th>WSAQUERYSET member</th>
<th>Result interpretation</th>
</tr>
<tr>
<td><b>dwSize</b></td>
<td>Will be set to sizeof(
<a href="https://msdn.microsoft.com/6c81fbba-aaf4-49ca-ab79-b6fe5dfb0076">WSAQUERYSET</a>). This is used as a versioning mechanism.</td>
</tr>
<tr>
<td><b>dwOutputFlags</b></td>
<td>RESULT_IS_ALIAS flag indicates this is an alias result.</td>
</tr>
<tr>
<td><b>lpszServiceInstanceName</b></td>
<td>Referenced string contains service name.</td>
</tr>
<tr>
<td><b>lpServiceClassId</b></td>
<td>The GUID corresponding to the service class.</td>
</tr>
<tr>
<td><b>lpVersion</b></td>
<td>References version number of the particular service instance.</td>
</tr>
<tr>
<td><b>lpszComment</b></td>
<td>Optional comment string specified by service instance.</td>
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
<td>When <i>dwControlFlags</i> includes LUP_RETURN_QUERY_STRING, this parameter returns the unparsed remainder of the <i>lpszServiceInstanceName</i> specified in the original query. For example, in a namespace that identifies services by hierarchical names that specify a host name and a file path within that host, the address returned might be the host address and the unparsed remainder might be the file path. If the <i>lpszServiceInstanceName</i> is fully parsed and LUP_RETURN_QUERY_STRING is used, this parameter is <b>NULL</b> or points to a zero-length string.</td>
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
<td>(Optional) This is a pointer to a provider-specific entity.</td>
</tr>
</table>
 

<b>Windows Phone 8:</b> The <b>WSALookupServiceNextW</b> function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: The <b>WSALookupServiceNextW</b> function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://msdn.microsoft.com/d43cf444-adb6-4313-9614-a8d6d868a88f">Bluetooth and WSALookupServiceNext</a>



<a href="https://msdn.microsoft.com/448309ef-b9dd-4960-8016-d26691df59ec">WSALookupServiceBegin</a>



<a href="https://msdn.microsoft.com/f9d2ac54-a818-464d-918e-80ebb5b1b106">WSALookupServiceEnd</a>



<a href="https://msdn.microsoft.com/6c81fbba-aaf4-49ca-ab79-b6fe5dfb0076">WSAQUERYSET</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>
 

 

