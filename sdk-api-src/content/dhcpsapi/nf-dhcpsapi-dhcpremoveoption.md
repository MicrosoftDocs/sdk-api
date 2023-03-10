---
UID: NF:dhcpsapi.DhcpRemoveOption
title: DhcpRemoveOption function (dhcpsapi.h)
description: Removes the definition of a specific option for the default user class and vendor class at the default option level on the DHCP server.
helpviewer_keywords: ["DhcpRemoveOption","DhcpRemoveOption function [DHCP]","dhcp.dhcpremoveoption","dhcpsapi/DhcpRemoveOption"]
old-location: dhcp\dhcpremoveoption.htm
tech.root: DHCP
ms.assetid: a165d88c-113c-41ed-920e-f8f434578158
ms.date: 12/05/2018
ms.keywords: DhcpRemoveOption, DhcpRemoveOption function [DHCP], dhcp.dhcpremoveoption, dhcpsapi/DhcpRemoveOption
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
 - DhcpRemoveOption
 - dhcpsapi/DhcpRemoveOption
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
 - DhcpRemoveOption
---

# DhcpRemoveOption function


## -description

The <b>DhcpRemoveOption</b> function removes the definition of a specific option for the default user class and vendor class at the default option level on the DHCP server.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param OptionID [in]

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_OPTION_ID</a> value that contains the code uniquely identifying the specific option to remove from the DHCP server.

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

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpcreateoption">DhcpCreateOption</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpremoveoptionv5">DhcpRemoveOptionV5</a>