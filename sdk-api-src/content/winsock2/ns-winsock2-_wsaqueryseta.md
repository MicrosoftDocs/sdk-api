---
UID: NS:winsock2._WSAQuerySetA
title: "_WSAQuerySetA"
author: windows-sdk-content
description: Provides relevant information about a given service, including service class ID, service name, applicable namespace identifier and protocol information, as well as a set of transport addresses at which the service listens.
old-location: winsock\wsaqueryset_2.htm
old-project: winsock
ms.assetid: 6c81fbba-aaf4-49ca-ab79-b6fe5dfb0076
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: "*LPWSAQUERYSETA, *PWSAQUERYSETA, LPWSAQUERYSET, LPWSAQUERYSET structure pointer [Winsock], NS_ALL, NS_BTH, NS_DNS, NS_EMAIL, NS_NLA, NS_PNRPCLOUD, NS_PNRPNAME, PWSAQUERYSET, PWSAQUERYSET structure pointer [Winsock], WSAQUERYSET, WSAQUERYSET structure [Winsock], WSAQUERYSETA, WSAQUERYSETW, _WSAQuerySetA, _win32_wsaqueryset_2, winsock.wsaqueryset_2, winsock2/LPWSAQUERYSET, winsock2/PWSAQUERYSET, winsock2/WSAQUERYSET, winsock2/WSAQUERYSETA, winsock2/WSAQUERYSETW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winsock2.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WSAQUERYSETW (Unicode) and WSAQUERYSETA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSAQUERYSETA, *PWSAQUERYSETA, *LPWSAQUERYSETA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winsock2.h
api_name:
 - WSAQUERYSET
 - WSAQUERYSETA
 - WSAQUERYSETW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSAQuerySetA structure


## -description


The 
<b>WSAQUERYSET</b> structure provides relevant information about a given service, including service class ID, service name, applicable namespace identifier and protocol information, as well as a set of transport addresses at which the service listens.


## -struct-fields




### -field dwSize

Type: <b>DWORD</b>

The size, in bytes, of the <b>WSAQUERYSET</b> structure. This member is used as a versioning mechanism since the size of the <b>WSAQUERYSET</b> structure has changed on later versions of Windows.


### -field lpszServiceInstanceName

Type: <b>LPTSTR</b>

A pointer to an optional NULL-terminated string  that contains service name. The semantics for using wildcards within the string are not defined, but can be supported by certain namespace providers. 


### -field lpServiceClassId

Type: <b>LPGUID</b>

The GUID corresponding to the service class. This member is required to be set.


### -field lpVersion

Type: <b>LPWSAVERSION</b>

A pointer to an optional desired version number of the namespace provider. This member provides version comparison semantics (that is, the version requested must match exactly, or version must be not less than the value supplied). 


### -field lpszComment

Type: <b>LPTSTR</b>

This member is ignored for queries.


### -field dwNameSpace

Type: <b>DWORD</b>

A namespace identifier that determines which namespace providers are queried.  Passing a specific namespace identifier will result in only namespace providers that support the specified namespace being queried. Specifying <b>NS_ALL</b> will result in all installed and active namespace providers being queried. 


Options for the <b>dwNameSpace</b> member are listed in the <i>Winsock2.h</i> include file. Several new namespace providers are included with Windows Vista and later. Other namespace providers can be installed, so the following possible values  are only those commonly available. Many other values are possible.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NS_ALL"></a><a id="ns_all"></a><dl>
<dt><b>NS_ALL</b></dt>
</dl>
</td>
<td width="60%">
All installed and active namespaces.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_BTH"></a><a id="ns_bth"></a><dl>
<dt><b>NS_BTH</b></dt>
</dl>
</td>
<td width="60%">
The Bluetooth namespace. This namespace identifier is supported on Windows Vista and later.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_DNS"></a><a id="ns_dns"></a><dl>
<dt><b>NS_DNS</b></dt>
</dl>
</td>
<td width="60%">
The domain name system (DNS) namespace.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_EMAIL"></a><a id="ns_email"></a><dl>
<dt><b>NS_EMAIL</b></dt>
</dl>
</td>
<td width="60%">
The email namespace. This namespace identifier is supported on Windows Vista and later.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_NLA"></a><a id="ns_nla"></a><dl>
<dt><b>NS_NLA</b></dt>
</dl>
</td>
<td width="60%">
The network location awareness (NLA) namespace. This namespace identifier is supported on Windows XP and later.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_PNRPNAME"></a><a id="ns_pnrpname"></a><dl>
<dt><b>NS_PNRPNAME</b></dt>
</dl>
</td>
<td width="60%">
The peer-to-peer name space for a specific peer name. This namespace identifier is supported on Windows Vista and later.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_PNRPCLOUD"></a><a id="ns_pnrpcloud"></a><dl>
<dt><b>NS_PNRPCLOUD</b></dt>
</dl>
</td>
<td width="60%">
The peer-to-peer name space for a collection of peer names. This namespace identifier is supported on Windows Vista and later.

</td>
</tr>
</table>
 


### -field lpNSProviderId

Type: <b>LPGUID</b>

A pointer to an optional GUID of a specific namespace provider to query in the case where  multiple namespace providers are registered under a single namespace such as <b>NS_DNS</b>. Passing the GUID for a specific namespace provider will result in only the specified namespace provider being queried. The <a href="https://msdn.microsoft.com/f5b6cd42-c5cb-43b6-bb96-fd260217e252">WSAEnumNameSpaceProviders</a> and <a href="https://msdn.microsoft.com/34bc96aa-63f7-4ab8-9376-6f4b979225ca">WSAEnumNameSpaceProvidersEx</a> functions can be called to retrieve the GUID for a namespace provider. 


### -field lpszContext

Type: <b>LPTSTR</b>

A pointer to an optional starting point of the query in a hierarchical namespace.


### -field dwNumberOfProtocols

Type: <b>DWORD</b>

The size, in bytes, of the protocol constraint array. This member can be zero.


### -field lpafpProtocols

Type: <b>LPAFPROTOCOLS</b>

A pointer to an optional array of 
<a href="https://msdn.microsoft.com/ffd43aa1-bbc4-46f1-ad77-26c48f9ac0b7">AFPROTOCOLS</a> structures. Only services that utilize these protocols will be returned.


### -field lpszQueryString

Type: <b>LPTSTR</b>

A pointer to an optional NULL-terminated query string. Some namespaces, such as Whois++, support enriched SQL-like queries that are contained in a simple text string. This parameter is used to specify that string.


### -field dwNumberOfCsAddrs

Type: <b>DWORD</b>

This member is ignored for queries.


### -field lpcsaBuffer

Type: <b>LPCSADDR_INFO</b>

This member is ignored for queries.


### -field dwOutputFlags

Type: <b>DWORD</b>

This member is ignored for queries.


### -field lpBlob

Type: <b>LPBLOB</b>

An optional pointer to data that is used to query or set provider-specific namespace information. The format of this information is specific to the namespace provider. 



## -remarks



The 
<b>WSAQUERYSET</b> structure is used as part of the original namespace provider version 1 architecture available on Windows 95 and later. A newer version 2 of the namespace architecture  is available on Windows Vista and later. 

In most instances, applications interested in only a particular transport protocol should constrain their query by address family and protocol rather than by namespace. This would allow an application that needs to locate a TCP/IP service, for example, to have its query processed by all available namespaces such as the local hosts file, DNS, and NIS.




## -see-also




<a href="https://msdn.microsoft.com/0c0d26f7-b6c3-42a9-8c01-118278c381cc">Bluetooth and WSAQUERYSET for Device Inquiry</a>



<a href="https://msdn.microsoft.com/c52a7e7d-92ab-4103-a6c6-57c3fafec706">Bluetooth and WSAQUERYSET for Service Inquiry</a>



<a href="https://msdn.microsoft.com/e582156d-a298-4d9b-8ed1-4c558fa4f203">Bluetooth and WSAQUERYSET for Set Service</a>



<a href="https://msdn.microsoft.com/f5b6cd42-c5cb-43b6-bb96-fd260217e252">WSAEnumNameSpaceProviders</a>



<a href="https://msdn.microsoft.com/34bc96aa-63f7-4ab8-9376-6f4b979225ca">WSAEnumNameSpaceProvidersEx</a>



<a href="https://msdn.microsoft.com/448309ef-b9dd-4960-8016-d26691df59ec">WSALookupServiceBegin</a>



<a href="https://msdn.microsoft.com/ab4f1830-b38d-4224-a6a9-6d4512245ad6">WSALookupServiceNext</a>



<a href="https://msdn.microsoft.com/ffe71de0-3561-481f-b81f-835c6c3a3ee4">WSAQUERYSET2</a>



<a href="https://msdn.microsoft.com/21a8ff26-4c9e-4846-a75a-1a27c746edab">WSASetService</a>
 

 

