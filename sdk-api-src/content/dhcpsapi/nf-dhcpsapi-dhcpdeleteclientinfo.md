---
UID: NF:dhcpsapi.DhcpDeleteClientInfo
title: DhcpDeleteClientInfo function
author: windows-sdk-content
description: The DhcpDeleteClientInfo function deletes a client information record from the DHCP server.
old-location: dhcp\dhcpdeleteclientinfo.htm
old-project: dhcp
ms.assetid: abbf4843-2a4f-4d09-9a21-33587ad0d3e8
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: DhcpDeleteClientInfo, DhcpDeleteClientInfo function [DHCP], dhcp.dhcpdeleteclientinfo, dhcpsapi/DhcpDeleteClientInfo
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
 - DhcpDeleteClientInfo
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpDeleteClientInfo function


## -description



      The <b>DhcpDeleteClientInfo</b> function deletes a client information record from the DHCP server.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.


### -param ClientInfo [in]


<a href="https://msdn.microsoft.com/3c6f85d7-c156-4379-bad9-0705698f12e5">DHCP_SEARCH_INFO</a> union structure that contains one of the following items used to search the DHCP client record database: the client IP address, the client MAC address, or the client network name. All records matching the value will be deleted; for example, if a client IP address of 192.1.1.10 is supplied, all records with this address in the <b>ClientIpAddress</b> field will be deleted.


## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.




## -remarks



This function requires host byte ordering for all <a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> values in parameter structures.




## -see-also




<a href="https://msdn.microsoft.com/3c6f85d7-c156-4379-bad9-0705698f12e5">DHCP_SEARCH_INFO</a>



<a href="https://msdn.microsoft.com/121718db-a7d8-42b7-b1a1-5c2dbe7d3d6b">DhcpCreateClientInfo</a>
 

 

