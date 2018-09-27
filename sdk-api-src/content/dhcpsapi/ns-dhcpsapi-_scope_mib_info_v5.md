---
UID: NS:dhcpsapi._SCOPE_MIB_INFO_V5
title: "_SCOPE_MIB_INFO_V5"
author: windows-sdk-content
description: Contains information about a specific DHCP scope.
old-location: dhcp\scope_mib_info_v5.htm
tech.root: DHCP
ms.assetid: 5144d83e-f21e-4f68-bf33-c7245b31da01
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*LPSCOPE_MIB_INFO_V5, LPSCOPE_MIB_INFO_V5, LPSCOPE_MIB_INFO_V5 structure pointer [DHCP], SCOPE_MIB_INFO_V5, SCOPE_MIB_INFO_V5 structure [DHCP], _SCOPE_MIB_INFO_V5, dhcp.scope_mib_info_v5, dhcpsapi/LPSCOPE_MIB_INFO_V5, dhcpsapi/SCOPE_MIB_INFO_V5"
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
 - SCOPE_MIB_INFO_V5
product: Windows
targetos: Windows
req.typenames: SCOPE_MIB_INFO_V5, *LPSCOPE_MIB_INFO_V5
req.redist: 
---

# _SCOPE_MIB_INFO_V5 structure


## -description


The <b>SCOPE_MIB_INFO_V5</b> structure contains information about a specific DHCP scope.


## -struct-fields




### -field Subnet


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> value that contains the IP address of the subnet gateway that defines the scope.


### -field NumAddressesInuse

 


### -field NumAddressesFree

The number of IP addresses in the scope that are not currently  assigned to DHCP clients.


### -field NumPendingOffers

The number of IP addresses in the scope that have been offered to DHCP clients but have not yet received REQUEST messages.


#### - NumAddressesInUse

The number of IP addresses in the scope that are currently assigned to DHCP clients.


## -see-also




<a href="https://msdn.microsoft.com/5081ebce-d3b9-4548-8d80-23d994bce7ab">DHCP_MIB_INFO_V5</a>



<a href="https://msdn.microsoft.com/3439198d-5391-4f9b-a6fe-9a600e7dc77b">DhcpGetMibInfoV5</a>
 

 

