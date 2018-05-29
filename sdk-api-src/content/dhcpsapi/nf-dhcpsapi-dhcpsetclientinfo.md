---
UID: NF:dhcpsapi.DhcpSetClientInfo
title: DhcpSetClientInfo function
author: windows-sdk-content
description: The DhcpSetClientInfo function sets information on a client whose IP address lease is administrated by the DHCP server.
old-location: dhcp\dhcpsetclientinfo.htm
old-project: DHCP
ms.assetid: 1eedddce-8b3e-419e-a065-163b22a0e9a8
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: DhcpSetClientInfo, DhcpSetClientInfo function [DHCP], dhcp.dhcpsetclientinfo, dhcpsapi/DhcpSetClientInfo
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
-	DhcpSetClientInfo
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpSetClientInfo function


## -description



      The <b>DhcpSetClientInfo</b> function sets information on a client whose IP address lease is administrated by the DHCP server.


## -parameters




### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.


### -param ClientInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/cc841dac-85d4-4250-a868-95c41731fe45">DHCP_CLIENT_INFO</a> structure that contains the information on a client in a subnet served by the DHCP server.


## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.




## -remarks



This function requires host byte ordering for all <a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> values in parameter structures.




## -see-also




<a href="https://msdn.microsoft.com/cc841dac-85d4-4250-a868-95c41731fe45">DHCP_CLIENT_INFO</a>



<a href="https://msdn.microsoft.com/67095868-7e02-4d82-b2f0-70c413fa8ed6">DhcpGetClientInfo</a>
 

 

