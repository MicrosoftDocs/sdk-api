---
UID: NE:dhcpsapi.__unnamed_enum_5
title: DHCP_POLICY_FIELDS_TO_UPDATE (dhcpsapi.h)
description: The DHCP_POLICY_FIELDS_TO_UPDATE enumeration defines which properties of a DHCP server policy must be updated.
helpviewer_keywords: ["DHCP_POLICY_FIELDS_TO_UPDATE","DHCP_POLICY_FIELDS_TO_UPDATE enumeration [DHCP]","DhcpUpdatePolicyDescr","DhcpUpdatePolicyExpr","DhcpUpdatePolicyName","DhcpUpdatePolicyOrder","DhcpUpdatePolicyRanges","DhcpUpdatePolicyStatus","dhcp.dhcp_policy_fields_to_update","dhcpsapi/DHCP_POLICY_FIELDS_TO_UPDATE","dhcpsapi/DhcpUpdatePolicyDescr","dhcpsapi/DhcpUpdatePolicyExpr","dhcpsapi/DhcpUpdatePolicyName","dhcpsapi/DhcpUpdatePolicyOrder","dhcpsapi/DhcpUpdatePolicyRanges","dhcpsapi/DhcpUpdatePolicyStatus"]
old-location: dhcp\dhcp_policy_fields_to_update.htm
tech.root: DHCP
ms.assetid: 5ce80514-ad63-44dd-9b9b-36679a97488b
ms.date: 12/05/2018
ms.keywords: DHCP_POLICY_FIELDS_TO_UPDATE, DHCP_POLICY_FIELDS_TO_UPDATE enumeration [DHCP], DhcpUpdatePolicyDescr, DhcpUpdatePolicyExpr, DhcpUpdatePolicyName, DhcpUpdatePolicyOrder, DhcpUpdatePolicyRanges, DhcpUpdatePolicyStatus, dhcp.dhcp_policy_fields_to_update, dhcpsapi/DHCP_POLICY_FIELDS_TO_UPDATE, dhcpsapi/DhcpUpdatePolicyDescr, dhcpsapi/DhcpUpdatePolicyExpr, dhcpsapi/DhcpUpdatePolicyName, dhcpsapi/DhcpUpdatePolicyOrder, dhcpsapi/DhcpUpdatePolicyRanges, dhcpsapi/DhcpUpdatePolicyStatus
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
req.typenames: DHCP_POLICY_FIELDS_TO_UPDATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DHCP_POLICY_FIELDS_TO_UPDATE
 - dhcpsapi/DHCP_POLICY_FIELDS_TO_UPDATE
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
 - DHCP_POLICY_FIELDS_TO_UPDATE
---

# DHCP_POLICY_FIELDS_TO_UPDATE enumeration


## -description

The <b>DHCP_POLICY_FIELDS_TO_UPDATE</b> enumeration defines which properties of a DHCP server policy must be updated.

## -enum-fields

### -field DhcpUpdatePolicyName:0x00000001

Update DHCP server policy name.

### -field DhcpUpdatePolicyOrder:0x00000002

Update DHCP server policy order.

### -field DhcpUpdatePolicyExpr:0x00000004

Update DHCP server policy expression.

### -field DhcpUpdatePolicyRanges:0x00000008

Update DHCP server policy ranges.

### -field DhcpUpdatePolicyDescr:0x00000010

Update DHCP server policy description.

### -field DhcpUpdatePolicyStatus:0x00000020

Update DHCP server policy enabled/disabled status.

### -field DhcpUpdatePolicyDnsSuffix:0x00000040

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4setpolicy">Dhcpv4SetPolicy</a>
