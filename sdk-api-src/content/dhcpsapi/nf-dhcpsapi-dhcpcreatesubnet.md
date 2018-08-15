---
UID: NF:dhcpsapi.DhcpCreateSubnet
title: DhcpCreateSubnet function
author: windows-sdk-content
description: The DhcpCreateSubnet function creates a new subnet on the DHCP server.
old-location: dhcp\dhcpcreatesubnet.htm
old-project: dhcp
ms.assetid: acae01cf-cbd9-4461-a1cc-5fcb745b9c8f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DhcpCreateSubnet, DhcpCreateSubnet function [DHCP], dhcp.dhcpcreatesubnet, dhcpsapi/DhcpCreateSubnet
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dhcpsapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: QuarantineStatus
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dhcpsapi.dll
api_name:
 - DhcpCreateSubnet
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpCreateSubnet function


## -description


The <b>DhcpCreateSubnet</b> function creates a new subnet on the DHCP server.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.


### -param SubnetAddress [in]


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> value that contains the IP address of the subnet's gateway.


### -param SubnetInfo [in]


<a href="https://msdn.microsoft.com/030b4743-7558-493c-931c-1ad28a6b435a">DHCP_SUBNET_INFO</a> structure that contains specific settings for the subnet, including the subnet mask and IP address of the  subnet gateway.


## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/030b4743-7558-493c-931c-1ad28a6b435a">DHCP_SUBNET_INFO</a>



<a href="https://msdn.microsoft.com/e000a81b-b61b-4ba9-adee-4940edc78050">DhcpDeleteSubnet</a>



<a href="https://msdn.microsoft.com/333381c9-66d1-44ef-911b-d543c79abefb">DhcpEnumSubnets</a>
 

 

