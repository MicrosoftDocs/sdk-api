---
UID: NF:dhcpv6csdk.Dhcpv6ReleasePrefix
title: Dhcpv6ReleasePrefix function
author: windows-sdk-content
description: Releases a prefix.
old-location: dhcp\dhcpv6releaseprefix.htm
tech.root: DHCP
ms.assetid: 252646db-f8d2-42d1-87af-2426dff2c72c
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Dhcpv6ReleasePrefix, Dhcpv6ReleasePrefix function [DHCP], dhcp.dhcpv6releaseprefix, dhcpv6csdk/Dhcpv6ReleasePrefix
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - Dhcpv6ReleasePrefix
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Dhcpv6ReleasePrefix function


## -description


The <a href="https://msdn.microsoft.com/60f18e54-a0a4-4fbe-a416-16b924ce4616">Dhcpv6ReleasePrefix</a> function releases  a prefix previously acquired with the <b>Dhcpv6RequestPrefix</b> function.


## -parameters




### -param adapterName [in]

Name of the adapter on which the PD request must be sent.


### -param classId [in]

Pointer to a <a href="https://msdn.microsoft.com/90dbc386-02d9-4631-8af3-edd34537fefc">DHCPV6CAPI_CLASSID</a> structure that contains the binary ClassId information to use to send on the wire.

<div class="alert"><b>Note</b>   DHCPv6 Option Code 15 (0x000F) is not supported by this API. Typically, the User Class option is used by a client to identify the type or category of user or application it represents. A server selects the configuration information for the client based on the classes identified in this option.</div>
<div> </div>

### -param leaseInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/d3e76716-a8cc-4618-a85f-d8fb9ca3257e">DHCPV6CAPIPrefixLeaseInformation</a> structure that is used to release the prefix.


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
</ul>
</td>
</tr>
</table>
 




## -remarks



Release messages sent as the result of the call to this function must  contain the following values for the <b>T1</b> and <b>T2</b> fields of the  <a href="https://msdn.microsoft.com/d3e76716-a8cc-4618-a85f-d8fb9ca3257e">DHCPV6CAPIPrefixLeaseInformation</a> structure supplied in the <i>prefixleaseInfo</i> parameter:

<ul>
<li><b>T1</b>: the renewal time for the prefix, in seconds specified as absolute time values.</li>
<li><b>T2</b>: the rebind time of the prefix, in seconds specified as absolute time values.
</li>
</ul>


