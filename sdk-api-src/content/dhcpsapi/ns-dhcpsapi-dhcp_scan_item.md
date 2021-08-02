---
UID: NS:dhcpsapi._DHCP_SCAN_ITEM
title: DHCP_SCAN_ITEM (dhcpsapi.h)
description: The DHCP_SCAN_ITEM structure defines a desynchronized client lease address stored on a DHCPv4 server, and the location in which it should be fixed (in-memory cache or database).
helpviewer_keywords: ["*LPDHCP_SCAN_ITEM","DHCP_SCAN_ITEM","DHCP_SCAN_ITEM structure [DHCP]","LPDHCP_SCAN_ITEM","LPDHCP_SCAN_ITEM structure pointer [DHCP]","dhcp.dhcp_scan_item","dhcpsapi/LPDHCP_SCAN_ITEM","dhcpsapi/_DHCP_SCAN_ITEM"]
old-location: dhcp\dhcp_scan_item.htm
tech.root: DHCP
ms.assetid: 82e36660-fb56-4334-97d0-c34facad55a6
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_SCAN_ITEM, DHCP_SCAN_ITEM, DHCP_SCAN_ITEM structure [DHCP], LPDHCP_SCAN_ITEM, LPDHCP_SCAN_ITEM structure pointer [DHCP], dhcp.dhcp_scan_item, dhcpsapi/LPDHCP_SCAN_ITEM, dhcpsapi/_DHCP_SCAN_ITEM'
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
req.typenames: DHCP_SCAN_ITEM, *LPDHCP_SCAN_ITEM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_SCAN_ITEM
 - dhcpsapi/_DHCP_SCAN_ITEM
 - LPDHCP_SCAN_ITEM
 - dhcpsapi/LPDHCP_SCAN_ITEM
 - DHCP_SCAN_ITEM
 - dhcpsapi/DHCP_SCAN_ITEM
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
 - DHCP_SCAN_ITEM
---

# DHCP_SCAN_ITEM structure


## -description

The <b>DHCP_SCAN_ITEM</b> structure defines a desynchronized client lease address stored on a DHCPv4 server, and the location in which it should be fixed (in-memory cache or database).

## -struct-fields

### -field IpAddress

DHCP_IP_ADDRESS value that specifies the address whose lease status was changed during a scan operation.

### -field ScanFlag

<a href="/windows/desktop/api/dhcpsapi/ne-dhcpsapi-dhcp_scan_flag">DHCP_SCAN_FLAG</a> enumeration value that indicates whether the supplied client lease IP address will be fixed in the DHCPv4 server's  in-memory client lease cache or the client lease database proper.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ne-dhcpsapi-dhcp_scan_flag">DHCP_SCAN_FLAG</a>



<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_scan_list">DHCP_SCAN_LIST</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpscandatabase">DhcpScanDatabase</a>