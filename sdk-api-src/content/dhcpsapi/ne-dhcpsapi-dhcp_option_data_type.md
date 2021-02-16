---
UID: NE:dhcpsapi._DHCP_OPTION_DATA_TYPE
title: DHCP_OPTION_DATA_TYPE (dhcpsapi.h)
description: The DHCP_OPTION_DATA_TYPE enumeration defines the set of formats that represent DHCP option data.
helpviewer_keywords: ["*LPDHCP_OPTION_DATA_TYPE","DHCP_OPTION_DATA_TYPE","DHCP_OPTION_DATA_TYPE enumeration [DHCP]","DhcpBinaryDataOption","DhcpByteOption","DhcpDWordDWordOption","DhcpDWordOption","DhcpEncapsulatedDataOption","DhcpIpAddressOption","DhcpIpv6AddressOption","DhcpStringDataOption","DhcpWordOption","LPDHCP_OPTION_DATA_TYPE","LPDHCP_OPTION_DATA_TYPE enumeration pointer [DHCP]","dhcp.dhcp_option_data_type","dhcpsapi/DHCP_OPTION_DATA_TYPE","dhcpsapi/DhcpBinaryDataOption","dhcpsapi/DhcpByteOption","dhcpsapi/DhcpDWordDWordOption","dhcpsapi/DhcpDWordOption","dhcpsapi/DhcpEncapsulatedDataOption","dhcpsapi/DhcpIpAddressOption","dhcpsapi/DhcpIpv6AddressOption","dhcpsapi/DhcpStringDataOption","dhcpsapi/DhcpWordOption","dhcpsapi/LPDHCP_OPTION_DATA_TYPE"]
old-location: dhcp\dhcp_option_data_type.htm
tech.root: DHCP
ms.assetid: 1f215915-07f0-4327-bb42-d5af09cd07c5
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_OPTION_DATA_TYPE, DHCP_OPTION_DATA_TYPE, DHCP_OPTION_DATA_TYPE enumeration [DHCP], DhcpBinaryDataOption, DhcpByteOption, DhcpDWordDWordOption, DhcpDWordOption, DhcpEncapsulatedDataOption, DhcpIpAddressOption, DhcpIpv6AddressOption, DhcpStringDataOption, DhcpWordOption, LPDHCP_OPTION_DATA_TYPE, LPDHCP_OPTION_DATA_TYPE enumeration pointer [DHCP], dhcp.dhcp_option_data_type, dhcpsapi/DHCP_OPTION_DATA_TYPE, dhcpsapi/DhcpBinaryDataOption, dhcpsapi/DhcpByteOption, dhcpsapi/DhcpDWordDWordOption, dhcpsapi/DhcpDWordOption, dhcpsapi/DhcpEncapsulatedDataOption, dhcpsapi/DhcpIpAddressOption, dhcpsapi/DhcpIpv6AddressOption, dhcpsapi/DhcpStringDataOption, dhcpsapi/DhcpWordOption, dhcpsapi/LPDHCP_OPTION_DATA_TYPE'
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DHCP_OPTION_DATA_TYPE, *LPDHCP_OPTION_DATA_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_OPTION_DATA_TYPE
 - dhcpsapi/_DHCP_OPTION_DATA_TYPE
 - LPDHCP_OPTION_DATA_TYPE
 - dhcpsapi/LPDHCP_OPTION_DATA_TYPE
 - DHCP_OPTION_DATA_TYPE
 - dhcpsapi/DHCP_OPTION_DATA_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpsapi.h
api_name:
 - DHCP_OPTION_DATA_TYPE
---

# DHCP_OPTION_DATA_TYPE enumeration


## -description

The <b>DHCP_OPTION_DATA_TYPE</b> enumeration defines the set of formats that represent DHCP  option data.

## -enum-fields

### -field DhcpByteOption

The option data is stored as a BYTE value.

### -field DhcpWordOption

The option data is stored as a WORD value.

### -field DhcpDWordOption

The option data is stored as a DWORD value.

### -field DhcpDWordDWordOption

The option data is stored as a DWORD_DWORD value.

### -field DhcpIpAddressOption

The option data is an IP address, stored as a <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> value (DWORD).

### -field DhcpStringDataOption

The option data is stored as a Unicode string.

### -field DhcpBinaryDataOption

The option data is stored as a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_binary_data">DHCP_BINARY_DATA</a> structure.

### -field DhcpEncapsulatedDataOption

The option data is encapsulated and stored as a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_binary_data">DHCP_BINARY_DATA</a> structure.

### -field DhcpIpv6AddressOption

The option data is stored as a Unicode string.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_binary_data">DHCP_BINARY_DATA</a>