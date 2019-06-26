---
UID: NS:dhcpsapi._SCOPE_MIB_INFO_V5
title: SCOPE_MIB_INFO_V5 (dhcpsapi.h)
author: windows-sdk-content
description: Contains information about a specific DHCP scope.
old-location: dhcp\scope_mib_info_v5.htm
tech.root: DHCP
ms.assetid: 5144d83e-f21e-4f68-bf33-c7245b31da01
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPSCOPE_MIB_INFO_V5, LPSCOPE_MIB_INFO_V5, LPSCOPE_MIB_INFO_V5 structure pointer [DHCP], SCOPE_MIB_INFO_V5, SCOPE_MIB_INFO_V5 structure [DHCP], dhcp.scope_mib_info_v5, dhcpsapi/LPSCOPE_MIB_INFO_V5, dhcpsapi/SCOPE_MIB_INFO_V5"
ms.topic: struct
f1_keywords: 
 - "dhcpsapi/SCOPE_MIB_INFO_V5"
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
ms.custom: 19H1
---

# SCOPE_MIB_INFO_V5 structure


## -description


The <b>SCOPE_MIB_INFO_V5</b> structure contains information about a specific DHCP scope.


## -struct-fields




### -field Subnet


<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> value that contains the IP address of the subnet gateway that defines the scope.


### -field NumAddressesInuse

 


### -field NumAddressesFree

The number of IP addresses in the scope that are not currently  assigned to DHCP clients.


### -field NumPendingOffers

The number of IP addresses in the scope that have been offered to DHCP clients but have not yet received REQUEST messages.


#### - NumAddressesInUse

The number of IP addresses in the scope that are currently assigned to DHCP clients.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/ns-dhcpsapi-_dhcp_mib_info_v5">DHCP_MIB_INFO_V5</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpgetmibinfov5">DhcpGetMibInfoV5</a>
 

 

