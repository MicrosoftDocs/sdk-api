---
UID: NE:dhcpsapi._DHCP_FORCE_FLAG
title: "_DHCP_FORCE_FLAG"
author: windows-driver-content
description: The DHCP_FORCE_FLAG enumeration defines the set of flags describing the force level of a DHCP subnet element deletion operation.
old-location: dhcp\dhcp_force_flag.htm
old-project: DHCP
ms.assetid: 2ec45a99-432d-4218-9048-81714ceff36b
ms.author: windowsdriverdev
ms.date: 5/2/2018
ms.keywords: "*LPDHCP_FORCE_FLAG, DHCP_FORCE_FLAG, DHCP_FORCE_FLAG enumeration [DHCP], DhcpFailoverForce, DhcpFullForce, DhcpNoForce, LPDHCP_FORCE_FLAG, LPDHCP_FORCE_FLAG enumeration pointer [DHCP], _DHCP_FORCE_FLAG, dhcp.dhcp_force_flag, dhcpsapi/DHCP_FORCE_FLAG, dhcpsapi/DhcpFailoverForce, dhcpsapi/DhcpFullForce, dhcpsapi/DhcpNoForce, dhcpsapi/LPDHCP_FORCE_FLAG"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DHCP_FORCE_FLAG, *LPDHCP_FORCE_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Dhcpsapi.h
api_name:
-	DHCP_FORCE_FLAG
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCP_FORCE_FLAG enumeration


## -description



      The <b>DHCP_FORCE_FLAG</b> enumeration defines the set of flags describing the force level of a DHCP subnet element deletion operation.


## -enum-fields




### -field DhcpFullForce

The operation deletes all client records affected by the element, and then deletes the element.


### -field DhcpNoForce

The operation only deletes the subnet element, leaving intact any client records impacted by the change.


### -field DhcpFailoverForce

The operation deletes all client records affected by the element, and then deletes the element from the DHCP server. But it does not delete any registered DNS records associated with the deleted client records from the DNS server. This flag is only valid when passed to <a href="https://msdn.microsoft.com/e000a81b-b61b-4ba9-adee-4940edc78050">DhcpDeleteSubnet</a>. Note that the minimum server OS requirement for this value is Windows Server 2012 R2 with KB 3100473 installed.


## -see-also




<a href="https://msdn.microsoft.com/8232b2cc-0bb1-4509-ad5f-6d1d1ece9fe5">
        DhcpRemoveSubnetElementV5</a>
 

 

