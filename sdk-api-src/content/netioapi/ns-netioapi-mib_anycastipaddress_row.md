---
UID: NS:netioapi._MIB_ANYCASTIPADDRESS_ROW
title: MIB_ANYCASTIPADDRESS_ROW (netioapi.h)
description: Stores information about an anycast IP address.
helpviewer_keywords: ["*PMIB_ANYCASTIPADDRESS_ROW","MIB_ANYCASTIPADDRESS_ROW","MIB_ANYCASTIPADDRESS_ROW structure [MIB]","PMIB_ANYCASTIPADDRESS_ROW","PMIB_ANYCASTIPADDRESS_ROW structure pointer [MIB]","_MIB_ANYCASTIPADDRESS_ROW","mib.mib_anycastipaddress_row","netioapi/MIB_ANYCASTIPADDRESS_ROW","netioapi/PMIB_ANYCASTIPADDRESS_ROW"]
old-location: mib\mib_anycastipaddress_row.htm
tech.root: MIB
ms.assetid: bdbe43b8-88aa-48af-aa6b-c88c4e8e404e
ms.date: 12/05/2018
ms.keywords: '*PMIB_ANYCASTIPADDRESS_ROW, MIB_ANYCASTIPADDRESS_ROW, MIB_ANYCASTIPADDRESS_ROW structure [MIB], PMIB_ANYCASTIPADDRESS_ROW, PMIB_ANYCASTIPADDRESS_ROW structure pointer [MIB], _MIB_ANYCASTIPADDRESS_ROW, mib.mib_anycastipaddress_row, netioapi/MIB_ANYCASTIPADDRESS_ROW, netioapi/PMIB_ANYCASTIPADDRESS_ROW'
req.header: netioapi.h
req.include-header: Iphlpapi.h
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
req.typenames: MIB_ANYCASTIPADDRESS_ROW, *PMIB_ANYCASTIPADDRESS_ROW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_ANYCASTIPADDRESS_ROW
 - netioapi/_MIB_ANYCASTIPADDRESS_ROW
 - PMIB_ANYCASTIPADDRESS_ROW
 - netioapi/PMIB_ANYCASTIPADDRESS_ROW
 - MIB_ANYCASTIPADDRESS_ROW
 - netioapi/MIB_ANYCASTIPADDRESS_ROW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Netioapi.h
api_name:
 - MIB_ANYCASTIPADDRESS_ROW
---

# MIB_ANYCASTIPADDRESS_ROW structure


## -description

The 
<b>MIB_ANYCASTIPADDRESS_ROW</b> structure stores information about an anycast IP address.

## -struct-fields

### -field Address

The anycast IP address. This member can be an IPv6 address or an IPv4 address.

### -field InterfaceLuid

The locally unique identifier (LUID) for the network interface associated with this IP address.

### -field InterfaceIndex

The local index value for the network interface associated with this IP address. This index value may change when a network adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent.

### -field ScopeId

The scope ID of the anycast IP address. This member is applicable only to an IPv6 address. This member cannot be set. It is automatically determined by the interface on which the address was added.

## -remarks

The <b>MIB_ANYCASTIPADDRESS_ROW</b> structure is defined on Windows Vista and later. 

Note that the <i>Netioapi.h</i> header file is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Netioapi.h</i> header file should never be used directly.

## -see-also

<a href="/windows/desktop/api/netioapi/nf-netioapi-createanycastipaddressentry">CreateAnycastIpAddressEntry</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-deleteanycastipaddressentry">DeleteAnycastIpAddressEntry</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getanycastipaddressentry">GetAnycastIpAddressEntry</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getanycastipaddresstable">GetAnycastIpAddressTable</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_anycastipaddress_table">MIB_ANYCASTIPADDRESS_TABLE</a>



<a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-sockaddr_inet">SOCKADDR_INET</a>