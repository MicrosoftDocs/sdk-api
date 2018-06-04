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

# IRpcOptions interface


## -description


Enables callers to set or query the values of various properties that control how COM handles remote procedure calls (RPC).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRpcOptions</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IRpcOptions</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRpcOptions</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406403">Query</a>
</td>
<td align="left" width="63%">
Retrieves the value of an RPC binding option property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff544503">Set</a>
</td>
<td align="left" width="63%">
Sets the value of an RPC binding option property.

</td>
</tr>
</table> 


## -remarks



Using this interface, callers can set or query the COMBND_RPCTIMEOUT property, which controls how long your machine will attempt to establish RPC communications with another before failing. The property can have any one of the values enumerated in the following table.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>RPC_C_BINDING_INFINITE_TIMEOUT
</td>
<td>Keep trying to establish communications with no timeout.
</td>
</tr>
<tr>
<td>RPC_C_BINDING_MIN_TIMEOUT
</td>
<td>Try to establish communications for the minimum time required by the protocol. This value favors performance over reliability.</td>
</tr>
<tr>
<td>RPC_C_BINDING_DEFAULT_TIMEOUT
</td>
<td>Try to establish communications for the default time. The value strikes a balance between performance and reliability.</td>
</tr>
<tr>
<td>RPC_C_BINDING_MAX_TIMEOUT
</td>
<td>Try to establish communications for the maximum time allowed by the protocol. This value favors reliability over performance.</td>
</tr>
</table>
 



