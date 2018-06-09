---
UID: NF:dhcpsapi.DhcpCreateOptionV5
title: DhcpCreateOptionV5 function
author: windows-sdk-content
description: Creates a DHCP option.
old-location: dhcp\dhcpcreateoptionv5.htm
old-project: DHCP
ms.assetid: de6e8f87-af4b-4e7f-8468-54359c5a8907
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: DHCP_FLAGS_OPTION_IS_VENDOR, DhcpCreateOptionV5, DhcpCreateOptionV5 function [DHCP], dhcp.dhcpcreateoptionv5, dhcpsapi/DhcpCreateOptionV5
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
 - DhcpCreateOptionV5
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpCreateOptionV5 function


## -description


The <b>DhcpCreateOptionV5</b> function creates a DHCP option.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.


### -param Flags [in]

Flag value that indicates whether the option is for a specific or default vendor class.

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
 


### -param OptionId [in]


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_OPTION_ID</a> value that contains the unique option ID number (also called an "option code") of the new option. Many of these option ID numbers are defined; a complete list of standard DHCP and BOOTP option codes can be found in  <a href="http://go.microsoft.com/fwlink/p/?linkid=84033">DHCP Options and BOOTP Vendor Extensions</a>.


### -param ClassName [in, optional]

Unicode string that specifies the name of the DHCP class that will contain this option. This field is optional.


### -param VendorName [in, optional]

Unicode string that contains a vendor name string if the class specified in <i>ClassName</i> is a vendor-specific class.


### -param OptionInfo [in]


<a href="https://msdn.microsoft.com/1be34eb4-a226-4f07-b763-173a4f8a0671">DHCP_OPTION</a> structure that contains information describing the new   DHCP option, including the name, an optional comment, and any related data items.


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
<dt><b>ERROR_DHCP_OPTION_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The specified option definition already exists in the DHCP server database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_CLASS_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified class name is unknown or incorrectly formed.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1be34eb4-a226-4f07-b763-173a4f8a0671"> DHCP_OPTION</a>
 

 

