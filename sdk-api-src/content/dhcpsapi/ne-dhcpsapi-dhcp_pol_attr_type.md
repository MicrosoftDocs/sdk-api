---
UID: NE:dhcpsapi.DHCP_POL_ATTR_TYPE
title: DHCP_POL_ATTR_TYPE (dhcpsapi.h)
description: The DHCP_POL_ATTR_TYPE enumeration defines the attribute type for a condition in a DHCP server policy.
helpviewer_keywords: ["DHCP_POL_ATTR_TYPE","DHCP_POL_ATTR_TYPE enumeration [DHCP]","DhcpAttrHWAddr","DhcpAttrOption","DhcpAttrSubOption","dhcp.dhcp_pol_attr_type","dhcpsapi/DHCP_POL_ATTR_TYPE","dhcpsapi/DhcpAttrHWAddr","dhcpsapi/DhcpAttrOption","dhcpsapi/DhcpAttrSubOption"]
old-location: dhcp\dhcp_pol_attr_type.htm
tech.root: DHCP
ms.assetid: 02a84c55-402c-40fe-8dad-6ed3f58052a1
ms.date: 12/05/2018
ms.keywords: DHCP_POL_ATTR_TYPE, DHCP_POL_ATTR_TYPE enumeration [DHCP], DhcpAttrHWAddr, DhcpAttrOption, DhcpAttrSubOption, dhcp.dhcp_pol_attr_type, dhcpsapi/DHCP_POL_ATTR_TYPE, dhcpsapi/DhcpAttrHWAddr, dhcpsapi/DhcpAttrOption, dhcpsapi/DhcpAttrSubOption
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: DHCP_POL_ATTR_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DHCP_POL_ATTR_TYPE
 - dhcpsapi/DHCP_POL_ATTR_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dhcpsapi.h
api_name:
 - DHCP_POL_ATTR_TYPE
---

# DHCP_POL_ATTR_TYPE enumeration


## -description

The <b>DHCP_POL_ATTR_TYPE</b> enumeration defines the attribute type for a condition in a DHCP server policy.

## -enum-fields

### -field DhcpAttrHWAddr

The condition is based on the hardware address (MAC address) present in the <b>chaddr</b> field of the DHCP message header as defined in <a href="http://www.ietf.org/rfc/rfc2131.txt">RFC2131</a>.

### -field DhcpAttrOption

The condition is based on a DHCP option.

### -field DhcpAttrSubOption

The condition is based on a DHCP sub-option

### -field DhcpAttrFqdn

### -field DhcpAttrFqdnSingleLabel

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_pol_cond">DHCP_POL_COND</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlpraddv4policycondition">DhcpHlprAddV4PolicyCondition</a>

