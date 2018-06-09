---
UID: NF:dhcpsapi.DhcpSetOptionInfoV5
title: DhcpSetOptionInfoV5 function
author: windows-sdk-content
description: Sets information for a specific DHCP option.
old-location: dhcp\dhcpsetoptioninfov5.htm
old-project: DHCP
ms.assetid: 2a58706e-dfae-418e-867a-328830d47d5b
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: DHCP_FLAGS_OPTION_IS_VENDOR, DhcpSetOptionInfoV5, DhcpSetOptionInfoV5 function [DHCP], dhcp.dhcpsetoptioninfov5, dhcpsapi/DhcpSetOptionInfoV5
ms.prod: windows
ms.technology: windows-sdk
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
 - DhcpSetOptionInfoV5
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpSetOptionInfoV5 function


## -description


The <b>DhcpSetOptionInfoV5</b> function sets information for a specific DHCP option. 


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
<td width="40%"><a id="DHCP_FLAGS_OPTION_IS_VENDOR"></a><a id="dhcp_flags_option_is_vendor"></a><dl>
<dt><b>DHCP_FLAGS_OPTION_IS_VENDOR</b></dt>
</dl>
</td>
<td width="60%">
This flag should be set if the option is provided by a vendor.

</td>
</tr>
</table>
 


### -param OptionID [in]


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_OPTION_ID</a> value that specifies the code for a specific DHCP option.


### -param ClassName [in]

Pointer to a  Unicode string that specifies the DHCP  class name of the option. This parameter is optional.


### -param VendorName [in]

Pointer to a Unicode string that specifies the vendor of the option. This parameter is optional, and should be <b>NULL</b> when <i>Flags</i> is not set to DHCP_FLAGS_OPTION_IS_VENDOR.


### -param OptionInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/1be34eb4-a226-4f07-b763-173a4f8a0671">DHCP_OPTION</a> structure that contains the information on the option specified by <i>OptionID</i>.


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
An error occurred while accessing the DHCPv6 server's database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_CLASS_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The provided class name is either incorrect or does not exist on the DHCP server.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1be34eb4-a226-4f07-b763-173a4f8a0671">
        DHCP_OPTION</a>



<a href="https://msdn.microsoft.com/bf7b744d-da02-4c2f-b29a-e2b9b3fe3881">DhcpGetOptionInfoV5</a>
 

 

