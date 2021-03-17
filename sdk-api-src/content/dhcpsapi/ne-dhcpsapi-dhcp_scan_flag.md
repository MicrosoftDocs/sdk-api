---
UID: NE:dhcpsapi._DHCP_SCAN_FLAG
title: DHCP_SCAN_FLAG (dhcpsapi.h)
description: The DHCP_SCAN_FLAG enumeration defines the set of possible targets of synchronization during a database scan operation.
helpviewer_keywords: ["*LPDHCP_SCAN_FLAG","DHCP_SCAN_FLAG","DHCP_SCAN_FLAG enumeration [DHCP]","DhcpDatabaseFix","DhcpRegistryFix","LPDHCP_SCAN_FLAG","LPDHCP_SCAN_FLAG enumeration pointer [DHCP]","dhcp.dhcp_scan_flag","dhcpsapi/DHCP_SCAN_FLAG","dhcpsapi/DhcpDatabaseFix","dhcpsapi/DhcpRegistryFix","dhcpsapi/LPDHCP_SCAN_FLAG"]
old-location: dhcp\dhcp_scan_flag.htm
tech.root: DHCP
ms.assetid: 825a0e64-b0c2-453e-8e00-52f84c40bef3
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_SCAN_FLAG, DHCP_SCAN_FLAG, DHCP_SCAN_FLAG enumeration [DHCP], DhcpDatabaseFix, DhcpRegistryFix, LPDHCP_SCAN_FLAG, LPDHCP_SCAN_FLAG enumeration pointer [DHCP], dhcp.dhcp_scan_flag, dhcpsapi/DHCP_SCAN_FLAG, dhcpsapi/DhcpDatabaseFix, dhcpsapi/DhcpRegistryFix, dhcpsapi/LPDHCP_SCAN_FLAG'
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2008 R2 [desktop apps only]
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
req.typenames: DHCP_SCAN_FLAG, *LPDHCP_SCAN_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_SCAN_FLAG
 - dhcpsapi/_DHCP_SCAN_FLAG
 - LPDHCP_SCAN_FLAG
 - dhcpsapi/LPDHCP_SCAN_FLAG
 - DHCP_SCAN_FLAG
 - dhcpsapi/DHCP_SCAN_FLAG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpsapi.h
api_name:
 - DHCP_SCAN_FLAG
---

# DHCP_SCAN_FLAG enumeration


## -description

The <b>DHCP_SCAN_FLAG</b> enumeration defines the set of possible targets of synchronization during a database scan operation.

## -enum-fields

### -field DhcpRegistryFix

Indicates that the in-memory client lease cache on the DHCPv4 server does not contain the client lease IP address, but the DHCPv4 client lease database does contain it. (Note that this enumeration does not inform <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpscandatabase">DhcpScanDatabase</a> to perform a registry operation despite the name.) Any reconciliation process should update the in-memory cache.

### -field DhcpDatabaseFix

Indicates that the client lease database on the DHCPv4 server does not contain the client lease IP address, but the in-memory cache of client leases  does contain it. Any reconciliation process should update the database.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_scan_item">DHCP_SCAN_ITEM</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpscandatabase">DhcpScanDatabase</a>