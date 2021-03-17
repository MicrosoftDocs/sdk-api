---
UID: NF:dhcpsapi.DhcpRemoveOptionV5
title: DhcpRemoveOptionV5 function (dhcpsapi.h)
description: Removes the definition of a specific option for a specific user class and vendor class at the default option level on the DHCP server. This extends the functionality in DhcpRemoveOption with support for specific class and vendor names.
helpviewer_keywords: ["DHCP_FLAGS_OPTION_IS_VENDOR","DhcpRemoveOptionV5","DhcpRemoveOptionV5 function [DHCP]","dhcp.dhcpremoveoptionv5","dhcpsapi/DhcpRemoveOptionV5"]
old-location: dhcp\dhcpremoveoptionv5.htm
tech.root: DHCP
ms.assetid: 53b57879-7533-4e92-a179-d6786052ad46
ms.date: 12/05/2018
ms.keywords: DHCP_FLAGS_OPTION_IS_VENDOR, DhcpRemoveOptionV5, DhcpRemoveOptionV5 function [DHCP], dhcp.dhcpremoveoptionv5, dhcpsapi/DhcpRemoveOptionV5
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DhcpRemoveOptionV5
 - dhcpsapi/DhcpRemoveOptionV5
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dhcpsapi.dll
api_name:
 - DhcpRemoveOptionV5
---

# DhcpRemoveOptionV5 function


## -description

The <b>DhcpRemoveOptionV5</b> function removes the definition of a specific option for a specific user class and vendor class at the default option level on the DHCP server.  This extends the functionality in <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpremoveoption">DhcpRemoveOption</a> with support for specific class and vendor names.

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
This flag should be set if the option is removed for the default vendor class..

</td>
</tr>
<tr>
<td width="40%"><a id="DHCP_FLAGS_OPTION_IS_VENDOR"></a><a id="dhcp_flags_option_is_vendor"></a><dl>
<dt><b>DHCP_FLAGS_OPTION_IS_VENDOR</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
This flag should be set if the option is removed for a specific vendor class..

</td>
</tr>
</table>

### -param OptionID [in]

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_OPTION_ID</a> value that specifies the code for the option  to remove.

### -param ClassName [in]

Unicode string that specifies the DHCP  class name of the option. This parameter is optional.

### -param VendorName [in]

Unicode string that specifies the vendor of the option. This parameter is optional, and should be <b>NULL</b> when <i>Flags</i> is not set to DHCP_FLAGS_OPTION_IS_VENDOR.

## -returns

This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

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
<dt><b>ERROR_DHCP_CLASS_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The supplied class name is either unknown or incorrect.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpcreateoptionv5">DhcpCreateOptionV5</a>