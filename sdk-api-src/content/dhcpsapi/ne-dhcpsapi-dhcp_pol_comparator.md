---
UID: NE:dhcpsapi.DHCP_POL_COMPARATOR
title: DHCP_POL_COMPARATOR (dhcpsapi.h)
description: The DHCP_POL_COMPARATOR enumeration defines the comparison operator for a condition when building a DHCP server policy.
helpviewer_keywords: ["DHCP_POL_COMPARATOR","DHCP_POL_COMPARATOR enumeration [DHCP]","DhcpCompBeginsWith","DhcpCompEqual","DhcpCompNotBeginWith","DhcpCompNotEqual","dhcp.dhcp_pol_comparator","dhcpsapi/DHCP_POL_COMPARATOR","dhcpsapi/DhcpCompBeginsWith","dhcpsapi/DhcpCompEqual","dhcpsapi/DhcpCompNotBeginWith","dhcpsapi/DhcpCompNotEqual"]
old-location: dhcp\dhcp_pol_comparator.htm
tech.root: DHCP
ms.assetid: 7b34e9ec-a3c6-4b85-bb36-d4f834912a64
ms.date: 12/05/2018
ms.keywords: DHCP_POL_COMPARATOR, DHCP_POL_COMPARATOR enumeration [DHCP], DhcpCompBeginsWith, DhcpCompEqual, DhcpCompNotBeginWith, DhcpCompNotEqual, dhcp.dhcp_pol_comparator, dhcpsapi/DHCP_POL_COMPARATOR, dhcpsapi/DhcpCompBeginsWith, dhcpsapi/DhcpCompEqual, dhcpsapi/DhcpCompNotBeginWith, dhcpsapi/DhcpCompNotEqual
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
req.typenames: DHCP_POL_COMPARATOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DHCP_POL_COMPARATOR
 - dhcpsapi/DHCP_POL_COMPARATOR
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
 - DHCP_POL_COMPARATOR
---

# DHCP_POL_COMPARATOR enumeration


## -description

The <b>DHCP_POL_COMPARATOR</b> enumeration defines the comparison operator for a condition when building a DHCP server policy.

## -enum-fields

### -field DhcpCompEqual

The DHCP client message field specified by the criterion must exactly match the value supplied in the condition.

### -field DhcpCompNotEqual

The DHCP client message field specified by the criterion must not exactly match the value supplied in the condition.

### -field DhcpCompBeginsWith

The DHCP client message field specified by the criterion must begin with the value supplied in the condition.

### -field DhcpCompNotBeginWith

The DHCP client message field specified by the criterion must not begin with the value supplied in the condition.

### -field DhcpCompEndsWith

### -field DhcpCompNotEndWith

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_pol_cond">DHCP_POL_COND</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlpraddv4policycondition">DhcpHlprAddV4PolicyCondition</a>

