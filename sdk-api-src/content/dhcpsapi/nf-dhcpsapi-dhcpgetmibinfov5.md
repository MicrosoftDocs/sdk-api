---
UID: NF:dhcpsapi.DhcpGetMibInfoV5
title: DhcpGetMibInfoV5 function
author: windows-sdk-content
description: Obtains a MIB data structure that contains current statistics about the specified DHCP server.
old-location: dhcp\dhcpgetmibinfov5.htm
tech.root: DHCP
ms.assetid: 3439198d-5391-4f9b-a6fe-9a600e7dc77b
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: DhcpGetMibInfoV5, DhcpGetMibInfoV5 function [DHCP], dhcp.dhcpgetmibinfov5, dhcpsapi/DhcpGetMibInfoV5
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
 - DhcpGetMibInfoV5
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DhcpGetMibInfoV5 function


## -description


The <b>DhcpGetMibInfoV5</b> function obtains a MIB data structure that contains current statistics about the specified DHCP server.


## -parameters




### -param ServerIpAddress [in, optional]

Pointer to a zero-delimited string that contains the IPv4 address of the DHCP server for which statistical information is to be retrieved. This value is specified in the format "*.*.*.*". 

If this parameter is <b>NULL</b>, then the local DHCP server process is queried.


### -param MibInfo [out]

Pointer to the address of a <a href="https://msdn.microsoft.com/5081ebce-d3b9-4548-8d80-23d994bce7ab">DHCP_MIB_INFO_V5</a> structure that contains statistical information about the DHCP server specified in the <i>ServerIpAddress</i> parameter.

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
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters provides an invalid value.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5081ebce-d3b9-4548-8d80-23d994bce7ab">DHCP_MIB_INFO_V5</a>
 

 

