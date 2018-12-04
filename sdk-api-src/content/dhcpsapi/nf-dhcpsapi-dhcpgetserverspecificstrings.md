---
UID: NF:dhcpsapi.DhcpGetServerSpecificStrings
title: DhcpGetServerSpecificStrings function
author: windows-sdk-content
description: Retrieves the names of the default vendor class and user class.
old-location: dhcp\dhcpgetserverspecificstrings.htm
tech.root: DHCP
ms.assetid: dc283fa3-6077-4010-8c71-9dc91ed2dadf
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DhcpGetServerSpecificStrings, DhcpGetServerSpecificStrings function [DHCP], dhcp.dhcpgetserverspecificstrings, dhcpsapi/DhcpGetServerSpecificStrings
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - DhcpGetServerSpecificStrings
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DhcpGetServerSpecificStrings function


## -description


The <b>DhcpGetServerSpecificStrings</b> function retrieves the names of the default vendor class and user class.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IPv4 address of the DHCPv4 server.


### -param ServerSpecificStrings [out]

Pointer to a <a href="https://msdn.microsoft.com/5fc52d5c-22b0-454b-bc07-8f9c4ca163e3">DHCP_SERVER_SPECIFIC_STRINGS</a> structure that receives the information for the default vendor class and user class name strings.

<div class="alert"><b>Note</b>  <p class="note">The memory for this parameter must be free using <a href="https://msdn.microsoft.com/bf22a0a6-2ecd-4460-89c4-3f870c6275dc">DhcpRpcFreeMemory</a>.

</div>
<div> </div>

## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_JET_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred while accessing the DHCP server database.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5fc52d5c-22b0-454b-bc07-8f9c4ca163e3">DHCP_SERVER_SPECIFIC_STRINGS</a>
 

 

