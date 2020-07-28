---
UID: NF:dhcpsapi.DhcpGetOptionInfoV5
title: DhcpGetOptionInfoV5 function (dhcpsapi.h)
description: The DhcpGetOptionInfoV5 function returns information on a specific DHCP option.
helpviewer_keywords: ["DHCP_FLAGS_OPTION_IS_VENDOR","DhcpGetOptionInfoV5","DhcpGetOptionInfoV5 function [DHCP]","dhcp.dhcpgetoptioninfov5","dhcpsapi/DhcpGetOptionInfoV5"]
old-location: dhcp\dhcpgetoptioninfov5.htm
tech.root: DHCP
ms.assetid: bf7b744d-da02-4c2f-b29a-e2b9b3fe3881
ms.date: 12/05/2018
ms.keywords: DHCP_FLAGS_OPTION_IS_VENDOR, DhcpGetOptionInfoV5, DhcpGetOptionInfoV5 function [DHCP], dhcp.dhcpgetoptioninfov5, dhcpsapi/DhcpGetOptionInfoV5
f1_keywords:
- dhcpsapi/DhcpGetOptionInfoV5
dev_langs:
- c++
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
- DhcpGetOptionInfoV5
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DhcpGetOptionInfoV5 function


## -description


The <b>DhcpGetOptionInfoV5</b> function returns information on a specific DHCP option.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.


### -param Flags [in]

Specifies a bit flag that indicates whether or not the option is vendor-specific. If it is not, this parameter should be 0.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
The option value is retrieved for a default vendor class.

</td>
</tr>
<tr>
<td width="40%"><a id="DHCP_FLAGS_OPTION_IS_VENDOR"></a><a id="dhcp_flags_option_is_vendor"></a><dl>
<dt><b>DHCP_FLAGS_OPTION_IS_VENDOR</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
The option value is retrieved for a specific vendor class. The vendor name is supplied in <i>VendorName</i>.

</td>
</tr>
</table>
 


### -param OptionID [in]


<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_OPTION_ID</a> value that specifies the code for the option to retrieve information on.


### -param ClassName [in]

Unicode string that specifies the DHCP  class name of the option. This parameter is optional.


### -param VendorName [in]

Unicode string that specifies the vendor of the option. This parameter is optional, and must be null when <i>Flags</i> is not set to DHCP_FLAGS_OPTION_IS_VENDOR. If it is not set, then the option definition for the default vendor class is returned.


### -param OptionInfo [out]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option">DHCP_OPTION</a> structure that contains the returned information on the option specified by <i>OptionID</i>.

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
<dt><b>ERROR_DHCP_SUBNET_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The specified IPv4 subnet is not defined on the DHCP server.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_OPTION_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The specified option definition does not exist in the DHCP server database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_NOT_RESERVED_CLIENT</b></dt>
</dl>
</td>
<td width="60%">
The specified DHCP client is not a reserved client. o

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option">DHCP_OPTION</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpsetoptioninfov5">DhcpSetOptionInfoV5</a>
 

 

