---
UID: NC:dhcpssdk.LPDHCP_DELETE_CLIENT
title: LPDHCP_DELETE_CLIENT (dhcpssdk.h)
author: windows-sdk-content
description: The DhcpDeleteClientHook function is called by Microsoft DHCP Server directly before a client lease is deleted from the active leases database.
old-location: dhcp\dhcpdeleteclienthook.htm
tech.root: DHCP
ms.assetid: ae92436c-0774-4664-86ac-c7df65ef40b5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DhcpDeleteClientHook, DhcpDeleteClientHook callback function [DHCP], LPDHCP_DELETE_CLIENT, LPDHCP_DELETE_CLIENT callback, _dhcp_dhcpdeleteclienthook, dhcp.dhcpdeleteclienthook, dhcpssdk/DhcpDeleteClientHook
ms.topic: callback
f1_keywords: 
 - "dhcpssdk/DhcpDeleteClientHook"
req.header: dhcpssdk.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Dhcpssdk.h
api_name:
 - DhcpDeleteClientHook
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LPDHCP_DELETE_CLIENT callback function


## -description


The 
<b>DhcpDeleteClientHook</b> function is called by Microsoft DHCP Server directly before a client lease is deleted from the active leases database.

The 
<b>DhcpDeleteClientHook</b> function should not block.


## -parameters




### -param IpAddress [in]

Internet Protocol (IP) address of the client lease being deleted. The IP address is in host order.


### -param HwAddress [in]

Buffer holding the Hardware address of the client, often referred to as the MAC address.


### -param HwAddressLength [in]

Length of the <i>HwAddress</i> buffer, in bytes.


### -param Reserved [in]

Reserved for future use.


### -param ClientType [in]

Reserved for future use.


## -returns



Return values are defined by the application providing the callback.




## -remarks



The 
<b>DhcpDeleteClientHook</b> function should not block.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpssdk/ns-dhcpssdk-_dhcp_callout_table">DHCP_CALLOUT_TABLE</a>
 

 

