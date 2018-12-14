---
UID: NS:dhcpsapi._DHCP_SCAN_LIST
title: DHCP_SCAN_LIST
author: windows-sdk-content
description: Defines a list of all desynchronized client lease IP address on a DHCPv4 server that must be fixed.
old-location: dhcp\dhcp_scan_list.htm
tech.root: DHCP
ms.assetid: 9dc20612-1c08-4493-aab3-b524d8d88251
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPDHCP_SCAN_LIST, DHCP_SCAN_LIST, DHCP_SCAN_LIST structure [DHCP], LPDHCP_SCAN_LIST, LPDHCP_SCAN_LIST structure pointer [DHCP], dhcp.dhcp_scan_list, dhcpsapi/LPDHCP_SCAN_LIST, dhcpsapi/_DHCP_SCAN_LIST"
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
 - DHCP_SCAN_LIST
product: Windows
targetos: Windows
req.typenames: DHCP_SCAN_LIST, *LPDHCP_SCAN_LIST
req.redist: 
---

# DHCP_SCAN_LIST structure


## -description


The <b>DHCP_SCAN_LIST</b> structure defines a list of all desynchronized client lease IP address on a DHCPv4 server that must be fixed.


## -struct-fields




### -field NumScanItems

Specifies the number of <a href="https://msdn.microsoft.com/82e36660-fb56-4334-97d0-c34facad55a6">DHCP_SCAN_ITEM</a>structures listed in <i>ScanItems</i>.


### -field ScanItems

Pointer to a list of <a href="https://msdn.microsoft.com/82e36660-fb56-4334-97d0-c34facad55a6">DHCP_SCAN_ITEM</a>structures that contain the specific client IP addresses whose leases differed between the in-memory cache of client leases and the subnet client lease database during a <a href="https://msdn.microsoft.com/6324c197-7237-449f-ae23-4f04b1b7498e">DhcpScanDatabase</a>operation.


### -field ScanItems.size_is

 


### -field ScanItems.size_is.NumScanItems

 




## -see-also




<a href="https://msdn.microsoft.com/82e36660-fb56-4334-97d0-c34facad55a6">DHCP_SCAN_ITEM</a>



<a href="https://msdn.microsoft.com/6324c197-7237-449f-ae23-4f04b1b7498e">DhcpScanDatabase</a>
 

 

