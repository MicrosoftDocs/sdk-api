---
UID: NS:winsock2._WSAQuerySet2A
title: WSAQUERYSET2A (winsock2.h)
description: Provides relevant information about a given service, including service class ID, service name , applicable namespace identifier and protocol information, as well as a set of transport addresses at which the service listens. (ANSI)
helpviewer_keywords: ["*LPWSAQUERYSET2A","*PWSAQUERYSET2A","LPWSAQUERYSET2","LPWSAQUERYSET2 structure pointer [Winsock]","NS_ALL","NS_BTH","NS_DNS","NS_EMAIL","NS_NLA","NS_PNRPCLOUD","NS_PNRPNAME","PWSAQUERYSET2","PWSAQUERYSET2 structure pointer [Winsock]","WSAQUERYSET2","WSAQUERYSET2 structure [Winsock]","WSAQUERYSET2A","WSAQUERYSET2W","winsock.wsaqueryset2","winsock2/LPWSAQUERYSET2","winsock2/PWSAQUERYSET2","winsock2/WSAQUERYSET2","winsock2/WSAQUERYSET2A","winsock2/WSAQUERYSET2W"]
old-location: winsock\wsaqueryset2.htm
tech.root: WinSock
ms.assetid: ffe71de0-3561-481f-b81f-835c6c3a3ee4
ms.date: 12/05/2018
ms.keywords: '*LPWSAQUERYSET2A, *PWSAQUERYSET2A, LPWSAQUERYSET2, LPWSAQUERYSET2 structure pointer [Winsock], NS_ALL, NS_BTH, NS_DNS, NS_EMAIL, NS_NLA, NS_PNRPCLOUD, NS_PNRPNAME, PWSAQUERYSET2, PWSAQUERYSET2 structure pointer [Winsock], WSAQUERYSET2, WSAQUERYSET2 structure [Winsock], WSAQUERYSET2A, WSAQUERYSET2W, winsock.wsaqueryset2, winsock2/LPWSAQUERYSET2, winsock2/PWSAQUERYSET2, winsock2/WSAQUERYSET2, winsock2/WSAQUERYSET2A, winsock2/WSAQUERYSET2W'
req.header: winsock2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WSAQUERYSET2W (Unicode) and WSAQUERYSET2A (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WSAQUERYSET2A, *PWSAQUERYSET2A, *LPWSAQUERYSET2A
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSAQuerySet2A
 - winsock2/_WSAQuerySet2A
 - PWSAQUERYSET2A
 - winsock2/PWSAQUERYSET2A
 - WSAQUERYSET2A
 - winsock2/WSAQUERYSET2A
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winsock2.h
api_name:
 - WSAQUERYSET2
 - WSAQUERYSET2A
 - WSAQUERYSET2W
---

# WSAQUERYSET2A structure


## -description

The 
<b>WSAQUERYSET2</b> structure provides relevant information about a given service, including service class ID, service name , applicable namespace identifier and protocol information, as well as a set of transport addresses at which the service listens.

## -struct-fields

### -field dwSize

Type: <b>DWORD</b>

The size, in bytes, of the <b>WSAQUERYSET2</b> structure. This member is used as a versioning mechanism since the size of the <b>WSAQUERYSET2</b> structure may change on later versions of Windows.

### -field lpszServiceInstanceName

Type: <b>LPTSTR</b>

A pointer to an optional <b>NULL</b>-terminated string  that contains service name. The semantics for using wildcards within the string are not defined, but can be supported by certain namespace providers.

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

A pointer to an optional GUID of a specific namespace provider to query in the case where  multiple namespace providers are registered under a single namespace such as <b>NS_DNS</b>. Passing the GUID for a specific namespace provider will result in only the specified namespace provider being queried. The <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersa">WSAEnumNameSpaceProviders</a> and <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersexa">WSAEnumNameSpaceProvidersEx</a> functions can be called to retrieve the GUID for a namespace provider.

### -field lpszContext

Type: <b>LPTSTR</b>

A pointer to an optional starting point of the query in a hierarchical namespace.

### -field dwNumberOfProtocols

Type: <b>DWORD</b>

The size, in bytes, of the protocol constraint array. This member can be zero.

### -field lpafpProtocols

Type: <b>LPAFPROTOCOLS</b>

A pointer to an optional array of 
<a href="/windows/desktop/api/winsock2/ns-winsock2-afprotocols">AFPROTOCOLS</a> structures. Only services that utilize these protocols will be returned.

### -field lpszQueryString

Type: <b>LPTSTR</b>

A pointer to an optional <b>NULL</b>-terminated query string. Some namespaces, such as Whois++, support enriched SQL-like queries that are contained in a simple text string. This parameter is used to specify that string.

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
<b>WSAQUERYSET2</b> structure is used as part of the namespace service provider version-2 (NSPv2) architecture available on Windows Vista and later. 

On Windows Vista and Windows Server 2008, the <b>WSAQUERYSET2</b> structure can only be used for operations on NS_EMAIL namespace providers.





> [!NOTE]
> The winsock2.h header defines WSAQUERYSET2 as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersa">WSAEnumNameSpaceProviders</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersexa">WSAEnumNameSpaceProvidersEx</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea">WSASetService</a>
