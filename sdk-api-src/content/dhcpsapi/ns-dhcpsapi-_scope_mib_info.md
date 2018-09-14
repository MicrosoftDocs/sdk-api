---
UID: NS:dhcpsapi._SCOPE_MIB_INFO
title: "_SCOPE_MIB_INFO"
author: windows-sdk-content
description: Defines information about an available scope for use within returned DHCP-specific SNMP Management Information Block (MIB) data.
old-location: dhcp\scope_mib_info.htm
tech.root: DHCP
ms.assetid: 54f54734-3e4a-489f-a61d-85fd436d28ad
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*LPSCOPE_MIB_INFO, LPSCOPE_MIB_INFO, LPSCOPE_MIB_INFO structure pointer [DHCP], SCOPE_MIB_INFO, SCOPE_MIB_INFO structure [DHCP], _SCOPE_MIB_INFO, dhcp.scope_mib_info, dhcpsapi/LPSCOPE_MIB_INFO, dhcpsapi/_SCOPE_MIB_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpsapi.h
api_name:
 - SCOPE_MIB_INFO
product: Windows
targetos: Windows
req.typenames: SCOPE_MIB_INFO, *LPSCOPE_MIB_INFO
req.redist: 
---

# _SCOPE_MIB_INFO structure


## -description


The <b>SCOPE_MIB_INFO</b> structure defines information about an available scope for use within returned DHCP-specific SNMP Management Information Block (MIB) data.


## -struct-fields




### -field Subnet


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> value that specifies the subnet mask for this scope.


### -field NumAddressesInuse

Contains the number of IP addresses currently in use for this scope.


### -field NumAddressesFree

Contains the number of IP addresses currently available for this scope.


### -field NumPendingOffers

Contains the number of IP addresses currently in the offer state for this scope.


## -see-also




<a href="https://msdn.microsoft.com/58f3e3a3-8246-48ff-be45-20a7eed1ed0e">DHCP_MIB_INFO</a>



<a href="https://msdn.microsoft.com/8b961666-4b55-47b4-be52-81b67c9d1cae">DHCP_MIB_INFO_V6</a>
 

 

