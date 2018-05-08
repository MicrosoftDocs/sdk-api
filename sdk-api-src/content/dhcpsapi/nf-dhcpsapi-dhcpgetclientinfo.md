---
UID: NF:dhcpsapi.DhcpGetClientInfo
title: DhcpGetClientInfo function
author: windows-driver-content
description: The DhcpGetClientInfo function returns information about a specific DHCP client.
old-location: dhcp\dhcpgetclientinfo.htm
old-project: DHCP
ms.assetid: 67095868-7e02-4d82-b2f0-70c413fa8ed6
ms.author: windowsdriverdev
ms.date: 5/2/2018
ms.keywords: DhcpGetClientInfo, DhcpGetClientInfo function [DHCP], dhcp.dhcpgetclientinfo, dhcpsapi/DhcpGetClientInfo
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
req.typenames: QuarantineStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Dhcpsapi.dll
api_name:
-	DhcpGetClientInfo
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpGetClientInfo function


## -description



      The <b>DhcpGetClientInfo</b> function returns information about  a specific DHCP client.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.


### -param SearchInfo [in]


<a href="https://msdn.microsoft.com/3c6f85d7-c156-4379-bad9-0705698f12e5">DHCP_SEARCH_INFO</a> structure that contains the parameters for the search.


### -param ClientInfo [out]

Pointer to a  <a href="https://msdn.microsoft.com/cc841dac-85d4-4250-a868-95c41731fe45">DHCP_CLIENT_INFO</a> structure that contains information describing the DHCP client that most closely matches the provided search parameters. If no client is found, this parameter will be null.

<div class="alert"><b>Note</b>  <p class="note">The memory for this parameter must be free using <a href="https://msdn.microsoft.com/bf22a0a6-2ecd-4460-89c4-3f870c6275dc">DhcpRpcFreeMemory</a>.

</div>
<div> </div>

## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.




## -remarks



This function requires host byte ordering for all <a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> values in parameter structures.




## -see-also




<a href="https://msdn.microsoft.com/cc841dac-85d4-4250-a868-95c41731fe45">
		  DHCP_CLIENT_INFO</a>



<a href="https://msdn.microsoft.com/3c6f85d7-c156-4379-bad9-0705698f12e5">DHCP_SEARCH_INFO</a>



<a href="https://msdn.microsoft.com/1eedddce-8b3e-419e-a065-163b22a0e9a8">DhcpSetClientInfo</a>
 

 

