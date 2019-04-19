---
UID: NC:ws2spi.LPNSPV2LOOKUPSERVICEBEGIN
title: LPNSPV2LOOKUPSERVICEBEGIN (ws2spi.h)
author: windows-sdk-content
description: Initiates a client query of a namespace version-2 service provider that is constrained by the information contained within a WSAQUERYSET2 structure.
old-location: winsock\nspv2lookupservicebegin.htm
tech.root: WinSock
ms.assetid: 5664b85d-8432-4068-aa97-caa57d9377ac
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: LPNSPV2LOOKUPSERVICEBEGIN, LUP_ADDRCONFIG, LUP_CONTAINERS, LUP_DEEP, LUP_DISABLE_IDN_ENCODING, LUP_DUAL_ADDR, LUP_FLUSHCACHE, LUP_FLUSHPREVIOUS, LUP_NEAREST, LUP_NOCONTAINERS, LUP_NON_AUTHORITATIVE, LUP_RES_RESERVICE, LUP_RETURN_ADDR, LUP_RETURN_ALIASES, LUP_RETURN_ALL, LUP_RETURN_BLOB, LUP_RETURN_COMMENT, LUP_RETURN_NAME, LUP_RETURN_PREFERRED_NAMES, LUP_RETURN_QUERY_STRING, LUP_RETURN_TYPE, LUP_RETURN_VERSION, LUP_SECURE, NSPv2LookupServiceBegin, NSPv2LookupServiceBegin function [Winsock], winsock.nspv2lookupservicebegin, ws2spi/NSPv2LookupServiceBegin
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ws2spi.h
api_name:
 - NSPv2LookupServiceBegin
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LPNSPV2LOOKUPSERVICEBEGIN callback function


## -description


The 
<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPv2LookupServiceBegin</a> function initiates a client query of a namespace version-2 service provider that is constrained by the information contained within a 
<a href="https://msdn.microsoft.com/ffe71de0-3561-481f-b81f-835c6c3a3ee4">WSAQUERYSET2</a> structure.


## -parameters




### -param lpProviderId [in]

A pointer to the identifier for the namespace service provider to query.


### -param lpqsRestrictions [in]

A pointer to the search criteria. See Remarks.


### -param dwControlFlags [in]

A set of flags that affect the search. This parameter can be a combination of the following values defined in the <i>Winsock2.h</i> header file.

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
<a href="https://msdn.microsoft.com/957fe544-9a3f-47f4-a98c-0624747650f4">NSPv2LookupServiceNextEx</a>, and each alias returned will have the <b>RESULT_IS_ALIAS</b> flag set.

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
<a href="https://msdn.microsoft.com/957fe544-9a3f-47f4-a98c-0624747650f4">NSPv2LookupServiceNextEx</a>. Setting this flag instructs the provider to discard the last result set, which was too large for the supplied buffer, and move on to the next result set.

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
<tr>
<td width="40%"><a id="LUP_DISABLE_IDN_ENCODING"></a><a id="lup_disable_idn_encoding"></a><dl>
<dt><b>LUP_DISABLE_IDN_ENCODING</b></dt>
<dt>0x800000</dt>
</dl>
</td>
<td width="60%">
Indicates that the namespace provider should disable automatic International Domain Names encoding.

This value is supported on Windows 8 and Windows Server 2012

</td>
</tr>
</table>
 


### -param lpvClientSessionArg [out]

A pointer to the client session.


### -param lphLookup [out]

A pointer to the handle to be used in subsequent calls to 
<a href="https://msdn.microsoft.com/957fe544-9a3f-47f4-a98c-0624747650f4">NSPv2LookupServiceNextEx</a> in order to retrieve the results set.


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
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
One or more parameters were invalid, or missing, for this provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSANO_DATA</a></b></dt>
</dl>
</td>
<td width="60%">
The name was found in the database, but it does not have the correct associated data that is resolved for.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSASERVICE_NOT_FOUND</a></b></dt>
</dl>
</td>
<td width="60%">
The service is unknown. The service cannot be found in the specified namespace.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory available to perform this operation.

</td>
</tr>
</table>
 




## -remarks



The 
<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPv2LookupServiceBegin</a> function is used as part of the namespace service provider version-2 (NSPv2) architecture available on Windows Vista and later. 

On Windows Vista and Windows Server 2008, the <a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPv2LookupServiceBegin</a> function can only be used for operations on NS_EMAIL namespace providers.

The 
				<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPv2LookupServiceBegin</a> function only returns a handle, which should be used by subsequent calls to 
<a href="https://msdn.microsoft.com/957fe544-9a3f-47f4-a98c-0624747650f4">NSPv2LookupServiceNextEx</a> to get the actual results. Because this operation cannot be canceled, it should be implemented to execute quickly. While it is acceptable to initiate a network query, this function should not require a response  to return successfully.

The 
<a href="https://msdn.microsoft.com/93224e66-9c94-4b5c-af11-ae988b74bc03">NSPv2Startup</a> function is called each time a new client process begins using namespace provider.  Providers may use the 
client session argument pointed to by the <i>ppvClientSessionArg</i> parameter to store information about this session. If a value was specified for the client session argument in the call to the <b>NSPv2Startup</b> function, then this same client session argument is passed in the  <i>lpvClientSessionArg </i> parameter to the <a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPv2LookupServiceBegin</a> function.

If <b>LUP_CONTAINERS</b> is specified in a call, avoid all other restriction values. If any are supplied, the name service provider must decide if it can support this restriction over the containers. If not, it should return an error.

Some name service providers may have other means of finding containers. For example, containers can all be of some well-known type, or of a set of well-known types, and therefore a query restriction could be created for finding them. No matter what other means the name service provider has for locating containers, <b>LUP_CONTAINERS</b> and <b>LUP_NOCONTAINERS</b> take precedence. Therefore, if a query restriction is given that includes containers, specifying <b>LUP_NOCONTAINERS</b> will prevent the container items from being returned. Similarly, no matter what the query restriction, if <b>LUP_CONTAINERS</b> is given, only containers should be returned. If a namespace does not support containers and <b>LUP_CONTAINERS</b> is specified, it should return <a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSANO_DATA</a>.

The preferred method of obtaining the containers within another container, is the call:


```cpp
dwStatus = NSPv2LookupServiceBegin(
    lpProviderId,
    lpqsRestrictions,
    LUP_CONTAINERS,
    lpClientSession,
    lphLookup);

```


followed by the requisite number of 
<a href="https://msdn.microsoft.com/957fe544-9a3f-47f4-a98c-0624747650f4">NSPv2LookupServiceNextEx</a> calls. This will return all containers contained immediately within the starting context; that is, it is not a deep query. With this, one can map the address space structure by walking the hierarchy, perhaps enumerating the content of selected containers. Subsequent uses of 
<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPv2LookupServiceBegin</a> use the containers returned from a previous call.

<h3><a id="Forming_Queries"></a><a id="forming_queries"></a><a id="FORMING_QUERIES"></a>Forming Queries</h3>
The 
<a href="https://msdn.microsoft.com/ffe71de0-3561-481f-b81f-835c6c3a3ee4">WSAQUERYSET2</a> structure is used as an input parameter to 
<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPv2LookupServiceBegin</a> to qualify the query. The following table lists <b>WSAQUERYSET2</b> member names and describes how the 
<b>WSAQUERYSET2</b> is used to construct a query. Members labeled as optional and dependent on the requirements of the NSPv2 provider may be supplied as a <b>NULL</b> pointer when unused as a search criteria by the namespace provider. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms739852(v=VS.85).aspx">Query-Related Data Structures</a>.

<table>
<tr>
<th>WSAQUERYSET2 member name</th>
<th>Query interpretation</th>
</tr>
<tr>
<td><b>dwSize</b></td>
<td>Will be set to sizeof(<a href="https://msdn.microsoft.com/ffe71de0-3561-481f-b81f-835c6c3a3ee4">WSAQUERYSET2</a>). This is a versioning mechanism.</td>
</tr>
<tr>
<td><b>lpszServiceInstanceName</b></td>
<td>A string that contains the service name. The semantics for wildcarding within the string are not defined, but can be supported by certain namespace providers. This member is optional, dependent on the requirements of the NSPv2 service provider.

</td>
</tr>
<tr>
<td><b>lpVersion</b></td>
<td>The  desired version number that provides version comparison semantics (that is, version must match exactly, or version must be not less than the value supplied). This member is optional, dependent on the requirements of the NSPv2 service provider.

</td>
</tr>
<tr>
<td><b>lpszComment</b></td>
<td>This member is ignored for queries.</td>
</tr>
<tr>
<td><b>dwNameSpace</b></td>
<td>The identifier of a single namespace in which to constrain the search, or <b>NS_ALL</b> to include all namespaces.</td>
</tr>
<tr>
<td><b>lpNSProviderId</b></td>
<td>The GUID of a specific namespace provider that limits the query to this provider only. This member is optional, dependent on the requirements of the NSPv2 service provider.

</td>
</tr>
<tr>
<td><b>lpszContext</b></td>
<td>The starting point of the query in a hierarchical namespace. This member is optional, dependent on the requirements of the NSPv2 service provider.

</td>
</tr>
<tr>
<td><b>dwNumberOfProtocols</b></td>
<td>The size, in bytes, of the number of entries in the protocol constraint array. This member can be zero.</td>
</tr>
<tr>
<td><b>lpafpProtocols</b></td>
<td>An array of 
<a href="https://msdn.microsoft.com/ffd43aa1-bbc4-46f1-ad77-26c48f9ac0b7">AFPROTOCOLS</a> structures. Only services that use these protocols will be returned. It is permissable for the value <b>AF_UNSPEC</b> to appear as a protocol family value, signifying a wildcard. Namespace providers may supply information about any service that uses the corresponding protocol, regardless of address family. This member is optional, dependent on the requirements of the NSPv2 service provider.

</td>
</tr>
<tr>
<td><b>lpszQueryString</b></td>
<td>Some namespaces (such as whois++) support rich SQL-like queries contained in a simple text string. This parameter is used to specify that string.This member is optional, dependent on the requirements of the NSPv2 service provider.

</td>
</tr>
<tr>
<td><b>dwNumberOfCsAddrs</b></td>
<td>This member is ignored for queries.</td>
</tr>
<tr>
<td><b>lpcsaBuffer</b></td>
<td>This member is ignored for queries.</td>
</tr>
<tr>
<td><b>dwOutputFlags</b></td>
<td>This member is ignored for queries.</td>
</tr>
<tr>
<td><b>lpBlob</b></td>
<td>A pointer to a provider-specific entity. This member is optional, dependent on the requirements of the NSPv2 service provider.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ffd43aa1-bbc4-46f1-ad77-26c48f9ac0b7">AFPROTOCOLS</a>



<a href="https://msdn.microsoft.com/22a4ee47-030b-4aee-b9b1-c9e33b3e4fce">NSPV2_ROUTINE</a>



<a href="https://msdn.microsoft.com/36064c0e-c83c-4819-a3e4-c89df50eb659">NSPv2Cleanup</a>



<a href="https://msdn.microsoft.com/7379b502-129a-4dac-b7eb-e6fae8fb23f8">NSPv2ClientSessionRundown</a>



<a href="https://msdn.microsoft.com/5f2b56c5-3a8e-4bf9-8f28-d2a06543227b">NSPv2LookupServiceEnd</a>



<a href="https://msdn.microsoft.com/957fe544-9a3f-47f4-a98c-0624747650f4">NSPv2LookupServiceNextEx</a>



<a href="https://msdn.microsoft.com/596fe0bd-ec11-44f3-bffe-333758171ea6">NSPv2SetServiceEx</a>



<a href="https://msdn.microsoft.com/93224e66-9c94-4b5c-af11-ae988b74bc03">NSPv2Startup</a>



<a href="https://msdn.microsoft.com/ffe71de0-3561-481f-b81f-835c6c3a3ee4">WSAQUERYSET2</a>



<a href="https://msdn.microsoft.com/02422c24-34a6-4e34-a795-66b0b687ac44">WSASERVICECLASSINFO</a>



<a href="https://msdn.microsoft.com/596155ee-3dcc-4ae3-97ab-0653e019cbee">WSASetLastError</a>
 

 

