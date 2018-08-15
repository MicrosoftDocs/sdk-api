---
UID: NF:dhcpsapi.DhcpGetSubnetInfo
title: DhcpGetSubnetInfo function
author: windows-sdk-content
description: The DhcpGetSubnetInfo function returns information on a specific subnet.
old-location: dhcp\dhcpgetsubnetinfo.htm
old-project: dhcp
ms.assetid: 0e511993-a9c3-445b-bafc-3d66182ee32d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DhcpGetSubnetInfo, DhcpGetSubnetInfo function [DHCP], dhcp.dhcpgetsubnetinfo, dhcpsapi/DhcpGetSubnetInfo
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
 - DhcpGetSubnetInfo
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpGetSubnetInfo function


## -description


The <b>DhcpGetSubnetInfo</b> function returns information on a specific subnet.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.


### -param SubnetAddress [in]


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> value that specifies the subnet ID.


### -param SubnetInfo [out]


<a href="https://msdn.microsoft.com/030b4743-7558-493c-931c-1ad28a6b435a">DHCP_SUBNET_INFO</a> structure that contains the returned information for the subnet matching the ID specified by <i>SubnetAddress</i>.

<div class="alert"><b>Note</b>  <p class="note">The memory for this parameter must be free using <a href="https://msdn.microsoft.com/bf22a0a6-2ecd-4460-89c4-3f870c6275dc">DhcpRpcFreeMemory</a>.

</div>
<div> </div>

## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.




## -remarks



This function uses host byte ordering for all <a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> values in the <a href="https://msdn.microsoft.com/030b4743-7558-493c-931c-1ad28a6b435a">DHCP_SUBNET_INFO</a> structure passed back to the caller in the <i>SubnetInfo</i> parameter. However, this function uses network byte order for the <b>IpAddress</b> member of the <a href="https://msdn.microsoft.com/3d38f69d-2808-4e52-a3da-b6142578c981">DHCP_HOST_INFO</a> structure within the <b>DHCP_SUBNET_INFO</b> structure.




## -see-also




<a href="https://msdn.microsoft.com/030b4743-7558-493c-931c-1ad28a6b435a">DHCP_SUBNET_INFO</a>
 

 

