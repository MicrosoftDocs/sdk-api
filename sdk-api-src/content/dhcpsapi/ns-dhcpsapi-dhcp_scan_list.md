---
UID: NS:dhcpsapi._DHCP_SCAN_LIST
title: DHCP_SCAN_LIST (dhcpsapi.h)
description: Defines a list of all desynchronized client lease IP address on a DHCPv4 server that must be fixed.
helpviewer_keywords: ["*LPDHCP_SCAN_LIST","DHCP_SCAN_LIST","DHCP_SCAN_LIST structure [DHCP]","LPDHCP_SCAN_LIST","LPDHCP_SCAN_LIST structure pointer [DHCP]","dhcp.dhcp_scan_list","dhcpsapi/LPDHCP_SCAN_LIST","dhcpsapi/_DHCP_SCAN_LIST"]
old-location: dhcp\dhcp_scan_list.htm
tech.root: DHCP
ms.assetid: 9dc20612-1c08-4493-aab3-b524d8d88251
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_SCAN_LIST, DHCP_SCAN_LIST, DHCP_SCAN_LIST structure [DHCP], LPDHCP_SCAN_LIST, LPDHCP_SCAN_LIST structure pointer [DHCP], dhcp.dhcp_scan_list, dhcpsapi/LPDHCP_SCAN_LIST, dhcpsapi/_DHCP_SCAN_LIST'
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
req.typenames: DHCP_SCAN_LIST, *LPDHCP_SCAN_LIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_SCAN_LIST
 - dhcpsapi/_DHCP_SCAN_LIST
 - LPDHCP_SCAN_LIST
 - dhcpsapi/LPDHCP_SCAN_LIST
 - DHCP_SCAN_LIST
 - dhcpsapi/DHCP_SCAN_LIST
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
 - DHCP_SCAN_LIST
---

# DHCP_SCAN_LIST structure


## -description

The <b>DHCP_SCAN_LIST</b> structure defines a list of all desynchronized client lease IP address on a DHCPv4 server that must be fixed.

## -struct-fields

### -field NumScanItems

Specifies the number of <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_scan_item">DHCP_SCAN_ITEM</a> structures listed in <i>ScanItems</i>.

### -field ScanItems

Pointer to a list of <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_scan_item">DHCP_SCAN_ITEM</a> structures that contain the specific client IP addresses whose leases differed between the in-memory cache of client leases and the subnet client lease database during a <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpscandatabase">DhcpScanDatabase</a> operation.

### -field ScanItems.size_is

### -field ScanItems.size_is.NumScanItems

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_scan_item">DHCP_SCAN_ITEM</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpscandatabase">DhcpScanDatabase</a>