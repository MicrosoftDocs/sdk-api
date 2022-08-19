---
UID: NS:iptypes._IP_ADAPTER_UNICAST_ADDRESS_XP
title: IP_ADAPTER_UNICAST_ADDRESS_XP (iptypes.h)
description: The IP_ADAPTER_UNICAST_ADDRESS_XP structure (iptypes.h) stores a single unicast IP address in a linked list of IP addresses for a particular adapter.
helpviewer_keywords: ["*PIP_ADAPTER_UNICAST_ADDRESS","*PIP_ADAPTER_UNICAST_ADDRESS_XP","IP_ADAPTER_ADDRESS_DNS_ELIGIBLE","IP_ADAPTER_ADDRESS_TRANSIENT","IP_ADAPTER_UNICAST_ADDRESS","IP_ADAPTER_UNICAST_ADDRESS structure [IP Helper]","IP_ADAPTER_UNICAST_ADDRESS_LH","IP_ADAPTER_UNICAST_ADDRESS_XP","PIP_ADAPTER_UNICAST_ADDRESS","PIP_ADAPTER_UNICAST_ADDRESS structure pointer [IP Helper]","_iphlp_ip_adapter_unicast_address","iphlp.ip_adapter_unicast_address","iptypes/IP_ADAPTER_UNICAST_ADDRESS","iptypes/PIP_ADAPTER_UNICAST_ADDRESS"]
old-location: iphlp\ip_adapter_unicast_address.htm
tech.root: IpHlp
ms.assetid: 65c3648c-89bd-417b-8a9b-feefa6149c4a
ms.date: 08/12/2022
ms.keywords: '*PIP_ADAPTER_UNICAST_ADDRESS, *PIP_ADAPTER_UNICAST_ADDRESS_XP, IP_ADAPTER_ADDRESS_DNS_ELIGIBLE, IP_ADAPTER_ADDRESS_TRANSIENT, IP_ADAPTER_UNICAST_ADDRESS, IP_ADAPTER_UNICAST_ADDRESS structure [IP Helper], IP_ADAPTER_UNICAST_ADDRESS_LH, IP_ADAPTER_UNICAST_ADDRESS_XP, PIP_ADAPTER_UNICAST_ADDRESS, PIP_ADAPTER_UNICAST_ADDRESS structure pointer [IP Helper], _iphlp_ip_adapter_unicast_address, iphlp.ip_adapter_unicast_address, iptypes/IP_ADAPTER_UNICAST_ADDRESS, iptypes/PIP_ADAPTER_UNICAST_ADDRESS'
req.header: iptypes.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
targetos: Windows
req.typenames: IP_ADAPTER_UNICAST_ADDRESS_XP, *PIP_ADAPTER_UNICAST_ADDRESS_XP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IP_ADAPTER_UNICAST_ADDRESS_XP
 - iptypes/_IP_ADAPTER_UNICAST_ADDRESS_XP
 - PIP_ADAPTER_UNICAST_ADDRESS_XP
 - iptypes/PIP_ADAPTER_UNICAST_ADDRESS_XP
 - IP_ADAPTER_UNICAST_ADDRESS_XP
 - iptypes/IP_ADAPTER_UNICAST_ADDRESS_XP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iptypes.h
api_name:
 - IP_ADAPTER_UNICAST_ADDRESS
---

## -description

The <b>IP_ADAPTER_UNICAST_ADDRESS</b> structure stores a single unicast IP address in a linked list of IP addresses for a particular adapter.

## -struct-fields

### -field Alignment

Type: <b>ULONGLONG</b>

Reserved. Used by the compiler to align the structure.

### -field Length

Type: <b>ULONG</b>

The length, in bytes, of this structure.

### -field Flags

Type: <b>DWORD</b>

A set of flags for this IP address. 

The following table shows possible values. These constants are defined in the <i>Iptypes.h</i> header file. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IP_ADAPTER_ADDRESS_DNS_ELIGIBLE"></a><a id="ip_adapter_address_dns_eligible"></a><dl>
<dt><b>IP_ADAPTER_ADDRESS_DNS_ELIGIBLE</b></dt>
</dl>
</td>
<td width="60%">
The IP address is legal to appear in DNS.

</td>
</tr>
<tr>
<td width="40%"><a id="IP_ADAPTER_ADDRESS_TRANSIENT"></a><a id="ip_adapter_address_transient"></a><dl>
<dt><b>IP_ADAPTER_ADDRESS_TRANSIENT</b></dt>
</dl>
</td>
<td width="60%">
The IP address is a cluster address and should not be used by most applications.

</td>
</tr>
</table>

### -field Next

Type: <b>struct _IP_ADAPTER_UNICAST_ADDRESS*</b>

A pointer to the next IP adapter address structure in the list.

### -field Address

Type: <b><a href="/windows/desktop/api/ws2def/ns-ws2def-socket_address">SOCKET_ADDRESS</a></b>

The IP address for this unicast IP address entry. This member can be an IPv6 address or an IPv4 address.

### -field PrefixOrigin

Type: <b>IP_PREFIX_ORIGIN</b>

The prefix or network part of IP the address. This member can be one of the values from the <a href="/windows/desktop/api/nldef/ne-nldef-nl_prefix_origin">IP_PREFIX_ORIGIN</a> enumeration type defined in the <i>Iptypes.h</i> header file.

### -field SuffixOrigin

Type: <b>IP_SUFFIX_ORIGIN</b>

The suffix or host part of the IP address. This member can be one of the values from the <a href="/windows/desktop/api/nldef/ne-nldef-nl_suffix_origin">IP_SUFFIX_ORIGIN</a> enumeration type defined in the <i>Iptypes.h</i> header file.

### -field DadState

Type: <b>IP_DAD_STATE</b>

The duplicate address detection (DAD) state. This member can be one of the values from the <a href="/windows/desktop/api/nldef/ne-nldef-nl_dad_state">IP_DAD_STATE</a> enumeration type defined in the <i>Iptypes.h</i> header file. 
Duplicate address detection is available for both IPv4 and IPv6 addresses.

### -field ValidLifetime

Type: <b>ULONG</b>

The maximum lifetime, in seconds, that the IP address is valid. A value of 0xffffffff is considered to be infinite.

### -field PreferredLifetime

Type: <b>ULONG</b>

The preferred lifetime, in seconds, that the IP address is valid. A value of 0xffffffff is considered to be infinite.

### -field LeaseLifetime

Type: <b>ULONG</b>

The lease lifetime, in seconds, that the IP address is valid.

## -remarks

The <a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_lh">IP_ADAPTER_ADDRESSES</a> structure is retrieved by the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses">GetAdaptersAddresses</a> function. The <b>FirstUnicastAddress</b> member of the <b>IP_ADAPTER_ADDRESSES</b> structure is a pointer to a linked list of <b>IP_ADAPTER_UNICAST_ADDRESS</b> structures. 

The size of the <b>IP_ADAPTER_UNICAST_ADDRESS</b> structure changed on Windows Vista and later. The <b>Length</b> member should be used to determine which version of the <b>IP_ADAPTER_UNICAST_ADDRESS</b> structure is being used. 

The version of the <b>IP_ADAPTER_UNICAST_ADDRESS</b> structure on Windows Vista and later has the following new member added: <b>OnLinkPrefixLength</b>.

When this structure is used with the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses">GetAdaptersAddresses</a> function and similar management functions, all configured addresses are shown, including duplicate addresses. Such duplicate address entries can occur when addresses are configured statically. Such reporting facilitates administrator troubleshooting. The <b>DadState</b> member is effective in identifying and troubleshooting such situations.

In the Windows SDK, the version of the structure for use on Windows Vista and later is  defined as <b>IP_ADAPTER_UNICAST_ADDRESS_LH</b>. In the Windows SDK, the version of this structure to be used on earlier systems including Windows XP with Service Pack 1 (SP1) and later is defined as <b>IP_ADAPTER_UNICAST_ADDRESS_XP</b>. When compiling an application if the target platform is Windows Vista and later (<code>NTDDI_VERSION &gt;= NTDDI_VISTA</code>, <code>_WIN32_WINNT &gt;= 0x0600</code>, or <code>WINVER &gt;= 0x0600</code>), the <b>IP_ADAPTER_UNICAST_ADDRESS_LH</b> structure is typedefed to the <b>IP_ADAPTER_UNICAST_ADDRESS</b> structure. When compiling an application if the target platform is not Windows Vista and later, the <b>IP_ADAPTER_UNICAST_ADDRESS_XP</b> structure is typedefed to the <b>IP_ADAPTER_UNICAST_ADDRESS</b> structure. 

The <a href="/windows/desktop/api/ws2def/ns-ws2def-socket_address">SOCKET_ADDRESS</a> structure is used in the <b>IP_ADAPTER_UNICAST_ADDRESS</b> structure. On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>SOCKET_ADDRESS</b> structure is defined in the <i>Ws2def.h</i> header file which is automatically included by the <i>Winsock2.h</i> header file. On the Platform Software Development Kit (SDK) released for Windows Server 2003 and Windows XP, the <b>SOCKET_ADDRESS</b> structure is declared in the <i>Winsock2.h</i> header file. In order to use the <b>IP_ADAPTER_UNICAST_ADDRESS</b> structure, the <i>Winsock2.h</i> header file must be included before the <i>Iphlpapi.h</i> header file.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses">GetAdaptersAddresses</a>

<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper
		  Start Page</a>

<a href="/windows/desktop/IpHlp/ip-helper-structures">IP Helper
		  Structures</a>

<a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_lh">IP_ADAPTER_ADDRESSES</a>

<a href="/windows/desktop/api/nldef/ne-nldef-nl_dad_state">IP_DAD_STATE</a>

<a href="/windows/desktop/api/nldef/ne-nldef-nl_prefix_origin">IP_PREFIX_ORIGIN</a>

<a href="/windows/desktop/api/nldef/ne-nldef-nl_suffix_origin">IP_SUFFIX_ORIGIN</a>

<a href="/windows/desktop/api/ws2def/ns-ws2def-socket_address">SOCKET_ADDRESS</a>
