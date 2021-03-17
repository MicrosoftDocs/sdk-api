---
UID: NE:dhcpsapi._DHCP_FAILOVER_SERVER
title: DHCP_FAILOVER_SERVER (dhcpsapi.h)
description: The DHCP_FAILOVER_SERVER enumeration defines whether the DHCP server is the primary or secondary server in a DHCPv4 failover relationship.
helpviewer_keywords: ["*LPDHCP_FAILOVER_SERVER","DHCP_FAILOVER_SERVER","DHCP_FAILOVER_SERVER enumeration [DHCP]","LPDHCP_FAILOVER_SERVER","LPDHCP_FAILOVER_SERVER enumeration pointer [DHCP]","PrimaryServer","SecondaryServer","dhcp.dhcp_failover_server","dhcpsapi/DHCP_FAILOVER_SERVER","dhcpsapi/LPDHCP_FAILOVER_SERVER","dhcpsapi/PrimaryServer","dhcpsapi/SecondaryServer"]
old-location: dhcp\dhcp_failover_server.htm
tech.root: DHCP
ms.assetid: a75a1132-3c49-44f1-a1f6-c98991ebb8c4
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_FAILOVER_SERVER, DHCP_FAILOVER_SERVER, DHCP_FAILOVER_SERVER enumeration [DHCP], LPDHCP_FAILOVER_SERVER, LPDHCP_FAILOVER_SERVER enumeration pointer [DHCP], PrimaryServer, SecondaryServer, dhcp.dhcp_failover_server, dhcpsapi/DHCP_FAILOVER_SERVER, dhcpsapi/LPDHCP_FAILOVER_SERVER, dhcpsapi/PrimaryServer, dhcpsapi/SecondaryServer'
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
req.typenames: DHCP_FAILOVER_SERVER, *LPDHCP_FAILOVER_SERVER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_FAILOVER_SERVER
 - dhcpsapi/_DHCP_FAILOVER_SERVER
 - LPDHCP_FAILOVER_SERVER
 - dhcpsapi/LPDHCP_FAILOVER_SERVER
 - DHCP_FAILOVER_SERVER
 - dhcpsapi/DHCP_FAILOVER_SERVER
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
 - DHCP_FAILOVER_SERVER
---

# DHCP_FAILOVER_SERVER enumeration


## -description

The <b>DHCP_FAILOVER_SERVER</b> enumeration defines whether the DHCP server is the primary or secondary server in a DHCPv4 failover relationship.

## -enum-fields

### -field PrimaryServer

The server is a primary server in the failover relationship.

### -field SecondaryServer

The server is a secondary server in the failover relationship.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_failover_relationship">DHCP_FAILOVER_RELATIONSHIP</a>