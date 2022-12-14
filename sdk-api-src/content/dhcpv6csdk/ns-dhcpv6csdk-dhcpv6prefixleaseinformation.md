---
UID: NS:dhcpv6csdk._DHCPV6PrefixLeaseInformation
title: DHCPV6PrefixLeaseInformation (dhcpv6csdk.h)
description: Information about a prefix lease.
helpviewer_keywords: ["*LPDHCPV6PrefixLeaseInformation","*PDHCPV6PrefixLeaseInformation","DHCPV6PrefixLeaseInformation","DHCPV6PrefixLeaseInformation structure [DHCP]","LPDHCPV6PrefixLeaseInformation","LPDHCPV6PrefixLeaseInformation structure pointer [DHCP]","PDHCPV6PrefixLeaseInformation","PDHCPV6PrefixLeaseInformation structure pointer [DHCP]","STATUS_NOPREFIX_AVAIL","STATUS_NO_BINDING","STATUS_NO_ERROR","STATUS_UNSPECIFIED_FAILURE","dhcp.dhcpv6prefixleaseinformation","dhcpv6csdk/DHCPV6PrefixLeaseInformation","dhcpv6csdk/LPDHCPV6PrefixLeaseInformation","dhcpv6csdk/PDHCPV6PrefixLeaseInformation"]
old-location: dhcp\dhcpv6prefixleaseinformation.htm
tech.root: DHCP
ms.assetid: d3e76716-a8cc-4618-a85f-d8fb9ca3257e
ms.date: 12/05/2018
ms.keywords: '*LPDHCPV6PrefixLeaseInformation, *PDHCPV6PrefixLeaseInformation, DHCPV6PrefixLeaseInformation, DHCPV6PrefixLeaseInformation structure [DHCP], LPDHCPV6PrefixLeaseInformation, LPDHCPV6PrefixLeaseInformation structure pointer [DHCP], PDHCPV6PrefixLeaseInformation, PDHCPV6PrefixLeaseInformation structure pointer [DHCP], STATUS_NOPREFIX_AVAIL, STATUS_NO_BINDING, STATUS_NO_ERROR, STATUS_UNSPECIFIED_FAILURE, dhcp.dhcpv6prefixleaseinformation, dhcpv6csdk/DHCPV6PrefixLeaseInformation, dhcpv6csdk/LPDHCPV6PrefixLeaseInformation, dhcpv6csdk/PDHCPV6PrefixLeaseInformation'
req.header: dhcpv6csdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DHCPV6PrefixLeaseInformation, *PDHCPV6PrefixLeaseInformation, *LPDHCPV6PrefixLeaseInformation
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCPV6PrefixLeaseInformation
 - dhcpv6csdk/_DHCPV6PrefixLeaseInformation
 - PDHCPV6PrefixLeaseInformation
 - dhcpv6csdk/PDHCPV6PrefixLeaseInformation
 - DHCPV6PrefixLeaseInformation
 - dhcpv6csdk/DHCPV6PrefixLeaseInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpv6csdk.h
api_name:
 - DHCPV6PrefixLeaseInformation
---

# DHCPV6PrefixLeaseInformation structure


## -description

The <b>DHCPV6PrefixLeaseInformation</b> structure contains information about a prefix lease.

## -struct-fields

### -field nPrefixes

Number of prefixes.

### -field prefixArray

Pointer to a list <a href="/windows/desktop/api/dhcpv6csdk/ns-dhcpv6csdk-dhcpv6prefix">DHCPV6Prefix</a> structures that contain the prefixes requested or returned by the server.

### -field iaid

Identity Association identifier for the prefix operation.

### -field T1

The renewal time for the prefix, in seconds.

### -field T2

The rebind time of the prefix, in seconds.

### -field MaxLeaseExpirationTime

The maximum lease expiration time of all the prefix leases in this structure.

### -field LastRenewalTime

The time at which the last renewal for the prefixes occurred.

### -field status

Status code returned by the server for the IAPD. The following codes can be returned by the DHCP server for prefix delegation scenarios:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="STATUS_NO_ERROR"></a><a id="status_no_error"></a><dl>
<dt><b>STATUS_NO_ERROR</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The prefix was successfully leased or renewed.

</td>
</tr>
<tr>
<td width="40%"><a id="STATUS_UNSPECIFIED_FAILURE"></a><a id="status_unspecified_failure"></a><dl>
<dt><b>STATUS_UNSPECIFIED_FAILURE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The lease or renewal action failed for an unspecified reason.

</td>
</tr>
<tr>
<td width="40%"><a id="STATUS_NO_BINDING"></a><a id="status_no_binding"></a><dl>
<dt><b>STATUS_NO_BINDING</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The DHCPv6 server does not have a binding for the prefix.

</td>
</tr>
<tr>
<td width="40%"><a id="STATUS_NOPREFIX_AVAIL"></a><a id="status_noprefix_avail"></a><dl>
<dt><b>STATUS_NOPREFIX_AVAIL</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
The DHCPv6 server does not have a prefix available to offer the requesting client.

</td>
</tr>
</table>

### -field ServerId

The server DUID from which the prefix is received.  This data is used in subsequent renews.

### -field ServerIdLen

The length of the above DUID data.

## -remarks

In a prefix delegation scenario, the validation of lease lifetime values (specific status codes, <b>T1</b>, <b>T2</b>, <b>MaxLeaseExpirationTime</b>, and <b>LastRenewalTime</b>) are performed by the calling API, rather than the application consuming the data, as the latter might interpret these values differently.