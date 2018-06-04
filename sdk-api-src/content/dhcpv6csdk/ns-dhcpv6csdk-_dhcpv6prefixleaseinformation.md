---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _DHCPV6PrefixLeaseInformation structure


## -description


The <b>DHCPV6PrefixLeaseInformation</b> structure contains information about a prefix lease.


## -struct-fields




### -field nPrefixes

Number of prefixes.


### -field prefixArray

Pointer to a list <a href="https://msdn.microsoft.com/e04e3275-e4be-44bc-bd63-c45500971af7">DHCPV6Prefix</a> structures that contain the prefixes requested or returned by the server.


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
The DHCPv6 server does not have a prefix availble to offer the requesting client.

</td>
</tr>
</table>
 


### -field ServerId

The server DUID from which the prefix is received.  This data is used in subsequent renews.


### -field ServerIdLen

The length of the above DUID data.


## -remarks



In a prefix delegation scenario, the validation of lease lifetime values (specific status codes, <b>T1</b>, <b>T2</b>, <b>MaxLeaseExpirationTime</b>, and <b>LastRenewalTime</b>) are performed by the calling API, rather than the application consuming the data, as the latter might interpret these values differently.



