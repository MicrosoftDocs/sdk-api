---
UID: NS:iphlpapi.NET_ADDRESS_INFO_
title: NET_ADDRESS_INFO (iphlpapi.h)
description: Contains IP address information returned by the ParseNetworkString function.
helpviewer_keywords: ["*PNET_ADDRESS_INFO","NET_ADDRESS_INFO","NET_ADDRESS_INFO structure [IP Helper]","NET_ADDRESS_INFO_","PNET_ADDRESS_INFO","PNET_ADDRESS_INFO structure pointer [IP Helper]","iphlp.net_address_info","iphlpapi/NET_ADDRESS_INFO","iphlpapi/PNET_ADDRESS_INFO"]
old-location: iphlp\net_address_info.htm
tech.root: IpHlp
ms.assetid: 1a59cc13-a3fc-4489-aafd-444a96d9a339
ms.date: 12/05/2018
ms.keywords: '*PNET_ADDRESS_INFO, NET_ADDRESS_INFO, NET_ADDRESS_INFO structure [IP Helper], NET_ADDRESS_INFO_, PNET_ADDRESS_INFO, PNET_ADDRESS_INFO structure pointer [IP Helper], iphlp.net_address_info, iphlpapi/NET_ADDRESS_INFO, iphlpapi/PNET_ADDRESS_INFO'
req.header: iphlpapi.h
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
targetos: Windows
req.typenames: NET_ADDRESS_INFO, *PNET_ADDRESS_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NET_ADDRESS_INFO_
 - iphlpapi/NET_ADDRESS_INFO_
 - PNET_ADDRESS_INFO
 - iphlpapi/PNET_ADDRESS_INFO
 - NET_ADDRESS_INFO
 - iphlpapi/NET_ADDRESS_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iphlpapi.h
api_name:
 - NET_ADDRESS_INFO
---

# NET_ADDRESS_INFO structure


## -description

The <b>NET_ADDRESS_INFO</b> structure contains IP address information returned by the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-parsenetworkstring">ParseNetworkString</a> function.

## -struct-fields

### -field Format

Type: <b>NET_ADDRESS_FORMAT</b>

The format of the network address in the union in this structure. This member is an enumeration value from the [NET_ADDRESS_FORMAT](/windows/desktop/api/iphlpapi/ne-iphlpapi-net_address_format) enumeration declared in the <i>Iphlpapi.h</i> header file.

### -field NamedAddress

A DNS named address and port.

### -field NamedAddress.Address

Type: <b>WCHAR[DNS_MAX_NAME_BUFFER_LENGTH]</b>

A DNS name formatted as a <b>NULL</b>-terminated wide character string. The maximum length of this string is the <b>DNS_MAX_NAME_BUFFER_LENGTH</b> constant defined in the <i>Windns.h</i> header file.

### -field NamedAddress.Port

Type: <b>WCHAR[6]</b>

The network port formatted as a <b>NULL</b>-terminated wide character string.

### -field Ipv4Address

Type: <b>SOCKADDR_IN</b>

An IPv4 address represented as a <a href="/windows/desktop/WinSock/sockaddr-2">SOCKADDR_IN</a> structure.

### -field Ipv6Address

Type: <b>SOCKADDR_IN6</b>

An IPv6 address represented as a <a href="/windows/desktop/WinSock/sockaddr-2">SOCKADDR_IN6</a> structure.

### -field IpAddress

Type: <b>SOCKADDR</b>

An IPv4 or IPv6 address represented as a <a href="/windows/desktop/WinSock/sockaddr-2">SOCKADDR</a> structure.

## -remarks

The <b>NET_ADDRESS_INFO</b> structure is defined on Windows Vista and later. 

The <b>NET_ADDRESS_INFO</b> structure is returned by the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-parsenetworkstring">ParseNetworkString</a> function. 

The <a href="/windows/desktop/WinSock/sockaddr-2">SOCKADDR_IN</a>,  SOCKADDR_IN6, and  SOCKADDR structures are used in the <b>NET_ADDRESS_INFO</b> structure. The SOCKADDR_IN and SOCKADDR structures are defined in the  <i>Ws2def.h</i> header file which is automatically included by the <i>Winsock2.h</i> header file. The SOCKADDR_IN6 structure is defined in the <i>Ws2ipdef.h</i> header file which is automatically included by the <i>Ws2tcpip.h</i> header file. In order to use the <b>NET_ADDRESS_INFO</b> structure, the <i>Winsock2.h</i> and <i>Ws2tcpip.h</i> header files must be included before the <i>Iphlpapi.h</i> header file.

## -see-also

[NET_ADDRESS_FORMAT](/windows/desktop/api/iphlpapi/ne-iphlpapi-net_address_format)



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-parsenetworkstring">ParseNetworkString</a>



<a href="/windows/desktop/WinSock/sockaddr-2">SOCKADDR</a>