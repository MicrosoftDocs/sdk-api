---
UID: NF:dhcpsapi.DhcpAddSubnetElementV5
title: DhcpAddSubnetElementV5 function
author: windows-sdk-content
description: The DhcpAddSubnetElementV5 function adds an element describing a feature or aspect of the subnet to the subnet entry in the DHCP database. Windows 2000 and earlier:  This function is not available.
old-location: dhcp\dhcpaddsubnetelementv5.htm
old-project: DHCP
ms.assetid: 200fc8da-d05c-4502-9cfc-d1092c5d0417
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: DhcpAddSubnetElementV5, DhcpAddSubnetElementV5 function [DHCP], dhcp.dhcpaddsubnetelementv5, dhcpsapi/DhcpAddSubnetElementV5
ms.prod: windows
ms.technology: windows-sdk
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
 - DhcpAddSubnetElementV5
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpAddSubnetElementV5 function


## -description



      The <b>DhcpAddSubnetElementV5</b> function  adds an element describing a feature or aspect of the subnet to the subnet entry in the DHCP database. <b>Windows 2000 and earlier:  </b>This function is not available.




## -parameters




### -param ServerIpAddress [in, optional]

Pointer to a Unicode string that contains the IP address or hostname of the subnet DHCP server.


### -param SubnetAddress [in]


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> structure that contains the IP address of the subnet.


### -param AddElementInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/ea6df1bc-2d15-4a09-8100-ee17d3de34d9">DHCP_SUBNET_ELEMENT_DATA_V5</a> structure that contains the element data to add to the subnet. The V5 structure adds support for BOOTP clients.


## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.




## -remarks



This API emulates the RPC interface used by the Windows NT 4.0 DHCP server. It is provided for backward compatibility with older versions of the DHCP Administrator application.




## -see-also




<a href="https://msdn.microsoft.com/ea6df1bc-2d15-4a09-8100-ee17d3de34d9">DHCP_SUBNET_ELEMENT_DATA_V5</a>
 

 

