---
UID: NS:dhcpsapi._DHCP_POLICY
title: DHCP_POLICY (dhcpsapi.h)
description: The DHCP_POLICY structure defines a DHCP server policy.
helpviewer_keywords: ["*LPDHCP_POLICY","*PDHCP_POLICY","DHCP_POLICY","DHCP_POLICY structure [DHCP]","LPDHCP_POLICY","LPDHCP_POLICY structure pointer [DHCP]","PDHCP_POLICY","PDHCP_POLICY structure pointer [DHCP]","dhcp.dhcp_policy","dhcpsapi/DHCP_POLICY","dhcpsapi/LPDHCP_POLICY","dhcpsapi/PDHCP_POLICY"]
old-location: dhcp\dhcp_policy.htm
tech.root: DHCP
ms.assetid: 7e62d2f3-275a-45ab-baab-648fe135d0fc
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_POLICY, *PDHCP_POLICY, DHCP_POLICY, DHCP_POLICY structure [DHCP], LPDHCP_POLICY, LPDHCP_POLICY structure pointer [DHCP], PDHCP_POLICY, PDHCP_POLICY structure pointer [DHCP], dhcp.dhcp_policy, dhcpsapi/DHCP_POLICY, dhcpsapi/LPDHCP_POLICY, dhcpsapi/PDHCP_POLICY'
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
req.typenames: DHCP_POLICY, *PDHCP_POLICY, *LPDHCP_POLICY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_POLICY
 - dhcpsapi/_DHCP_POLICY
 - PDHCP_POLICY
 - dhcpsapi/PDHCP_POLICY
 - DHCP_POLICY
 - dhcpsapi/DHCP_POLICY
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
 - DHCP_POLICY
---

# DHCP_POLICY structure


## -description

The <b>DHCP_POLICY</b> structure defines a DHCP server policy.

## -struct-fields

### -field PolicyName

Pointer to a null-terminated Unicode string that represents the DHCP server policy name.

### -field IsGlobalPolicy

<b>TRUE</b> if the DHCP server policy is global. Otherwise, it is <b>FALSE</b>.

### -field Subnet

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> structure that specifies the IPv4 subnet ID for a scope level policy.

### -field ProcessingOrder

Integer that specifies the processing order of the DHCP server policy. 1 indicates the highest priority and <b>MAX_DWORD</b> indicates the lowest.

### -field Conditions

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_pol_expr_array">DHCP_POL_EXPR_ARRAY</a> that specifies the DHCP server policy conditions.

### -field Expressions

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_pol_expr_array">DHCP_POL_EXPR_ARRAY</a> that specifies the DHCP server policy expressions.

### -field Ranges

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_ip_range_array">DHCP_IP_RANGE_ARRAY</a> that specifies the DHCP server IPv4 range associated with the policy.

### -field Description

A pointer to a null-terminated Unicode string that contains the description of the DHCP server policy.

### -field Enabled

<b>TRUE</b> if the policy is enabled. Otherwise, it is <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_policy_array">DHCP_POLICY_ARRAY</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/ne-dhcpsapi-dhcp_policy_fields_to_update">DHCP_POLICY_FIELDS_TO_UPDATE</a>