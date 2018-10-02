---
UID: NS:dhcpsapi._DHCP_POLICY_ARRAY
title: "_DHCP_POLICY_ARRAY"
author: windows-sdk-content
description: The DHCP_POLICY_ARRAY structure defines an array of DHCP server policies.
old-location: dhcp\dhcp_policy_array.htm
tech.root: DHCP
ms.assetid: 220CD2F8-AFB4-4B87-9B10-904AD04E4C1F
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*LPDHCP_POLICY_ARRAY, *PDHCP_POLICY_ARRAY, DHCP_POLICY_ARRAY, DHCP_POLICY_ARRAY structure [DHCP], LPDHCP_POLICY_ARRAY, LPDHCP_POLICY_ARRAY structure pointer [DHCP], PDHCP_POLICY_ARRAY, PDHCP_POLICY_ARRAY structure pointer [DHCP], _DHCP_POLICY_ARRAY, dhcp.dhcp_policy_array, dhcpsapi/DHCP_POLICY_ARRAY, dhcpsapi/LPDHCP_POLICY_ARRAY, dhcpsapi/PDHCP_POLICY_ARRAY"
ms.prod: windows
ms.technology: windows-sdk
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
 - DHCP_POLICY_ARRAY
product: Windows
targetos: Windows
req.typenames: DHCP_POLICY_ARRAY, *PDHCP_POLICY_ARRAY, *LPDHCP_POLICY_ARRAY
req.redist: 
---

# _DHCP_POLICY_ARRAY structure


## -description


The <b>DHCP_POLICY_ARRAY</b> structure defines an array of DHCP server policies.


## -struct-fields




### -field NumElements

Integer that specifies the number of DHCP server policies in <b>Elements</b>.


### -field Elements

Pointer to a list of <a href="https://msdn.microsoft.com/7e62d2f3-275a-45ab-baab-648fe135d0fc">DHCP_POLICY</a>  structures.


### -field Elements.size_is

 


### -field Elements.size_is.NumElements

 




## -see-also




<a href="https://msdn.microsoft.com/c3915699-f60d-495c-81df-85dc6fe2657c">DhcpV4EnumPolicies</a>
 

 

