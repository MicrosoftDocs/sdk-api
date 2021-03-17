---
UID: NF:dhcpv6csdk.Dhcpv6ReleasePrefix
title: Dhcpv6ReleasePrefix function (dhcpv6csdk.h)
description: Releases a prefix.
helpviewer_keywords: ["Dhcpv6ReleasePrefix","Dhcpv6ReleasePrefix function [DHCP]","dhcp.dhcpv6releaseprefix","dhcpv6csdk/Dhcpv6ReleasePrefix"]
old-location: dhcp\dhcpv6releaseprefix.htm
tech.root: DHCP
ms.assetid: 252646db-f8d2-42d1-87af-2426dff2c72c
ms.date: 12/05/2018
ms.keywords: Dhcpv6ReleasePrefix, Dhcpv6ReleasePrefix function [DHCP], dhcp.dhcpv6releaseprefix, dhcpv6csdk/Dhcpv6ReleasePrefix
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
 - Dhcpv6ReleasePrefix
 - dhcpv6csdk/Dhcpv6ReleasePrefix
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
 - Dhcpv6ReleasePrefix
---

# Dhcpv6ReleasePrefix function


## -description

The <a href="/previous-versions/windows/desktop/api/dhcpv6csdk/nf-dhcpv6csdk-dhcpv6requestprefix">Dhcpv6ReleasePrefix</a> function releases  a prefix previously acquired with the <b>Dhcpv6RequestPrefix</b> function.

## -parameters

### -param adapterName [in]

Name of the adapter on which the PD request must be sent.

### -param classId [in]

Pointer to a <a href="/windows/desktop/api/dhcpv6csdk/ns-dhcpv6csdk-dhcpv6capi_classid">DHCPV6CAPI_CLASSID</a> structure that contains the binary ClassId information to use to send on the wire.

<div class="alert"><b>Note</b>   DHCPv6 Option Code 15 (0x000F) is not supported by this API. Typically, the User Class option is used by a client to identify the type or category of user or application it represents. A server selects the configuration information for the client based on the classes identified in this option.</div>
<div> </div>

### -param leaseInfo [in]

Pointer to a <a href="/windows/desktop/api/dhcpv6csdk/ns-dhcpv6csdk-dhcpv6prefixleaseinformation">DHCPV6CAPIPrefixLeaseInformation</a> structure that is used to release the prefix.

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
<li><i>AdapterName</i> is <b>NULL</b>. Or no adapter is found with the GUID specified.</li>
<li><i>prefixleaseInfo</i> is <b>NULL</b>.</li>
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

## -remarks

Release messages sent as the result of the call to this function must  contain the following values for the <b>T1</b> and <b>T2</b> fields of the  <a href="/windows/desktop/api/dhcpv6csdk/ns-dhcpv6csdk-dhcpv6prefixleaseinformation">DHCPV6CAPIPrefixLeaseInformation</a> structure supplied in the <i>prefixleaseInfo</i> parameter:

<ul>
<li><b>T1</b>: the renewal time for the prefix, in seconds specified as absolute time values.</li>
<li><b>T2</b>: the rebind time of the prefix, in seconds specified as absolute time values.
</li>
</ul>