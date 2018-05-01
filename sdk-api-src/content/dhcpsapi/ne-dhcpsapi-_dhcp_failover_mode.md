---
UID: NE:dhcpsapi._DHCP_FAILOVER_MODE
title: "_DHCP_FAILOVER_MODE"
author: windows-driver-content
description: The DHCP_FAILOVER_MODE enumeration defines the DHCPv4 server mode operation in a failover relationship.
old-location: dhcp\dhcp_failover_mode.htm
old-project: DHCP
ms.assetid: 333f70a5-63bd-47f0-bb56-c5f6060e2a72
ms.author: windowsdriverdev
ms.date: 4/7/2018
ms.keywords: "*LPDHCP_FAILOVER_MODE, DHCP_FAILOVER_MODE, DHCP_FAILOVER_MODE enumeration [DHCP], HotStandby, LPDHCP_FAILOVER_MODE, LPDHCP_FAILOVER_MODE enumeration pointer [DHCP], LoadBalance, _DHCP_FAILOVER_MODE, dhcp.dhcp_failover_mode, dhcpsapi/DHCP_FAILOVER_MODE, dhcpsapi/HotStandby, dhcpsapi/LPDHCP_FAILOVER_MODE, dhcpsapi/LoadBalance"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: DHCP_FAILOVER_MODE, *LPDHCP_FAILOVER_MODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	dhcpsapi.h
api_name:
-	DHCP_FAILOVER_MODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCP_FAILOVER_MODE enumeration


## -description


The <b>DHCP_FAILOVER_MODE</b> enumeration defines the DHCPv4 server mode operation in a failover relationship.




## -enum-fields




### -field LoadBalance

The DHCPv4 server failover relationship is in <i>Load Balancing</i> mode.


### -field HotStandby

The DHCPv4 server failover relationship is in <i>Hot Standby</i> mode.


## -see-also




<a href="https://msdn.microsoft.com/b409b0ff-2fdc-416c-a7ce-2cba9cf75122">DHCP_FAILOVER_RELATIONSHIP</a>
 

 

