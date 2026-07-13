---
UID: NS:winsock2._WSANAMESPACE_INFOA
title: WSANAMESPACE_INFOA (winsock2.h)
description: Contains all registration information for a namespace provider. (WSANAMESPACE_INFOA)
helpviewer_keywords: ["*LPWSANAMESPACE_INFOA","*PWSANAMESPACE_INFOA","NS_BTH","NS_DNS","NS_EMAIL","NS_NLA","NS_NTDS","NS_PNRPCLOUD","NS_PNRPNAME","PWSANAMESPACE_INFO","PWSANAMESPACE_INFO structure pointer [Winsock]","WSANAMESPACE_INFO","WSANAMESPACE_INFO structure [Winsock]","WSANAMESPACE_INFOA","WSANAMESPACE_INFOW","_win32_wsanamespace_info_2","winsock.wsanamespace_info_2","winsock2/PWSANAMESPACE_INFO","winsock2/WSANAMESPACE_INFO","winsock2/WSANAMESPACE_INFOA","winsock2/WSANAMESPACE_INFOW"]
old-location: winsock\wsanamespace_info_2.htm
tech.root: WinSock
ms.assetid: a5c76657-df62-471a-95e9-8017cad47b00
ms.date: 12/05/2018
ms.keywords: '*LPWSANAMESPACE_INFOA, *PWSANAMESPACE_INFOA, NS_BTH, NS_DNS, NS_EMAIL, NS_NLA, NS_NTDS, NS_PNRPCLOUD, NS_PNRPNAME, PWSANAMESPACE_INFO, PWSANAMESPACE_INFO structure pointer [Winsock], WSANAMESPACE_INFO, WSANAMESPACE_INFO structure [Winsock], WSANAMESPACE_INFOA, WSANAMESPACE_INFOW, _win32_wsanamespace_info_2, winsock.wsanamespace_info_2, winsock2/PWSANAMESPACE_INFO, winsock2/WSANAMESPACE_INFO, winsock2/WSANAMESPACE_INFOA, winsock2/WSANAMESPACE_INFOW'
req.header: winsock2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WSANAMESPACE_INFOW (Unicode) and WSANAMESPACE_INFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WSANAMESPACE_INFOA, *PWSANAMESPACE_INFOA, *LPWSANAMESPACE_INFOA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSANAMESPACE_INFOA
 - winsock2/_WSANAMESPACE_INFOA
 - PWSANAMESPACE_INFOA
 - winsock2/PWSANAMESPACE_INFOA
 - WSANAMESPACE_INFOA
 - winsock2/WSANAMESPACE_INFOA
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
 - WSANAMESPACE_INFO
 - WSANAMESPACE_INFOA
 - WSANAMESPACE_INFOW
---

# WSANAMESPACE_INFOA structure


## -description

The 
<b>WSANAMESPACE_INFO</b> structure contains all registration information for a namespace provider.

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

## -remarks

The <b>WSANAMESPACE_INFO</b> structure is used by the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersa">WSAEnumNameSpaceProviders</a> and <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumnamespaceproviders32">WSCEnumNameSpaceProviders32</a> functions to return information on available namespace providers. The <b>WSANAMESPACE_INFO</b>  structure contains the provider-specific information on the namespace entry
                     passed to the <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallnamespace">WSCInstallNameSpace</a> and <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallnamespace32">WSCInstallNameSpace32</a> functions when the namespace provider was installed.

When UNICODE or _UNICODE is defined, <b>WSANAMESPACE_INFO</b> is defined to <b>WSANAMESPACE_INFOW</b>, the Unicode version of this data structure and the <b>lpszIdentifier</b> string member is defined to the  <b>LPWSTR</b> data type.

When UNICODE or _UNICODE is not defined, <b>WSANAMESPACE_INFO</b> is defined to <b>WSANAMESPACE_INFOA</b>, the ANSI version of this data structure and the <b>lpszIdentifier</b> string member is defined to the  <b>LPSTR</b> data type.

On Windows Vista and later, <a href="/windows/desktop/api/winsock2/ns-winsock2-wsanamespace_infoexw">WSANAMESPACE_INFOEX</a>, an enhanced version of the <b>WSANAMESPACE_INFO</b> structure, is returned by calls to the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersexa">WSAEnumNameSpaceProvidersEx</a> and <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumnamespaceprovidersex32">WSCEnumNameSpaceProvidersEx32</a> functions





> [!NOTE]
> The winsock2.h header defines WSANAMESPACE_INFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersa">WSAEnumNameSpaceProviders</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersexa">WSAEnumNameSpaceProvidersEx</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-wsanamespace_infoexw">WSANAMESPACE_INFOEX</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumnamespaceproviders32">WSCEnumNameSpaceProviders32</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumnamespaceprovidersex32">WSCEnumNameSpaceProvidersEx32</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallnamespace">WSCInstallNameSpace</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallnamespace32">WSCInstallNameSpace32</a>
