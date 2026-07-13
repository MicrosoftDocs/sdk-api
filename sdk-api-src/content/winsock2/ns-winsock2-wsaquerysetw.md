---
UID: NS:winsock2._WSAQuerySetW
title: WSAQUERYSETW (winsock2.h)
description: Provides relevant information about a given service, including service class ID, service name, applicable namespace identifier and protocol information, as well as a set of transport addresses at which the service listens. (Unicode)
helpviewer_keywords: ["*LPWSAQUERYSETW","*PWSAQUERYSETW","LPWSAQUERYSET","LPWSAQUERYSET structure pointer [Winsock]","NS_ALL","NS_BTH","NS_DNS","NS_EMAIL","NS_NLA","NS_PNRPCLOUD","NS_PNRPNAME","PWSAQUERYSET","PWSAQUERYSET structure pointer [Winsock]","WSAQUERYSET","WSAQUERYSET structure [Winsock]","WSAQUERYSETA","WSAQUERYSETW","_win32_wsaqueryset_2","winsock.wsaqueryset_2","winsock2/LPWSAQUERYSET","winsock2/PWSAQUERYSET","winsock2/WSAQUERYSET","winsock2/WSAQUERYSETA","winsock2/WSAQUERYSETW"]
old-location: winsock\wsaqueryset_2.htm
tech.root: WinSock
ms.assetid: 6c81fbba-aaf4-49ca-ab79-b6fe5dfb0076
ms.date: 12/05/2018
ms.keywords: '*LPWSAQUERYSETW, *PWSAQUERYSETW, LPWSAQUERYSET, LPWSAQUERYSET structure pointer [Winsock], NS_ALL, NS_BTH, NS_DNS, NS_EMAIL, NS_NLA, NS_PNRPCLOUD, NS_PNRPNAME, PWSAQUERYSET, PWSAQUERYSET structure pointer [Winsock], WSAQUERYSET, WSAQUERYSET structure [Winsock], WSAQUERYSETA, WSAQUERYSETW, _win32_wsaqueryset_2, winsock.wsaqueryset_2, winsock2/LPWSAQUERYSET, winsock2/PWSAQUERYSET, winsock2/WSAQUERYSET, winsock2/WSAQUERYSETA, winsock2/WSAQUERYSETW'
req.header: winsock2.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WSAQUERYSETW, *PWSAQUERYSETW, *LPWSAQUERYSETW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSAQuerySetW
 - winsock2/_WSAQuerySetW
 - PWSAQUERYSETW
 - winsock2/PWSAQUERYSETW
 - WSAQUERYSETW
 - winsock2/WSAQUERYSETW
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
 - WSAQUERYSET
 - WSAQUERYSETA
 - WSAQUERYSETW
---

# WSAQUERYSETW structure


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





> [!NOTE]
> The winsock2.h header defines WSAQUERYSET as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Bluetooth/bluetooth-and-wsaqueryset-for-device-inquiry">Bluetooth and WSAQUERYSET for Device Inquiry</a>



<a href="/windows/desktop/Bluetooth/bluetooth-and-wsaqueryset-for-service-inquiry">Bluetooth and WSAQUERYSET for Service Inquiry</a>



<a href="/windows/desktop/Bluetooth/bluetooth-and-wsaqueryset-for-set-service">Bluetooth and WSAQUERYSET for Set Service</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersa">WSAEnumNameSpaceProviders</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersexa">WSAEnumNameSpaceProvidersEx</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina">WSALookupServiceBegin</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta">WSALookupServiceNext</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaqueryset2w">WSAQUERYSET2</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea">WSASetService</a>
