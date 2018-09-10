---
UID: NF:dhcpv6csdk.Dhcpv6RequestParams
title: Dhcpv6RequestParams function
author: windows-sdk-content
description: Requests options from the DHCPv6 client cache or directly from the DHCPv6 server.
old-location: dhcp\dhcpv6requestparams.htm
tech.root: dhcp
ms.assetid: dfe94735-ee9d-4781-9d54-90a10d0e243a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Dhcpv6RequestParams, Dhcpv6RequestParams function [DHCP], dhcp.dhcpv6requestparams, dhcpv6csdk/Dhcpv6RequestParams
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dhcpcsvc6.dll
api_name:
 - Dhcpv6RequestParams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

Name of the adapter for which this request is meant.  This parameter must not be <b>NULL</b>.


### -param classId

Pointer to a <a href="https://msdn.microsoft.com/90dbc386-02d9-4631-8af3-edd34537fefc">DHCPV6CAPI_CLASSID</a> structure that contains the binary ClassId information to use to send on the wire.


### -param recdParams

A <a href="https://msdn.microsoft.com/2392586f-94a0-4667-b59a-88c0e1d88713">DHCPV6CAPI_PARAMS_ARRAY</a> structure that contains the parameters to be received from the DHCPV6 server.


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
<li><i>AdapterName</i> is <b>NULL</b>.</li>
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
</table>
 



