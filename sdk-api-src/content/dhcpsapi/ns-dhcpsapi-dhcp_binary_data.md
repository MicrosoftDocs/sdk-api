---
UID: NS:dhcpsapi._DHCP_BINARY_DATA
title: DHCP_BINARY_DATA (dhcpsapi.h)
description: The DHCP_BINARY_DATA structure defines an opaque blob of binary data.
helpviewer_keywords: ["*LPDHCP_BINARY_DATA","DHCP_BINARY_DATA","DHCP_BINARY_DATA structure [DHCP]","DHCP_CLIENT_UID","DHCP_CLIENT_UID structure [DHCP]","LPDHCP_BINARY_DATA","LPDHCP_BINARY_DATA structure pointer [DHCP]","dhcp.dhcp_binary_data","dhcpsapi/DHCP_CLIENT_UID","dhcpsapi/LPDHCP_BINARY_DATA","dhcpsapi/_DHCP_BINARY_DATA"]
old-location: dhcp\dhcp_binary_data.htm
tech.root: DHCP
ms.assetid: 0afdddb4-12f9-4c0b-937a-2cc311c126b4
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_BINARY_DATA, DHCP_BINARY_DATA, DHCP_BINARY_DATA structure [DHCP], DHCP_CLIENT_UID, DHCP_CLIENT_UID structure [DHCP], LPDHCP_BINARY_DATA, LPDHCP_BINARY_DATA structure pointer [DHCP], dhcp.dhcp_binary_data, dhcpsapi/DHCP_CLIENT_UID, dhcpsapi/LPDHCP_BINARY_DATA, dhcpsapi/_DHCP_BINARY_DATA'
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
req.typenames: DHCP_BINARY_DATA, *LPDHCP_BINARY_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_BINARY_DATA
 - dhcpsapi/_DHCP_BINARY_DATA
 - LPDHCP_BINARY_DATA
 - dhcpsapi/LPDHCP_BINARY_DATA
 - DHCP_BINARY_DATA
 - dhcpsapi/DHCP_BINARY_DATA
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
 - DHCP_BINARY_DATA
---

# DHCP_BINARY_DATA structure


## -description

The <b>DHCP_BINARY_DATA</b> structure defines an opaque blob of binary data.

## -struct-fields

### -field DataLength

Specifies the size of <b>Data</b>, in bytes.

### -field Data

Pointer to an opaque blob of byte (binary) data.

The data is formatted as follows:

<table>
<tr>
<th>Byte</th>
<th>Format</th>
</tr>
<tr>
<td>Byte 0 to byte 3 </td>
<td>The result of a binary AND on the IP address and the subnet mask in reverse order.</td>
</tr>
<tr>
<td>Byte 4</td>
<td>Hardware identifier. This value is always 0x01.</td>
</tr>
<tr>
<td>Byte 5 to Byte 10 </td>
<td>The MAC address of the client.</td>
</tr>
</table>

### -field Data.size_is

### -field Data.size_is.DataLength

