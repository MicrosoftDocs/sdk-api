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

# Dhcpv6RenewPrefix function


## -description


The <b>Dhcpv6RenewPrefix</b> function renews a prefix previously acquired with the <a href="https://msdn.microsoft.com/60f18e54-a0a4-4fbe-a416-16b924ce4616">Dhcpv6RequestPrefix</a> function.


## -parameters




### -param adapterName [in]

Name of the adapter on which the prefix renewal must be sent.


### -param pclassId

TBD


### -param prefixleaseInfo [in, out]

Pointer to a <a href="https://msdn.microsoft.com/d3e76716-a8cc-4618-a85f-d8fb9ca3257e">DHCPV6PrefixLeaseInformation</a> structure that contains the prefix lease information.


### -param pdwTimeToWait [out]

Contains the number of seconds a requesting application needs to wait before calling the <b>Dhcpv6RenewPrefix</b> function to renew its acquired prefixes.  A value of 0xFFFFFFFF indicates that the application does not need to renew its lease.


### -param bValidatePrefix [in]

Specifies  to the DHCPv6 client whether or not to send a REBIND in order to validate the prefix bindings.  <b>TRUE</b> indicates that a REBIND is required.  <b>FALSE</b> indicates RENEW is required.


#### - classId [in]

Pointer to a <a href="https://msdn.microsoft.com/90dbc386-02d9-4631-8af3-edd34537fefc">DHCPV6CAPI_CLASSID</a> structure that contains the binary ClassId information to send on the wire.

<div class="alert"><b>Note</b>  DHCPv6 Option Code 15 (0x000F) is not supported by this API. Typically, the User Class option is used by a client to identify the type or category of user or application it represents. A server selects the configuration information for the client based on the classes identified in this option.</div>
<div> </div>

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
 



