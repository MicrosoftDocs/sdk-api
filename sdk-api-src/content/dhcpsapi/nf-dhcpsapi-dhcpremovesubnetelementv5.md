---
UID: NF:dhcpsapi.DhcpRemoveSubnetElementV5
title: DhcpRemoveSubnetElementV5 function
author: windows-sdk-content
description: The DhcpRemoveSubnetElementV5 function removes an element from a subnet defined on the DHCP server.
old-location: dhcp\dhcpremovesubnetelementv5.htm
old-project: DHCP
ms.assetid: 8232b2cc-0bb1-4509-ad5f-6d1d1ece9fe5
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: DhcpRemoveSubnetElementV5, DhcpRemoveSubnetElementV5 function [DHCP], dhcp.dhcpremovesubnetelementv5, dhcpsapi/DhcpRemoveSubnetElementV5
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
req.typenames: QuarantineStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Dhcpsapi.dll
api_name:
-	DhcpRemoveSubnetElementV5
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpRemoveSubnetElementV5 function


## -description


The <b>DhcpRemoveSubnetElementV5</b> function removes an element from a subnet defined on the DHCP server.


## -parameters




### -param ServerIpAddress [in, optional]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.


### -param SubnetAddress [in]


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> value that specifies the IP address of the subnet gateway and uniquely identifies it.


### -param RemoveElementInfo [in]


<a href="https://msdn.microsoft.com/ea6df1bc-2d15-4a09-8100-ee17d3de34d9">DHCP_SUBNET_ELEMENT_DATA_V5</a> structure that contains information used to find the element that will be removed from subnet specified in <i>SubnetAddress</i>.


### -param ForceFlag [in]


<a href="https://msdn.microsoft.com/2ec45a99-432d-4218-9048-81714ceff36b">DHCP_FORCE_FLAG</a> enumeration value that indicates whether or not the clients affected by the removal of the subnet element should also be deleted.


## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.




## -remarks



This function emulates the RPC interface used by the Windows NT 4.0 DHCP server. It is provided for backward compatibility with older versions of the DHCP Administrator application.




## -see-also




<a href="https://msdn.microsoft.com/2ec45a99-432d-4218-9048-81714ceff36b">
        DHCP_FORCE_FLAG</a>



<a href="https://msdn.microsoft.com/ea6df1bc-2d15-4a09-8100-ee17d3de34d9">DHCP_SUBNET_ELEMENT_DATA_V5</a>



<a href="https://msdn.microsoft.com/200fc8da-d05c-4502-9cfc-d1092c5d0417">DhcpAddSubnetElementV5</a>
 

 

