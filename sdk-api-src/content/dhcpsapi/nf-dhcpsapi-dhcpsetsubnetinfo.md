---
UID: NF:dhcpsapi.DhcpSetSubnetInfo
title: DhcpSetSubnetInfo function
author: windows-sdk-content
description: The DhcpSetSubnetInfo function sets information about a subnet defined on the DHCP server.
old-location: dhcp\dhcpsetsubnetinfo.htm
tech.root: dhcp
ms.assetid: a7978da5-945f-4893-83a8-5986c55703a5
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DhcpSetSubnetInfo, DhcpSetSubnetInfo function [DHCP], dhcp.dhcpsetsubnetinfo, dhcpsapi/DhcpSetSubnetInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dhcpsapi.h
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
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dhcpsapi.dll
api_name:
 - DhcpSetSubnetInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DhcpSetSubnetInfo function


## -description


The <b>DhcpSetSubnetInfo</b> function sets information about a subnet defined on the DHCP server.


## -parameters




### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.


### -param SubnetAddress [in]


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> value that specifies the IP address of the subnet gateway, as well as uniquely identifies the subnet.


### -param SubnetInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/030b4743-7558-493c-931c-1ad28a6b435a">DHCP_SUBNET_INFO</a> structure that contains the information about the subnet.


## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/030b4743-7558-493c-931c-1ad28a6b435a">DHCP_SUBNET_INFO</a>



<a href="https://msdn.microsoft.com/0e511993-a9c3-445b-bafc-3d66182ee32d">DhcpGetSubnetInfo</a>
 

 

