---
UID: NF:dhcpsapi.DhcpCreateClientInfo
title: DhcpCreateClientInfo function
author: windows-sdk-content
description: The DhcpCreateClientInfo function creates a client information record on the DHCP server.
old-location: dhcp\dhcpcreateclientinfo.htm
old-project: DHCP
ms.assetid: 121718db-a7d8-42b7-b1a1-5c2dbe7d3d6b
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: DhcpCreateClientInfo, DhcpCreateClientInfo function [DHCP], dhcp.dhcpcreateclientinfo, dhcpsapi/DhcpCreateClientInfo
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
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Dhcpsapi.dll
api_name:
-	DhcpCreateClientInfo
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpCreateClientInfo function


## -description



      The <b>DhcpCreateClientInfo</b> function creates a client information record on the DHCP server.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.


### -param ClientInfo [in]


<a href="https://msdn.microsoft.com/cc841dac-85d4-4250-a868-95c41731fe45">DHCP_CLIENT_INFO</a> structure that contains information about the DHCP client, including the assigned IP address, subnet mask, and host.


## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.




## -remarks



This function requires host byte ordering for all <a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> values in parameter structures.




## -see-also




<a href="https://msdn.microsoft.com/cc841dac-85d4-4250-a868-95c41731fe45">DHCP_CLIENT_INFO</a>



<a href="https://msdn.microsoft.com/abbf4843-2a4f-4d09-9a21-33587ad0d3e8">DhcpDeleteClientInfo</a>
 

 

