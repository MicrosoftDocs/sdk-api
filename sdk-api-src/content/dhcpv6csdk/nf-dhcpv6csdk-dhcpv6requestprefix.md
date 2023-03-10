---
UID: NF:dhcpv6csdk.Dhcpv6RequestPrefix
title: Dhcpv6RequestPrefix function (dhcpv6csdk.h)
description: Requests a specific prefix.
helpviewer_keywords: ["Dhcpv6RequestPrefix","Dhcpv6RequestPrefix function [DHCP]","dhcp.dhcpv6requestprefix","dhcpv6csdk/Dhcpv6RequestPrefix"]
old-location: dhcp\dhcpv6requestprefix.htm
tech.root: DHCP
ms.assetid: 60f18e54-a0a4-4fbe-a416-16b924ce4616
ms.date: 12/05/2018
ms.keywords: Dhcpv6RequestPrefix, Dhcpv6RequestPrefix function [DHCP], dhcp.dhcpv6requestprefix, dhcpv6csdk/Dhcpv6RequestPrefix
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
req.lib: Dhcpcsvc6.lib
req.dll: Dhcpcsvc6.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Dhcpv6RequestPrefix
 - dhcpv6csdk/Dhcpv6RequestPrefix
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dhcpcsvc6.dll
api_name:
 - Dhcpv6RequestPrefix
---

# Dhcpv6RequestPrefix function


## -description

The <b>Dhcpv6RequestPrefix</b> function requests a specific prefix.

## -parameters

### -param adapterName [in]

GUID of the adapter on which the prefix request must be sent.

### -param pclassId [in]

Pointer to a <a href="/windows/desktop/api/dhcpv6csdk/ns-dhcpv6csdk-dhcpv6capi_classid">DHCPV6CAPI_CLASSID</a> structure that contains the binary ClassId information to  send on the wire. This parameter is optional.

<div class="alert"><b>Note</b>  DHCPv6 Option Code 15 (0x000F) is not supported by this API. Typically, the User Class option is used by a client to identify the type or category of user or application it represents. A server selects the configuration information for the client based on the classes identified in this option.</div>
<div> </div>

### -param prefixleaseInfo [in, out]

Pointer to a <a href="/windows/desktop/api/dhcpv6csdk/ns-dhcpv6csdk-dhcpv6prefixleaseinformation">DHCPV6PrefixLeaseInformation</a> structure that contains the prefix lease information.

The following members of the <a href="/windows/desktop/api/dhcpv6csdk/ns-dhcpv6csdk-dhcpv6prefixleaseinformation">DHCPV6PrefixLeaseInformation</a> structure must follow these guidelines.

<table>
<tr>
<th>
<a href="/windows/desktop/api/dhcpv6csdk/ns-dhcpv6csdk-dhcpv6prefixleaseinformation">DHCPV6PrefixLeaseInformation</a> member</th>
<th>Consideration</th>
</tr>
<tr>
<td><b>nPrefixes</b></td>
<td>Must contain a maximum value of 10. The caller should have the memory allocated in the   <b>prefixArray</b> member based on the number of prefixes specified.
 </td>
</tr>
<tr>
<td><b>iaid</b></td>
<td>A unique positive number assigned to this member. This same value should be reused if this function is called again.This mandatory value must be set by the calling application.

</td>
</tr>
<tr>
<td><b>ServerIdLen</b></td>
<td>Must contain a maximum value of 128. The caller must have the memory allocated in the <b>ServerId</b> member based on the specified <b>ServerIdLen</b> value.</td>
</tr>
</table>
 

The caller must follow these considerations when assigning the values of the <b>nPrefixes</b>,  <b>iaid</b>, and <b>ServerIdLen</b> members of the <a href="/windows/desktop/api/dhcpv6csdk/ns-dhcpv6csdk-dhcpv6prefixleaseinformation">DHCPV6PrefixLeaseInformation</a> structure.  Based on these values, memory must also be  properly allocated to the <b>ServerId</b> and <b>PrefixArray</b> members before the <b>Dhcpv6RequestPrefix</b> function is called.

### -param pdwTimeToWait [out]

Contains the number of seconds a requesting application needs to wait before calling the <a href="/previous-versions/windows/desktop/api/dhcpv6csdk/nf-dhcpv6csdk-dhcpv6renewprefix">Dhcpv6RenewPrefix</a> function to renew its acquired prefixes.  A value of 0xFFFFFFFF indicates that the application does not need to renew its lease.

## -returns

Returns ERROR_SUCCESS upon successful completion.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The value of the <b>nPrefixes</b> or the <b>ServerIdLen</b> member specified is less than the number of prefixes available from the server or the available server ID length. Increase the <b>nPrefixes</b> or the <b>ServerIdLen</b> member  and make sure the corresponding memory has been allocated properly before calling the <a href="/previous-versions/windows/desktop/api/dhcpv6csdk/nf-dhcpv6csdk-dhcpv6requestprefix">Dhcpv6RequestPrefix</a> function again.


</td>
</tr>

<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
Returned if one of the following conditions are true:

<ul>
<li><i>AdapterName</i> is <b>NULL</b>. Or no adapter is found with the GUID specified. </li>
<li><i>prefixleaseInfo</i> is <b>NULL</b>.</li>
<li><i>pdwTimeToWait</i> is <b>NULL</b>.</li>
<li>The <b>iaid</b> member of the <i>prefixleaseInfo</i> is zero.</li>
</ul>
</td>
</tr>


<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_NAME</b></dt>
</dl>
</td>
<td width="60%">
The <i>AdapterName</i> is not in the correct format. It should be in this format: {00000000-0000-0000-0000-000000000000}.

</td>
</tr>

</table>