---
UID: NS:dhcpsapi._SCOPE_MIB_INFO
title: SCOPE_MIB_INFO (dhcpsapi.h)
description: Defines information about an available scope for use within returned DHCP-specific SNMP Management Information Block (MIB) data.
helpviewer_keywords: ["*LPSCOPE_MIB_INFO","LPSCOPE_MIB_INFO","LPSCOPE_MIB_INFO structure pointer [DHCP]","SCOPE_MIB_INFO","SCOPE_MIB_INFO structure [DHCP]","dhcp.scope_mib_info","dhcpsapi/LPSCOPE_MIB_INFO","dhcpsapi/_SCOPE_MIB_INFO"]
old-location: dhcp\scope_mib_info.htm
tech.root: DHCP
ms.assetid: 54f54734-3e4a-489f-a61d-85fd436d28ad
ms.date: 12/05/2018
ms.keywords: '*LPSCOPE_MIB_INFO, LPSCOPE_MIB_INFO, LPSCOPE_MIB_INFO structure pointer [DHCP], SCOPE_MIB_INFO, SCOPE_MIB_INFO structure [DHCP], dhcp.scope_mib_info, dhcpsapi/LPSCOPE_MIB_INFO, dhcpsapi/_SCOPE_MIB_INFO'
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: SCOPE_MIB_INFO, *LPSCOPE_MIB_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SCOPE_MIB_INFO
 - dhcpsapi/_SCOPE_MIB_INFO
 - LPSCOPE_MIB_INFO
 - dhcpsapi/LPSCOPE_MIB_INFO
 - SCOPE_MIB_INFO
 - dhcpsapi/SCOPE_MIB_INFO
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
 - SCOPE_MIB_INFO
---

# SCOPE_MIB_INFO structure


## -description

The <b>SCOPE_MIB_INFO</b> structure defines information about an available scope for use within returned DHCP-specific SNMP Management Information Block (MIB) data.

## -struct-fields

### -field Subnet

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> value that specifies the subnet mask for this scope.

### -field NumAddressesInuse

Contains the number of IP addresses currently in use for this scope.

### -field NumAddressesFree

Contains the number of IP addresses currently available for this scope.

### -field NumPendingOffers

Contains the number of IP addresses currently in the offer state for this scope.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_mib_info">DHCP_MIB_INFO</a>



<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_mib_info_v6">DHCP_MIB_INFO_V6</a>