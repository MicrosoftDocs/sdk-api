---
UID: NF:dhcpsapi.DhcpRemoveOptionV6
title: DhcpRemoveOptionV6 function
author: windows-sdk-content
description: The DhcpRemoveOptionV6 function removes an option defined on the DHCP server.
old-location: dhcp\dhcpremoveoptionv6.htm
old-project: DHCP
ms.assetid: fccd07f2-b796-46b9-a004-edefa92ed08c
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: DHCP_FLAGS_OPTION_IS_VENDOR, DhcpRemoveOptionV6, DhcpRemoveOptionV6 function [DHCP], dhcp.dhcpremoveoptionv6, dhcpsapi/DhcpRemoveOptionV6
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
-	DhcpRemoveOptionV6
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpRemoveOptionV6 function


## -description


The <b>DhcpRemoveOptionV6</b> function removes an option defined on the DHCP server..


## -parameters




### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.


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


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_OPTION_ID</a> value that specifies the code for the option  to remove.


### -param ClassName [in]

Unicode string that specifies the DHCP  class name of the option. This parameter is optional.


### -param VendorName [in]

Unicode string that specifies the vendor of the option. This parameter is optional, and should be <b>NULL</b> when <i>Flags</i> is not set to DHCP_FLAGS_OPTION_IS_VENDOR.


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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The parameters were invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_OPTION_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The specified option is not present on the DHCP server.

</td>
</tr>
</table>
 



