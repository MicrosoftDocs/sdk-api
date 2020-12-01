---
UID: NF:dhcpsapi.DhcpV4FailoverSetRelationship
title: DhcpV4FailoverSetRelationship function (dhcpsapi.h)
description: Sets or modifies the parameters of a DHCPv4 server failover relationship.
helpviewer_keywords: ["CHANGESTATE","DhcpV4FailoverSetRelationship","DhcpV4FailoverSetRelationship function [DHCP]","MCLT","MODE","PERCENTAGE","PREVSTATE","SAFEPERIOD","dhcp.dhcpv4failoversetrelationship","dhcpsapi/DhcpV4FailoverSetRelationship"]
old-location: dhcp\dhcpv4failoversetrelationship.htm
tech.root: DHCP
ms.assetid: 04012953-dca3-426f-99de-798870d1eb97
ms.date: 12/05/2018
ms.keywords: CHANGESTATE, DhcpV4FailoverSetRelationship, DhcpV4FailoverSetRelationship function [DHCP], MCLT, MODE, PERCENTAGE, PREVSTATE, SAFEPERIOD, dhcp.dhcpv4failoversetrelationship, dhcpsapi/DhcpV4FailoverSetRelationship
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
 - DhcpV4FailoverSetRelationship
 - dhcpsapi/DhcpV4FailoverSetRelationship
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
 - DhcpV4FailoverSetRelationship
---

# DhcpV4FailoverSetRelationship function


## -description

The <b>DhcpV4FailoverSetRelationship</b> function sets or modifies the parameters of a DHCPv4 server failover relationship.

## -parameters

### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.

### -param Flags [in]

A bitmask that specifies the fields to update in <i>pRelationship</i>. Each value specifies a member of the <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_failover_relationship">DHCP_FAILOVER_RELATIONSHIP</a> structure to be modified. 

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MCLT"></a><a id="mclt"></a><dl>
<dt><b>MCLT</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The <b>mclt</b> member in <i>pRelationship</i> parameter structure is populated.

</td>
</tr>
<tr>
<td width="40%"><a id="SAFEPERIOD"></a><a id="safeperiod"></a><dl>
<dt><b>SAFEPERIOD</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The <b>safePeriod</b> member in <i>pRelationship</i> parameter structure is populated.

</td>
</tr>
<tr>
<td width="40%"><a id="CHANGESTATE"></a><a id="changestate"></a><dl>
<dt><b>CHANGESTATE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The <b>state</b> member in <i>pRelationship</i> parameter structure is populated.

</td>
</tr>
<tr>
<td width="40%"><a id="PERCENTAGE"></a><a id="percentage"></a><dl>
<dt><b>PERCENTAGE</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The <b>percentage</b> member in <i>pRelationship</i> parameter structure is populated.

</td>
</tr>
<tr>
<td width="40%"><a id="MODE"></a><a id="mode"></a><dl>
<dt><b>MODE</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
The <b>mode</b> member in <i>pRelationship</i> parameter structure is populated.

</td>
</tr>
<tr>
<td width="40%"><a id="PREVSTATE"></a><a id="prevstate"></a><dl>
<dt><b>PREVSTATE</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
The <b>prevState</b> member in <i>pRelationship</i> parameter structure is populated.

</td>
</tr>
</table>

### -param pRelationship [in]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_failover_relationship">DHCP_FAILOVER_RELATIONSHIP</a> structure that  contains  update information about the fields in the DHCPv4 failover relationship.

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
The failover relationship doesn’t exist.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failovercreaterelationship">DhcpV4FailoverCreateRelationship</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failoverdeleterelationship">DhcpV4FailoverDeleteRelationship</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failoverenumrelationship">DhcpV4FailoverEnumRelationship</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failovergetrelationship">DhcpV4FailoverGetRelationship</a>