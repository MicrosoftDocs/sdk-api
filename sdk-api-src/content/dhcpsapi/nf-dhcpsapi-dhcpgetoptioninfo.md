---
UID: NF:dhcpsapi.DhcpGetOptionInfo
title: DhcpGetOptionInfo function (dhcpsapi.h)
author: windows-sdk-content
description: Returns information on a specific DHCP option for the default user and vendor class.
old-location: dhcp\dhcpgetoptioninfo.htm
tech.root: DHCP
ms.assetid: b62b0a07-3043-417d-affe-d3a350907f4e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DhcpGetOptionInfo, DhcpGetOptionInfo function [DHCP], dhcp.dhcpgetoptioninfo, dhcpsapi/DhcpGetOptionInfo
ms.topic: function
f1_keywords: 
 - "dhcpsapi/DhcpGetOptionInfo"
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
 - DhcpGetOptionInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DhcpGetOptionInfo function


## -description


The <b>DhcpGetOptionInfo</b> function returns information on a specific DHCP option for the default user and vendor class.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IPv4 address of the DHCP server.


### -param OptionID [in]


<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_OPTION_ID</a> value that specifies the code for the option to retrieve information on.


### -param OptionInfo [out]

Pointer to a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/ns-dhcpsapi-_dhcp_option">DHCP_OPTION</a> structure that contains the returned information on the option specified by <i>OptionID</i>.

<div class="alert"><b>Note</b>  <p class="note">The memory for this parameter must be free using <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcprpcfreememory">DhcpRpcFreeMemory</a>.

</div>
<div> </div>

## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

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
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_OPTION_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The specified option definition could not be found in the DHCP server database.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/ns-dhcpsapi-_dhcp_option">DHCP_OPTION</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpgetoptioninfov5">DhcpGetOptionInfoV5</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpsetoptioninfo">DhcpSetOptionInfo</a>
 

 

