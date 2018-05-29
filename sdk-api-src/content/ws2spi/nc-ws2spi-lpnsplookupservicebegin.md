---
UID: NC:ws2spi.LPNSPLOOKUPSERVICEBEGIN
title: LPNSPLOOKUPSERVICEBEGIN
author: windows-sdk-content
description: Initiates a client query that is constrained by the information contained within a WSAQUERYSET structure.
old-location: winsock\nsplookupservicebegin_2.htm
old-project: WinSock
ms.assetid: a0b71821-4434-470f-b729-370d7e1722ec
ms.author: windowssdkdev
ms.date: 04/30/2018
ms.keywords: LPNSPLOOKUPSERVICEBEGIN, LUP_ADDRCONFIG, LUP_CONTAINERS, LUP_DEEP, LUP_DUAL_ADDR, LUP_FLUSHCACHE, LUP_FLUSHPREVIOUS, LUP_NEAREST, LUP_NOCONTAINERS, LUP_NON_AUTHORITATIVE, LUP_RES_RESERVICE, LUP_RETURN_ADDR, LUP_RETURN_ALIASES, LUP_RETURN_ALL, LUP_RETURN_BLOB, LUP_RETURN_COMMENT, LUP_RETURN_NAME, LUP_RETURN_PREFERRED_NAMES, LUP_RETURN_QUERY_STRING, LUP_RETURN_TYPE, LUP_RETURN_VERSION, LUP_SECURE, NSPLookupServiceBegin, NSPLookupServiceBegin function [Winsock], _win32_nsplookupservicebegin_2, winsock.nsplookupservicebegin_2, ws2spi/NSPLookupServiceBegin
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
req.typenames: SOCKADDR_INET, *PSOCKADDR_INET
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Ws2spi.h
api_name:
-	NSPLookupServiceBegin
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# LPNSPLOOKUPSERVICEBEGIN callback function


## -description



			The 
<b>NSPLookupServiceBegin</b> function initiates a client query of a name service provider that is constrained by the information contained within a 
<a href="https://msdn.microsoft.com/6c81fbba-aaf4-49ca-ab79-b6fe5dfb0076">WSAQUERYSET</a> structure.

<b>NSPLookupServiceBegin</b> only returns a handle, which should be used by subsequent calls to 
<a href="https://msdn.microsoft.com/321732e4-5d48-48f4-8795-ffac208852dc">NSPLookupServiceNext</a> to get the actual results. Because this operation cannot be canceled, it should be implemented to execute quickly. While it is acceptable to initiate a network query, this function should not require a response  to return successfully.


## -parameters




### -param lpProviderId [in]

A pointer to the name service provider identifier to query.


### -param lpqsRestrictions [in]

A pointer to the search criteria. See Remarks.


### -param lpServiceClassInfo [in]

A pointer to the  <a href="https://msdn.microsoft.com/02422c24-34a6-4e34-a795-66b0b687ac44">WSASERVICECLASSINFO</a> structure that contains schema information for the service.


### -param dwControlFlags [in]

A value that controls the depth of the search.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LUP_DEEP"></a><a id="lup_deep"></a><dl>
<dt><b>LUP_DEEP</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Queries down the hierarchy of a provider as opposed to just the first level.

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
Returns no containers.

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
Retrieves the name as <b>lpszServiceInstanceName</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_RETURN_TYPE"></a><a id="lup_return_type"></a><dl>
<dt><b>LUP_RETURN_TYPE</b></dt>
<dt>0x0020</dt>
</dl>
</td>
<td width="60%">
Retrieves the type as <b>lpServiceClassId</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_RETURN_VERSION"></a><a id="lup_return_version"></a><dl>
<dt><b>LUP_RETURN_VERSION</b></dt>
<dt>0x0040</dt>
</dl>
</td>
<td width="60%">
Retrieves the version as <b>lpVersion</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_RETURN_COMMENT"></a><a id="lup_return_comment"></a><dl>
<dt><b>LUP_RETURN_COMMENT</b></dt>
<dt>0x0080</dt>
</dl>
</td>
<td width="60%">
Retrieves the comment as <b>lpszComment</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_RETURN_ADDR"></a><a id="lup_return_addr"></a><dl>
<dt><b>LUP_RETURN_ADDR</b></dt>
<dt>0x0100</dt>
</dl>
</td>
<td width="60%">
Retrieves the addresses as <b>lpcsaBuffer</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_RETURN_BLOB"></a><a id="lup_return_blob"></a><dl>
<dt><b>LUP_RETURN_BLOB</b></dt>
<dt>0x0200</dt>
</dl>
</td>
<td width="60%">
Retrieves the private data as <b>lpBlob</b>.

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
<a href="https://msdn.microsoft.com/321732e4-5d48-48f4-8795-ffac208852dc">NSPLookupServiceNext</a>, and each alias returned will have the <b>RESULT_IS_ALIAS</b> flag set.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_RETURN_QUERY_STRING"></a><a id="lup_return_query_string"></a><dl>
<dt><b>LUP_RETURN_QUERY_STRING</b></dt>
<dt>0x0800</dt>
</dl>
</td>
<td width="60%">
Retrieves the query string as <b>lpszQueryString</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_RETURN_ALL"></a><a id="lup_return_all"></a><dl>
<dt><b>LUP_RETURN_ALL</b></dt>
<dt>0x0ff0</dt>
</dl>
</td>
<td width="60%">
Retrieves information including the name, type, version, comment, address, blob, aliases, and query string.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_FLUSHCACHE"></a><a id="lup_flushcache"></a><dl>
<dt><b>LUP_FLUSHCACHE</b></dt>
<dt>0x1000</dt>
</dl>
</td>
<td width="60%">
If the provider has cached information, ignore the cache and query the namespace itself.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_FLUSHPREVIOUS"></a><a id="lup_flushprevious"></a><dl>
<dt><b>LUP_FLUSHPREVIOUS</b></dt>
<dt>0x2000</dt>
</dl>
</td>
<td width="60%">
Used as a value for the <i>dwControlFlags</i> parameter in 
<a href="https://msdn.microsoft.com/321732e4-5d48-48f4-8795-ffac208852dc">NSPLookupServiceNext</a>. Setting this flag instructs the provider to discard the last result set, which was too large for the supplied buffer, and move on to the next result set.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_NON_AUTHORITATIVE"></a><a id="lup_non_authoritative"></a><dl>
<dt><b>LUP_NON_AUTHORITATIVE</b></dt>
<dt>0x4000</dt>
</dl>
</td>
<td width="60%">
Indicates that the namespace provider should included non-authoritative results for names. 

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_RES_RESERVICE"></a><a id="lup_res_reservice"></a><dl>
<dt><b>LUP_RES_RESERVICE</b></dt>
<dt>0x8000</dt>
</dl>
</td>
<td width="60%">
Indicates whether prime response is in the remote or local part of 
<a href="https://msdn.microsoft.com/9cad3586-e315-4f6f-9045-7c95502bb768">CSADDR_INFO</a> structure. The other part must be usable in either case. This option applies only to service instance requests.

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_SECURE"></a><a id="lup_secure"></a><dl>
<dt><b>LUP_SECURE</b></dt>
<dt>0x8000</dt>
</dl>
</td>
<td width="60%">
Indicates that the namespace provider should use a secure query. This option only applies to name query requests. 

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_RETURN_PREFERRED_NAMES"></a><a id="lup_return_preferred_names"></a><dl>
<dt><b>LUP_RETURN_PREFERRED_NAMES</b></dt>
<dt>0x10000</dt>
</dl>
</td>
<td width="60%">
Indicates that the namespace provider should return only preferred names. 

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_ADDRCONFIG"></a><a id="lup_addrconfig"></a><dl>
<dt><b>LUP_ADDRCONFIG</b></dt>
<dt>0x100000</dt>
</dl>
</td>
<td width="60%">
Indicates that the namespace provider should return the address configuration. 

</td>
</tr>
<tr>
<td width="40%"><a id="LUP_DUAL_ADDR"></a><a id="lup_dual_addr"></a><dl>
<dt><b>LUP_DUAL_ADDR</b></dt>
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
<a href="https://msdn.microsoft.com/321732e4-5d48-48f4-8795-ffac208852dc">NSPLookupServiceNext</a> in order to retrieve the results set.


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
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
One or more parameters were invalid, or missing, for this provider.

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
The name was found in the database, but it does not have the correct associated data that is resolved for.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSASERVICE_NOT_FOUND</a></b></dt>
</dl>
</td>
<td width="60%">
Service is unknown. The service cannot be found in the specified namespace.

</td>
</tr>
</table>
 




## -remarks



If <b>LUP_CONTAINERS</b> is specified in a call, avoid all other restriction values. If any are supplied, the name service provider must decide if it can support this restriction over the containers. If not, it should return an error.

Some name service providers may have other means of finding containers. For example, containers can all be of some well-known type, or of a set of well-known types, and therefore a query restriction could be created for finding them. No matter what other means the name service provider has for locating containers, <b>LUP_CONTAINERS</b> and <b>LUP_NOCONTAINERS</b> take precedence. Therefore, if a query restriction is given that includes containers, specifying <b>LUP_NOCONTAINERS</b> will prevent the container items from being returned. Similarly, no matter what the query restriction, if <b>LUP_CONTAINERS</b> is given, only containers should be returned. If a namespace does not support containers and <b>LUP_CONTAINERS</b> is specified, it should return <a href="windows_sockets_error_codes_2.htm">WSANO_DATA</a>.

The preferred method of obtaining the containers within another container, is the call:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>dwStatus = NSPLookupServiceBegin(
    lpqsRestrictions,
    LUP_CONTAINERS,
    lphLookup);
</pre>
</td>
</tr>
</table></span></div>
followed by the requisite number of 
<a href="https://msdn.microsoft.com/321732e4-5d48-48f4-8795-ffac208852dc">NSPLookupServiceNext</a> calls. This will return all containers contained immediately within the starting context; that is, it is not a deep query. With this, one can map the address space structure by walking the hierarchy, perhaps enumerating the content of selected containers. Subsequent uses of 
<b>NSPLookupServiceBegin</b> use the containers returned from a previous call.

<h3><a id="Forming_Queries"></a><a id="forming_queries"></a><a id="FORMING_QUERIES"></a>Forming Queries</h3>


As mentioned, a 
<a href="https://msdn.microsoft.com/6c81fbba-aaf4-49ca-ab79-b6fe5dfb0076">WSAQUERYSET</a> structure is used as an input parameter to 
<b>NSPLookupServiceBegin</b> to qualify the query. The following table lists <b>WSAQUERYSET</b> member names and describes how the 
<b>WSAQUERYSET</b> is used to construct a query. When a member is marked as (Optional) a null pointer can be supplied, indicating that the parameter will not be used as a search criteria. For more information, see <a href="name_resolution_data_structures_2.htm">Query-Related Data Structures</a>.

<table>
<tr>
<th>WSAQUERYSET member name</th>
<th>Query interpretation</th>
</tr>
<tr>
<td><b>dwSize</b></td>
<td>Will be set to sizeof(<a href="https://msdn.microsoft.com/6c81fbba-aaf4-49ca-ab79-b6fe5dfb0076">WSAQUERYSET</a>). This is a versioning mechanism.</td>
</tr>
<tr>
<td><b>dwOutputFlags</b></td>
<td>Ignored for queries.</td>
</tr>
<tr>
<td><b>lpszServiceInstanceName</b></td>
<td>Optional. Referenced string contains service name. The semantics for wildcarding within the string are not defined, but can be supported by certain namespace providers.</td>
</tr>
<tr>
<td><b>lpServiceClassId</b></td>
<td>Required. GUID corresponding to the service class.</td>
</tr>
<tr>
<td><b>lpVersion</b></td>
<td>Optional. References desired version number and provides version comparison semantics (that is, version must match exactly, or version must be not less than the value supplied).</td>
</tr>
<tr>
<td><b>lpszComment</b></td>
<td>Ignored for queries.</td>
</tr>
<tr>
<td><b>dwNameSpace</b></td>
<td>Identifier of a single namespace in which to constrain the search, or <b>NS_ALL</b> to include all namespaces.</td>
</tr>
<tr>
<td><b>lpNSProviderId</b></td>
<td>Optional. References the GUID of a specific namespace provider and limits the query to this provider only.</td>
</tr>
<tr>
<td><b>lpszContext</b></td>
<td>Optional. Specifies the starting point of the query in a hierarchical namespace.</td>
</tr>
<tr>
<td><b>dwNumberOfProtocols</b></td>
<td>Size, in bytes, of the number of entries in the protocol constraint array, can be zero.</td>
</tr>
<tr>
<td><b>lpafpProtocols</b></td>
<td>Optional. A references to an array of 
<a href="https://msdn.microsoft.com/ffd43aa1-bbc4-46f1-ad77-26c48f9ac0b7">AFPROTOCOLS</a> structures. Only services that use these protocols will be returned. It is permissable for the value <b>AF_UNSPEC</b> to appear as a protocol family value, signifying a wildcard. Namespace providers may supply information about any service that uses the corresponding protocol, regardless of address family.</td>
</tr>
<tr>
<td><b>lpszQueryString</b></td>
<td>Optional. Some namespaces (such as whois++) support rich SQL-like queries contained in a simple text string. This parameter is used to specify that string.</td>
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
<td>Optional. A pointer to a provider-specific entity.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ffd43aa1-bbc4-46f1-ad77-26c48f9ac0b7">AFPROTOCOLS</a>



<a href="https://msdn.microsoft.com/ec72c89a-a74b-449c-996a-02057dff9137">NSPLookupServiceEnd</a>



<a href="https://msdn.microsoft.com/321732e4-5d48-48f4-8795-ffac208852dc">NSPLookupServiceNext</a>



<a href="https://msdn.microsoft.com/8f7736d5-ea77-472a-a94f-e422398fae3f">NSP_ROUTINE</a>



<a href="https://msdn.microsoft.com/6c81fbba-aaf4-49ca-ab79-b6fe5dfb0076">WSAQUERYSET</a>



<a href="https://msdn.microsoft.com/02422c24-34a6-4e34-a795-66b0b687ac44">WSASERVICECLASSINFO</a>



<a href="https://msdn.microsoft.com/596155ee-3dcc-4ae3-97ab-0653e019cbee">WSASetLastError</a>
 

 

