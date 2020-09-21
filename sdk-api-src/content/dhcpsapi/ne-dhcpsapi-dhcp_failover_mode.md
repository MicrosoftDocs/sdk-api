---
UID: NE:dhcpsapi._DHCP_FAILOVER_MODE
title: DHCP_FAILOVER_MODE (dhcpsapi.h)
description: The DHCP_FAILOVER_MODE enumeration defines the DHCPv4 server mode operation in a failover relationship.
helpviewer_keywords: ["*LPDHCP_FAILOVER_MODE","DHCP_FAILOVER_MODE","DHCP_FAILOVER_MODE enumeration [DHCP]","HotStandby","LPDHCP_FAILOVER_MODE","LPDHCP_FAILOVER_MODE enumeration pointer [DHCP]","LoadBalance","dhcp.dhcp_failover_mode","dhcpsapi/DHCP_FAILOVER_MODE","dhcpsapi/HotStandby","dhcpsapi/LPDHCP_FAILOVER_MODE","dhcpsapi/LoadBalance"]
old-location: dhcp\dhcp_failover_mode.htm
tech.root: DHCP
ms.assetid: 333f70a5-63bd-47f0-bb56-c5f6060e2a72
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_FAILOVER_MODE, DHCP_FAILOVER_MODE, DHCP_FAILOVER_MODE enumeration [DHCP], HotStandby, LPDHCP_FAILOVER_MODE, LPDHCP_FAILOVER_MODE enumeration pointer [DHCP], LoadBalance, dhcp.dhcp_failover_mode, dhcpsapi/DHCP_FAILOVER_MODE, dhcpsapi/HotStandby, dhcpsapi/LPDHCP_FAILOVER_MODE, dhcpsapi/LoadBalance'
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
req.typenames: DHCP_FAILOVER_MODE, *LPDHCP_FAILOVER_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_FAILOVER_MODE
 - dhcpsapi/_DHCP_FAILOVER_MODE
 - LPDHCP_FAILOVER_MODE
 - dhcpsapi/LPDHCP_FAILOVER_MODE
 - DHCP_FAILOVER_MODE
 - dhcpsapi/DHCP_FAILOVER_MODE
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
 - DHCP_FAILOVER_MODE
---

# DHCP_FAILOVER_MODE enumeration


## -description

The <b>DHCP_FAILOVER_MODE</b> enumeration defines the DHCPv4 server mode operation in a failover relationship.

## -enum-fields

### -field LoadBalance

The DHCPv4 server failover relationship is in <i>Load Balancing</i> mode.

### -field HotStandby

The DHCPv4 server failover relationship is in <i>Hot Standby</i> mode.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_failover_relationship">DHCP_FAILOVER_RELATIONSHIP</a>