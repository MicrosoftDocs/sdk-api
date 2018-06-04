---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

