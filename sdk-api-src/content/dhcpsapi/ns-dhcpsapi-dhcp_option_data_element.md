---
UID: NS:dhcpsapi._DHCP_OPTION_DATA_ELEMENT
title: DHCP_OPTION_DATA_ELEMENT (dhcpsapi.h)
description: The DHCP_OPTION_DATA_ELEMENT structure defines a data element present (either singly or as a member of an array) within a DHCP_OPTION_DATA structure.
helpviewer_keywords: ["*LPDHCP_OPTION_DATA_ELEMENT","DHCP_OPTION_DATA_ELEMENT","DHCP_OPTION_DATA_ELEMENT structure [DHCP]","LPDHCP_OPTION_DATA_ELEMENT","LPDHCP_OPTION_DATA_ELEMENT structure pointer [DHCP]","dhcp.dhcp_option_data_element","dhcpsapi/LPDHCP_OPTION_DATA_ELEMENT","dhcpsapi/_DHCP_OPTION_DATA_ELEMENT"]
old-location: dhcp\dhcp_option_data_element.htm
tech.root: DHCP
ms.assetid: 2ffc8968-f903-4d8e-8b34-c8031a56ebfc
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_OPTION_DATA_ELEMENT, DHCP_OPTION_DATA_ELEMENT, DHCP_OPTION_DATA_ELEMENT structure [DHCP], LPDHCP_OPTION_DATA_ELEMENT, LPDHCP_OPTION_DATA_ELEMENT structure pointer [DHCP], dhcp.dhcp_option_data_element, dhcpsapi/LPDHCP_OPTION_DATA_ELEMENT, dhcpsapi/_DHCP_OPTION_DATA_ELEMENT'
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
req.typenames: DHCP_OPTION_DATA_ELEMENT, *LPDHCP_OPTION_DATA_ELEMENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_OPTION_DATA_ELEMENT
 - dhcpsapi/_DHCP_OPTION_DATA_ELEMENT
 - LPDHCP_OPTION_DATA_ELEMENT
 - dhcpsapi/LPDHCP_OPTION_DATA_ELEMENT
 - DHCP_OPTION_DATA_ELEMENT
 - dhcpsapi/DHCP_OPTION_DATA_ELEMENT
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
 - DHCP_OPTION_DATA_ELEMENT
---

# DHCP_OPTION_DATA_ELEMENT structure


## -description

The <b>DHCP_OPTION_DATA_ELEMENT</b> structure defines a data element present (either singly or as a member of an array) within a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_data">DHCP_OPTION_DATA</a> structure.

## -struct-fields

### -field OptionType

A <a href="/windows/desktop/api/dhcpsapi/ne-dhcpsapi-dhcp_option_data_type">DHCP_OPTION_DATA_TYPE</a> enumeration value that indicates the type of data that is present in the subsequent field, <b>Element</b>.

### -field Element.ByteOption.case

### -field Element.ByteOption.case.DhcpByteOption

### -field Element.WordOption.case

### -field Element.WordOption.case.DhcpWordOption

### -field Element.DWordOption.case

### -field Element.DWordOption.case.DhcpDWordOption

### -field Element.DWordDWordOption.case

### -field Element.DWordDWordOption.case.DhcpDWordDWordOption

### -field Element.IpAddressOption.case

### -field Element.IpAddressOption.case.DhcpIpAddressOption

### -field Element.StringDataOption.case

### -field Element.StringDataOption.case.DhcpStringDataOption

### -field Element.BinaryDataOption.case

### -field Element.BinaryDataOption.case.DhcpBinaryDataOption

### -field Element.EncapsulatedDataOption.case

### -field Element.EncapsulatedDataOption.case.DhcpEncapsulatedDataOption

### -field Element.Ipv6AddressDataOption.case

### -field Element.Ipv6AddressDataOption.case.DhcpIpv6AddressOption





### -field Element

### -field Element.ByteOption

Specifies the data as a BYTE  value. This field will be present if the <b>OptionType</b> is <b>DhcpByteOption</b>.

### -field Element.WordOption

Specifies the data as a WORD value. This field will be present if the <b>OptionType</b> is <b>DhcpWordOption</b>.

### -field Element.DWordOption

Specifies the data as a DWORD value. This field will be present if the <b>OptionType</b> is <b>DhcpDWordOption</b>.

### -field Element.DWordDWordOption

Specifies the data as a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dword_dword">DWORD_DWORD</a> value. This field will be present if the <b>OptionType</b> is <b>DhcpDWordDWordOption</b>.

### -field Element.IpAddressOption

Specifies the data as a <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> (DWORD) value. This field will be present if the <b>OptionType</b> is <b>IpAddressOption</b>.

### -field Element.StringDataOption

Specifies the data as a Unicode string  value. This field will be present if the <b>OptionType</b> is <b>DhcpStringDataOption</b>.

### -field Element.BinaryDataOption

Specifies the data as a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_binary_data">DHCP_BINARY_DATA</a> structure. This field will be present if the <b>OptionType</b> is <b>DhcpBinaryDataOption</b>.

### -field Element.EncapsulatedDataOption

Specifies the data as encapsulated within a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_binary_data">DHCP_BINARY_DATA</a> structure. The application must know the format of the opaque data capsule in order to read it from the <b>Data</b> field of <b>DHCP_BINARY_DATA</b>. This field will be present if the <b>OptionType</b> is <b>DhcpEncapsulatedDataOption</b>.

### -field Element.Ipv6AddressDataOption

Specifies the data as a Unicode string value. This field will be present if the <b>OptionType</b> is <b>DhcpIpv6AddressOption</b>.

### -field _DHCP_OPTION_ELEMENT_UNION

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_binary_data">DHCP_BINARY_DATA</a>



<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_data">DHCP_OPTION_DATA</a>



<a href="/windows/desktop/api/dhcpsapi/ne-dhcpsapi-dhcp_option_data_type">DHCP_OPTION_DATA_TYPE</a>



<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dword_dword">DWORD_DWORD</a>