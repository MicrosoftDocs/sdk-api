---
UID: NF:dhcpsapi.DhcpGetMibInfoV5
title: DhcpGetMibInfoV5 function (dhcpsapi.h)
description: Obtains a MIB data structure that contains current statistics about the specified DHCP server.
helpviewer_keywords: ["DhcpGetMibInfoV5","DhcpGetMibInfoV5 function [DHCP]","dhcp.dhcpgetmibinfov5","dhcpsapi/DhcpGetMibInfoV5"]
old-location: dhcp\dhcpgetmibinfov5.htm
tech.root: DHCP
ms.assetid: 3439198d-5391-4f9b-a6fe-9a600e7dc77b
ms.date: 12/05/2018
ms.keywords: DhcpGetMibInfoV5, DhcpGetMibInfoV5 function [DHCP], dhcp.dhcpgetmibinfov5, dhcpsapi/DhcpGetMibInfoV5
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
 - DhcpGetMibInfoV5
 - dhcpsapi/DhcpGetMibInfoV5
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
 - DhcpGetMibInfoV5
---

# DhcpGetMibInfoV5 function


## -description

The <b>DhcpGetMibInfoV5</b> function obtains a MIB data structure that contains current statistics about the specified DHCP server.

## -parameters

### -param ServerIpAddress [in, optional]

Pointer to a zero-delimited string that contains the IPv4 address of the DHCP server for which statistical information is to be retrieved. This value is specified in the format "*.*.*.*". 

If this parameter is <b>NULL</b>, then the local DHCP server process is queried.

### -param MibInfo [out]

Pointer to the address of a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_mib_info_v5">DHCP_MIB_INFO_V5</a> structure that contains statistical information about the DHCP server specified in the <i>ServerIpAddress</i> parameter.

<div class="alert"><b>Note</b>  <p class="note">The memory for this parameter must be free using <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcprpcfreememory">DhcpRpcFreeMemory</a>.

</div>
<div> </div>

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters provides an invalid value.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_mib_info_v5">DHCP_MIB_INFO_V5</a>