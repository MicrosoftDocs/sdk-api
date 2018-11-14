---
UID: NC:dhcpssdk.LPDHCP_DELETE_CLIENT
title: LPDHCP_DELETE_CLIENT
author: windows-sdk-content
description: The DhcpDeleteClientHook function is called by Microsoft DHCP Server directly before a client lease is deleted from the active leases database.
old-location: dhcp\dhcpdeleteclienthook.htm
tech.root: DHCP
ms.assetid: ae92436c-0774-4664-86ac-c7df65ef40b5
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DhcpDeleteClientHook, DhcpDeleteClientHook callback function [DHCP], LPDHCP_DELETE_CLIENT, LPDHCP_DELETE_CLIENT callback, _dhcp_dhcpdeleteclienthook, dhcp.dhcpdeleteclienthook, dhcpssdk/DhcpDeleteClientHook
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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




<a href="https://msdn.microsoft.com/fa57e5c5-2335-44ba-8642-61dcb8b33ffe">DHCP_CALLOUT_TABLE</a>
 

 

