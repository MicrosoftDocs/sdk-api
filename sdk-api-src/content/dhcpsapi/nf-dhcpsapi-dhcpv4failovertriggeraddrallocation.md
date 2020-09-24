---
UID: NF:dhcpsapi.DhcpV4FailoverTriggerAddrAllocation
title: DhcpV4FailoverTriggerAddrAllocation function (dhcpsapi.h)
description: Redistributes the free addresses between the primary server and the secondary server that are part of a failover relationship.
helpviewer_keywords: ["DhcpV4FailoverTriggerAddrAllocation","DhcpV4FailoverTriggerAddrAllocation function [DHCP]","dhcp.dhcpv4failovertriggeraddrallocation","dhcpsapi/DhcpV4FailoverTriggerAddrAllocation"]
old-location: dhcp\dhcpv4failovertriggeraddrallocation.htm
tech.root: DHCP
ms.assetid: ff258179-1091-4338-9317-68fd8fe5a556
ms.date: 12/05/2018
ms.keywords: DhcpV4FailoverTriggerAddrAllocation, DhcpV4FailoverTriggerAddrAllocation function [DHCP], dhcp.dhcpv4failovertriggeraddrallocation, dhcpsapi/DhcpV4FailoverTriggerAddrAllocation
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - DhcpV4FailoverTriggerAddrAllocation
 - dhcpsapi/DhcpV4FailoverTriggerAddrAllocation
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
 - DhcpV4FailoverTriggerAddrAllocation
---

# DhcpV4FailoverTriggerAddrAllocation function


## -description

The <b>DhcpV4FailoverTriggerAddrAllocation</b> function redistributes the free addresses between the primary server and the secondary server that are part of a failover relationship.

## -parameters

### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.

### -param pFailRelName [in]

Pointer to a null-terminated Unicode string that represents the name of the failover relationship for which free addresses are to be redistributed.

## -returns

If the function succeeds, it returns <b>ERROR_SUCCESS</b>.

If the function fails, it returns one of the following or an error code from <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters were invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_FO_RELATIONSHIP_DOES_NOT_EXIST</b></dt>
</dl>
</td>
<td width="60%">
Failover relationship doesn't exit.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_FO_RELATION_IS_SECONDARY</b></dt>
</dl>
</td>
<td width="60%">
The <b>serverType</b> member of failover relationship is <b>SecondaryServer</b>.

</td>
</tr>
</table>