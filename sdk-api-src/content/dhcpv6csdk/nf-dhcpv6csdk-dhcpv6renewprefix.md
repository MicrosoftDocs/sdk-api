---
UID: NF:dhcpv6csdk.Dhcpv6RenewPrefix
title: Dhcpv6RenewPrefix function (dhcpv6csdk.h)
author: windows-sdk-content
description: Renews a prefix.
old-location: dhcp\dhcpv6renewprefix.htm
tech.root: DHCP
ms.assetid: e4eec40c-0e95-47f7-b102-daa63e5a8da0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Dhcpv6RenewPrefix, Dhcpv6RenewPrefix function [DHCP], dhcp.dhcpv6renewprefix, dhcpv6csdk/Dhcpv6RenewPrefix
ms.topic: function
f1_keywords:
- dhcpv6csdk/Dhcpv6RenewPrefix
dev_langs:
 - c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Dhcpcsvc6.dll
api_name:
- Dhcpv6RenewPrefix
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Dhcpv6RenewPrefix function


## -description


The <b>Dhcpv6RenewPrefix</b> function renews a prefix previously acquired with the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpv6csdk/nf-dhcpv6csdk-dhcpv6requestprefix">Dhcpv6RequestPrefix</a> function.


## -parameters




### -param adapterName [in]

Name of the adapter on which the prefix renewal must be sent.


### -param pclassId [in]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/dhcpv6csdk/ns-dhcpv6csdk-dhcpv6capi_classid">DHCPV6CAPI_CLASSID</a> structure that contains the binary ClassId information to send on the wire.

<div class="alert"><b>Note</b>  DHCPv6 Option Code 15 (0x000F) is not supported by this API. Typically, the User Class option is used by a client to identify the type or category of user or application it represents. A server selects the configuration information for the client based on the classes identified in this option.</div>
<div> </div>

### -param prefixleaseInfo [in, out]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/dhcpv6csdk/ns-dhcpv6csdk-dhcpv6prefixleaseinformation">DHCPV6PrefixLeaseInformation</a> structure that contains the prefix lease information.


### -param pdwTimeToWait [out]

Contains the number of seconds a requesting application needs to wait before calling the <b>Dhcpv6RenewPrefix</b> function to renew its acquired prefixes.  A value of 0xFFFFFFFF indicates that the application does not need to renew its lease.


### -param bValidatePrefix [in]

Specifies  to the DHCPv6 client whether or not to send a REBIND in order to validate the prefix bindings.  <b>TRUE</b> indicates that a REBIND is required.  <b>FALSE</b> indicates RENEW is required.


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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
Returned if one of the following conditions are true:

<ul>
<li><i>AdapterName</i> is <b>NULL</b>.</li>
<li><i>prefixleaseInfo</i> is <b>NULL</b>.</li>
<li><i>pdwTimeToWait</i> is <b>NULL</b>.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
Returned if the API responds with more prefixes than there is memory allocated.

</td>
</tr>
</table>
 



