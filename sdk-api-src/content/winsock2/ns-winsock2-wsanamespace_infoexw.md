---
UID: NS:winsock2._WSANAMESPACE_INFOEXW
title: WSANAMESPACE_INFOEXW (winsock2.h)
description: Contains all registration information for a namespace provider. (WSANAMESPACE_INFOEXW)
helpviewer_keywords: ["*LPWSANAMESPACE_INFOEXW","*PWSANAMESPACE_INFOEXW","LPWSANAMESPACE_INFOEX","LPWSANAMESPACE_INFOEX structure pointer [Winsock]","NS_BTH","NS_DNS","NS_EMAIL","NS_NLA","NS_NTDS","NS_PNRPCLOUD","NS_PNRPNAME","PWSANAMESPACE_INFOEX","PWSANAMESPACE_INFOEX structure pointer [Winsock]","WSANAMESPACE_INFOEX","WSANAMESPACE_INFOEX structure [Winsock]","WSANAMESPACE_INFOEXA","WSANAMESPACE_INFOEXW","winsock.wsanamespace_infoex","winsock2/LPWSANAMESPACE_INFOEX","winsock2/PWSANAMESPACE_INFOEX","winsock2/WSANAMESPACE_INFOEX","winsock2/WSANAMESPACE_INFOEXA","winsock2/WSANAMESPACE_INFOEXW"]
old-location: winsock\wsanamespace_infoex.htm
tech.root: WinSock
ms.assetid: 3f4a8916-9db9-4b65-982f-4cb4ec2205ed
ms.date: 12/05/2018
ms.keywords: '*LPWSANAMESPACE_INFOEXW, *PWSANAMESPACE_INFOEXW, LPWSANAMESPACE_INFOEX, LPWSANAMESPACE_INFOEX structure pointer [Winsock], NS_BTH, NS_DNS, NS_EMAIL, NS_NLA, NS_NTDS, NS_PNRPCLOUD, NS_PNRPNAME, PWSANAMESPACE_INFOEX, PWSANAMESPACE_INFOEX structure pointer [Winsock], WSANAMESPACE_INFOEX, WSANAMESPACE_INFOEX structure [Winsock], WSANAMESPACE_INFOEXA, WSANAMESPACE_INFOEXW, winsock.wsanamespace_infoex, winsock2/LPWSANAMESPACE_INFOEX, winsock2/PWSANAMESPACE_INFOEX, winsock2/WSANAMESPACE_INFOEX, winsock2/WSANAMESPACE_INFOEXA, winsock2/WSANAMESPACE_INFOEXW'
req.header: winsock2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WSANAMESPACE_INFOEXW (Unicode) and WSANAMESPACE_INFOEXA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WSANAMESPACE_INFOEXW, *PWSANAMESPACE_INFOEXW, *LPWSANAMESPACE_INFOEXW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSANAMESPACE_INFOEXW
 - winsock2/_WSANAMESPACE_INFOEXW
 - PWSANAMESPACE_INFOEXW
 - winsock2/PWSANAMESPACE_INFOEXW
 - WSANAMESPACE_INFOEXW
 - winsock2/WSANAMESPACE_INFOEXW
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
 - WSANAMESPACE_INFOEX
 - WSANAMESPACE_INFOEXA
 - WSANAMESPACE_INFOEXW
---

# WSANAMESPACE_INFOEXW structure


## -description

The 
<b>WSANAMESPACE_INFOEX</b> structure contains all registration information for a namespace provider.

## -struct-fields

### -field NSProviderId

Type: <b>GUID</b>

A unique GUID for this namespace provider.

### -field dwNameSpace

Type: <b>DWORD</b>

The namespace supported by this provider.


Possible values for the <b>dwNameSpace</b> member are listed in the <i>Winsock2.h</i> include file. Several namespace providers are included with Windows Vista and later. Other namespace providers can be installed, so the following possible values  are only those commonly available. Many other values are possible.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NS_BTH"></a><a id="ns_bth"></a><dl>
<dt><b>NS_BTH</b></dt>
</dl>
</td>
<td width="60%">
The Bluetooth namespace. 

This namespace identifier is supported on Windows Vista and later.

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
The email namespace. 

This namespace identifier is supported on Windows Vista and later.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_NLA"></a><a id="ns_nla"></a><dl>
<dt><b>NS_NLA</b></dt>
</dl>
</td>
<td width="60%">
The network location awareness (NLA) namespace. 

This namespace identifier is supported on Windows XP and later.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_NTDS"></a><a id="ns_ntds"></a><dl>
<dt><b>NS_NTDS</b></dt>
</dl>
</td>
<td width="60%">
The Windows NT directory service  (NTDS) namespace. 

</td>
</tr>
<tr>
<td width="40%"><a id="NS_PNRPNAME"></a><a id="ns_pnrpname"></a><dl>
<dt><b>NS_PNRPNAME</b></dt>
</dl>
</td>
<td width="60%">
The peer-to-peer name space for a specific peer name. 

This namespace identifier is supported on Windows Vista and later.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_PNRPCLOUD"></a><a id="ns_pnrpcloud"></a><dl>
<dt><b>NS_PNRPCLOUD</b></dt>
</dl>
</td>
<td width="60%">
The peer-to-peer name space for a collection of peer names. 

This namespace identifier is supported on Windows Vista and later.

</td>
</tr>
</table>

### -field fActive

Type: <b>BOOL</b>

If <b>TRUE</b>, indicates that this namespace provider is active. If <b>FALSE</b>, the namespace provider is inactive and is not accessible for queries, even if the query specifically references this namespace provider.

### -field dwVersion

Type: <b>DWORD</b>

The version number of the namespace provider.

### -field lpszIdentifier

Type: <b>LPTSTR</b>

A display string that identifies the namespace provider.

### -field ProviderSpecific

Type: <b>BLOB</b>

A provider-specific data blob associated with namespace entry.

## -remarks

The <b>WSANAMESPACE_INFOEX</b>  structure is an enhanced version of the <a href="/windows/desktop/api/winsock2/ns-winsock2-wsanamespace_infow">WSANAMESPACE_INFO</a> structure that is used by the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersexa">WSAEnumNameSpaceProvidersEx</a> and the <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumnamespaceprovidersex32">WSCEnumNameSpaceProvidersEx32</a> functions to return information on available namespace providers. The <b>WSANAMESPACE_INFOEX</b>  structure contains the provider-specific data blob associated with the namespace entry
                     passed in the <i>lpProviderInfo</i> parameter to the <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallnamespaceex">WSCInstallNameSpaceEx</a> and <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallnamespaceex32">WSCInstallNameSpaceEx32</a> functions.

  Currently, the only namespace included with Windows that uses information in the <b>ProviderSpecific</b> member of the <b>WSANAMESPACE_INFOEX</b> structure are namespace providers for the NS_EMAIL namespace. The format of the <b>ProviderSpecific</b> member for an NS_EMAIL namespace provider is a <a href="/windows/desktop/api/nsemail/ns-nsemail-napi_provider_installation_blob">NAPI_PROVIDER_INSTALLATION_BLOB</a> structure.

When UNICODE or _UNICODE is defined, <b>WSANAMESPACE_INFOEX</b> is defined to <b>WSANAMESPACE_INFOEXW</b>, the Unicode version of this structure and the <b>lpszIdentifier</b> string member is defined to the  <b>LPWSTR</b> data type.

When UNICODE or _UNICODE is not defined, <b>WSANAMESPACE_INFOEX</b> is defined to <b>WSANAMESPACE_INFOEXA</b>, the ANSI version of this structure and the <b>lpszIdentifier</b> string member is defined to the  <b>LPSTR</b> data type.

The <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumnamespaceprovidersex32">WSCEnumNameSpaceProvidersEx32</a> function is a Unicode only function and returns <b>WSANAMESPACE_INFOEXW</b> structures. 





> [!NOTE]
> The winsock2.h header defines WSANAMESPACE_INFOEX as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/nsemail/ns-nsemail-napi_provider_installation_blob">NAPI_PROVIDER_INSTALLATION_BLOB</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersexa">WSAEnumNameSpaceProvidersEx</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-wsanamespace_infow">WSANAMESPACE_INFO</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumnamespaceprovidersex32">WSCEnumNameSpaceProvidersEx32</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallnamespaceex">WSCInstallNameSpaceEx</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallnamespaceex32">WSCInstallNameSpaceEx32</a>
