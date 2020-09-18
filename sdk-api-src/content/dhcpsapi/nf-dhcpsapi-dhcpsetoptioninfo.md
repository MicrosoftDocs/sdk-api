---
UID: NF:dhcpsapi.DhcpSetOptionInfo
title: DhcpSetOptionInfo function (dhcpsapi.h)
description: Modifies the option definition of the specified option for the default user class and vendor class at the default option level.
helpviewer_keywords: ["DhcpSetOptionInfo","DhcpSetOptionInfo function [DHCP]","dhcp.dhcpsetoptioninfo","dhcpsapi/DhcpSetOptionInfo"]
old-location: dhcp\dhcpsetoptioninfo.htm
tech.root: DHCP
ms.assetid: 97cfe347-f4ca-4512-a33a-4da4532c4290
ms.date: 12/05/2018
ms.keywords: DhcpSetOptionInfo, DhcpSetOptionInfo function [DHCP], dhcp.dhcpsetoptioninfo, dhcpsapi/DhcpSetOptionInfo
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
 - DhcpSetOptionInfo
 - dhcpsapi/DhcpSetOptionInfo
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
 - DhcpSetOptionInfo
---

# DhcpSetOptionInfo function


## -description

The <b>DhcpSetOptionInfo</b> function 

modifies the option definition of the specified option for the default user class and vendor class at the default option level.

## -parameters

### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.

### -param OptionID [in]

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_OPTION_ID</a> value that contains the code uniquely identifying a specific DHCP option.

### -param OptionInfo [in]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option">DHCP_OPTION</a> structure that contains  information on the option specified by <i>OptionID</i>.

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

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option">DHCP_OPTION</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpgetoptioninfo">DhcpGetOptionInfo</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpsetoptioninfov5">DhcpSetOptionInfoV5</a>