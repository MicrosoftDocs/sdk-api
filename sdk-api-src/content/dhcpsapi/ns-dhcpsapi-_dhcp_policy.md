---
UID: NS:dhcpsapi._DHCP_POLICY
title: "_DHCP_POLICY"
author: windows-sdk-content
description: The DHCP_POLICY structure defines a DHCP server policy.
old-location: dhcp\dhcp_policy.htm
tech.root: DHCP
ms.assetid: 7e62d2f3-275a-45ab-baab-648fe135d0fc
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPDHCP_POLICY, *PDHCP_POLICY, DHCP_POLICY, DHCP_POLICY structure [DHCP], LPDHCP_POLICY, LPDHCP_POLICY structure pointer [DHCP], PDHCP_POLICY, PDHCP_POLICY structure pointer [DHCP], _DHCP_POLICY, dhcp.dhcp_policy, dhcpsapi/DHCP_POLICY, dhcpsapi/LPDHCP_POLICY, dhcpsapi/PDHCP_POLICY"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dhcpsapi.h
api_name:
 - DHCP_POLICY
product: Windows
targetos: Windows
req.typenames: DHCP_POLICY, *PDHCP_POLICY, *LPDHCP_POLICY
req.redist: 
---

# _DHCP_POLICY structure


## -description


The <b>DHCP_POLICY</b> structure defines a DHCP server policy.


## -struct-fields




### -field PolicyName

Pointer to a null-terminated Unicode string that represents the DHCP server policy name.


### -field IsGlobalPolicy

<b>TRUE</b> if the DHCP server policy is global. Otherwise, it is <b>FALSE</b>. 


### -field Subnet


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> structure that specifies the IPv4 subnet ID for a scope level policy.


### -field ProcessingOrder

Integer that specifies the processing order of the DHCP server policy. 1 indicates the highest priority and <b>MAX_DWORD</b> indicates the lowest.


### -field Conditions

Pointer to a <a href="https://msdn.microsoft.com/F6EDFFAC-ECBD-4B0E-A929-3DB67D8366AC">DHCP_POL_EXPR_ARRAY</a> that specifies the DHCP server policy conditions.


### -field Expressions

Pointer to a <a href="https://msdn.microsoft.com/F6EDFFAC-ECBD-4B0E-A929-3DB67D8366AC">DHCP_POL_EXPR_ARRAY</a> that specifies the DHCP server policy expressions.


### -field Ranges

Pointer to a <a href="https://msdn.microsoft.com/BC6C85D6-D123-44D6-BFE4-3073EC51B7EA">DHCP_IP_RANGE_ARRAY</a> that specifies the DHCP server IPv4 range associated with the policy.


### -field Description

A pointer to a null-terminated Unicode string that contains the description of the DHCP server policy.


### -field Enabled

<b>TRUE</b> if the policy is enabled. Otherwise, it is <b>FALSE</b>.


## -see-also




<a href="https://msdn.microsoft.com/220CD2F8-AFB4-4B87-9B10-904AD04E4C1F">DHCP_POLICY_ARRAY</a>



<a href="https://msdn.microsoft.com/5ce80514-ad63-44dd-9b9b-36679a97488b">DHCP_POLICY_FIELDS_TO_UPDATE</a>
 

 

