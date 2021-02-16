---
UID: NS:dhcpsapi._DHCP_BIND_ELEMENT
title: DHCP_BIND_ELEMENT (dhcpsapi.h)
description: Defines an individual network binding for the DHCP server. A single DHCP server can contain multiple bindings and serve multiple networks.
helpviewer_keywords: ["*LPDHCP_BIND_ELEMENT","DHCP_BIND_ELEMENT","DHCP_BIND_ELEMENT structure [DHCP]","DHCP_ENDPOINT_FLAG_CANT_MODIFY","LPDHCP_BIND_ELEMENT","LPDHCP_BIND_ELEMENT structure pointer [DHCP]","dhcp.dhcp_bind_element","dhcpsapi/LPDHCP_BIND_ELEMENT","dhcpsapi/_DHCP_BIND_ELEMENT"]
old-location: dhcp\dhcp_bind_element.htm
tech.root: DHCP
ms.assetid: 00d9d23e-fb39-4f3c-a2b9-9983322879fd
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_BIND_ELEMENT, DHCP_BIND_ELEMENT, DHCP_BIND_ELEMENT structure [DHCP], DHCP_ENDPOINT_FLAG_CANT_MODIFY, LPDHCP_BIND_ELEMENT, LPDHCP_BIND_ELEMENT structure pointer [DHCP], dhcp.dhcp_bind_element, dhcpsapi/LPDHCP_BIND_ELEMENT, dhcpsapi/_DHCP_BIND_ELEMENT'
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
req.typenames: DHCP_BIND_ELEMENT, *LPDHCP_BIND_ELEMENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_BIND_ELEMENT
 - dhcpsapi/_DHCP_BIND_ELEMENT
 - LPDHCP_BIND_ELEMENT
 - dhcpsapi/LPDHCP_BIND_ELEMENT
 - DHCP_BIND_ELEMENT
 - dhcpsapi/DHCP_BIND_ELEMENT
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
 - DHCP_BIND_ELEMENT
---

# DHCP_BIND_ELEMENT structure


## -description

The <b>DHCP_BIND_ELEMENT</b> structure defines an individual network binding for the DHCP server. A single DHCP server can contain multiple bindings and serve multiple networks.

## -struct-fields

### -field Flags

Specifies a set of bit flags indicating properties of the network binding.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DHCP_ENDPOINT_FLAG_CANT_MODIFY"></a><a id="dhcp_endpoint_flag_cant_modify"></a><dl>
<dt><b>DHCP_ENDPOINT_FLAG_CANT_MODIFY</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
The binding specified in this structure cannot be modified.

</td>
</tr>
</table>

### -field fBoundToDHCPServer

Specifies whether or not this binding is set on the DHCP server. If <b>TRUE</b>, the binding is set; if <b>FALSE</b>, it is not.

### -field AdapterPrimaryAddress

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> value that specifies the IP address assigned to the ethernet adapter of the DHCP server.

### -field AdapterSubnetAddress

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> value that specifies the subnet IP mask used by this ethernet adapter.

### -field IfDescription

Unicode string that specifies the name assigned to this network interface device.

### -field IfIdSize

Specifies the size of the network interface device ID, in bytes.

### -field IfId

Specifies the network interface device ID.

### -field IfId.size_is

### -field IfId.size_is.IfIdSize

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_bind_element_array">DHCP_BIND_ELEMENT_ARRAY</a>