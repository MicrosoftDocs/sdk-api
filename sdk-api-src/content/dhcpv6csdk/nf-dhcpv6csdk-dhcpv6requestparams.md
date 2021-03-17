---
UID: NF:dhcpv6csdk.Dhcpv6RequestParams
title: Dhcpv6RequestParams function (dhcpv6csdk.h)
description: Requests options from the DHCPv6 client cache or directly from the DHCPv6 server.
helpviewer_keywords: ["Dhcpv6RequestParams","Dhcpv6RequestParams function [DHCP]","dhcp.dhcpv6requestparams","dhcpv6csdk/Dhcpv6RequestParams"]
old-location: dhcp\dhcpv6requestparams.htm
tech.root: DHCP
ms.assetid: dfe94735-ee9d-4781-9d54-90a10d0e243a
ms.date: 12/05/2018
ms.keywords: Dhcpv6RequestParams, Dhcpv6RequestParams function [DHCP], dhcp.dhcpv6requestparams, dhcpv6csdk/Dhcpv6RequestParams
req.header: dhcpv6csdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - Dhcpv6RequestParams
 - dhcpv6csdk/Dhcpv6RequestParams
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
 - Dhcpv6RequestParams
---

# Dhcpv6RequestParams function


## -description

The Dhcpv6RequestParams function requests options from the DHCPv6 client cache or directly from the DHCPv6 server.

## -parameters

### -param forceNewInform

If this value is set to <b>TRUE</b>, any available cached information will be ignored and new information will be requested.  Otherwise, the request is only sent if there is no cached information.

### -param reserved

Reserved for future use.  Must be set to <b>NULL</b>.

### -param adapterName

GUID of the adapter for which this request is meant.  This parameter must not be <b>NULL</b>.

### -param classId

Pointer to a <a href="/windows/desktop/api/dhcpv6csdk/ns-dhcpv6csdk-dhcpv6capi_classid">DHCPV6CAPI_CLASSID</a> structure that contains the binary ClassId information to use to send on the wire. This parameter is optional.

### -param recdParams

A <a href="/windows/desktop/api/dhcpv6csdk/ns-dhcpv6csdk-dhcpv6capi_params_array">DHCPV6CAPI_PARAMS_ARRAY</a> structure that contains the parameters to be received from the DHCPV6 server.

### -param buffer

A buffer to contain information returned by some pointers in <i>recdParams</i>.

### -param pSize

Size of the buffer.  When the function returns ERROR_MORE_DATA, this parameter will contain the size, in bytes, required to complete the operation.  If the function is successful, this parameter contains the number of bytes used.

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
<li><i>reserved</i> has a value that is not <b>NULL</b>.</li>
<li><i>AdapterName</i> is <b>NULL</b>. Or no adapter is found with the GUID specified. </li>
<li><i>pSize</i> is <b>NULL</b>.</li>
<li><i>buffer</i> is <b>NULL</b>.</li>
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
The call to this API was made with insufficient memory allocated for the <i>Buffer</i> parameter, while <i>pSize</i> contains the actual memory size required.

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