---
UID: NS:dhcpsapi._DHCP_SCAN_ITEM
title: "_DHCP_SCAN_ITEM"
author: windows-driver-content
description: The DHCP_SCAN_ITEM structure defines a desynchronized client lease address stored on a DHCPv4 server, and the location in which it should be fixed (in-memory cache or database).
old-location: dhcp\dhcp_scan_item.htm
old-project: DHCP
ms.assetid: 82e36660-fb56-4334-97d0-c34facad55a6
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: "*LPDHCP_SCAN_ITEM, DHCP_SCAN_ITEM, DHCP_SCAN_ITEM structure [DHCP], LPDHCP_SCAN_ITEM, LPDHCP_SCAN_ITEM structure pointer [DHCP], _DHCP_SCAN_ITEM, dhcp.dhcp_scan_item, dhcpsapi/LPDHCP_SCAN_ITEM, dhcpsapi/_DHCP_SCAN_ITEM"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: DHCP_SCAN_ITEM, *LPDHCP_SCAN_ITEM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Dhcpsapi.h
api_name:
-	DHCP_SCAN_ITEM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCP_SCAN_ITEM structure


## -description


The <b>DHCP_SCAN_ITEM</b> structure defines a desynchronized client lease address stored on a DHCPv4 server, and the location in which it should be fixed (in-memory cache or database).


## -struct-fields




### -field IpAddress

DHCP_IP_ADDRESS value that specifies the address whose lease status was changed during a scan operation.


### -field ScanFlag


<a href="https://msdn.microsoft.com/825a0e64-b0c2-453e-8e00-52f84c40bef3">DHCP_SCAN_FLAG</a>
         enumeration value that indicates whether the supplied client lease IP address will be fixed in the DHCPv4 server's  in-memory client lease cache or the client lease database proper.


## -see-also




<a href="https://msdn.microsoft.com/825a0e64-b0c2-453e-8e00-52f84c40bef3">DHCP_SCAN_FLAG</a>



<a href="https://msdn.microsoft.com/9dc20612-1c08-4493-aab3-b524d8d88251">DHCP_SCAN_LIST</a>



<a href="https://msdn.microsoft.com/6324c197-7237-449f-ae23-4f04b1b7498e">DhcpScanDatabase</a>
 

 

