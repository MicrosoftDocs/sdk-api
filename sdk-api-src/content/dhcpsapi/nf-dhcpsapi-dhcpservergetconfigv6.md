---
UID: NF:dhcpsapi.DhcpServerGetConfigV6
title: DhcpServerGetConfigV6 function
author: windows-driver-content
description: Retrieves the configuration information for the DHCPv6 server.
old-location: dhcp\dhcpservergetconfigv6.htm
old-project: DHCP
ms.assetid: a867d8fe-0222-44aa-a00a-65a94cf59730
ms.author: windowsdriverdev
ms.date: 5/2/2018
ms.keywords: DhcpServerGetConfigV6, DhcpServerGetConfigV6 function [DHCP], dhcp.dhcpservergetconfigv6, dhcpsapi/DhcpServerGetConfigV6
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
req.typenames: QuarantineStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Dhcpsapi.dll
api_name:
-	DhcpServerGetConfigV6
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpServerGetConfigV6 function


## -description


The <b>DhcpServerGetConfigV6</b> function retrieves the configuration information for the DHCPv6 server.


## -parameters




### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.


### -param ScopeInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/d5c0cff9-7164-4f14-a0a9-58311390ebd9">DHCP_OPTION_SCOPE_INFO6</a> structure used to identify the DHCPv6 scope for which configuration information will be retrieved.


### -param ConfigInfo [out]

Pointer to the address of a  <a href="https://msdn.microsoft.com/9862f0c1-3c42-4ad7-af3c-15868e4a9314">DHCP_SERVER_CONFIG_INFO_V6</a> structure that contains the requested configuration information.

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
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
This call was performed by a client who is not a member of the "DHCP Administrators" security group.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_JET_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred while accessing the DHCP server's database.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d5c0cff9-7164-4f14-a0a9-58311390ebd9">DHCP_OPTION_SCOPE_INFO6</a>



<a href="https://msdn.microsoft.com/9862f0c1-3c42-4ad7-af3c-15868e4a9314">DHCP_SERVER_CONFIG_INFO_V6</a>
 

 

