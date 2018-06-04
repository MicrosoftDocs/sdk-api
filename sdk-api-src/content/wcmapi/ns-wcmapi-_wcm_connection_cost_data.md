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

# _WCM_CONNECTION_COST_DATA structure


## -description


The <b>WCM_CONNECTION_COST_DATA</b> structure specifies information about a connection cost.


## -struct-fields




### -field ConnectionCost

Type: <b>DWORD</b>

Specifies the connection cost type.


This must include one (and only one) of the following flags:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WCM_CONNECTION_COST_UNKNOWN"></a><a id="wcm_connection_cost_unknown"></a><dl>
<dt><b>WCM_CONNECTION_COST_UNKNOWN</b></dt>
<dt>0x0</dt>
</dl>
</td>
<td width="60%">
Connection cost information is not available.

</td>
</tr>
<tr>
<td width="40%"><a id="WCM_CONNECTION_COST_UNRESTRICTED"></a><a id="wcm_connection_cost_unrestricted"></a><dl>
<dt><b>WCM_CONNECTION_COST_UNRESTRICTED</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
The connection is unlimited and has unrestricted usage constraints.

</td>
</tr>
<tr>
<td width="40%"><a id="WCM_CONNECTION_COST_FIXED"></a><a id="wcm_connection_cost_fixed"></a><dl>
<dt><b>WCM_CONNECTION_COST_FIXED</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
Usage counts toward a fixed allotment of data which the user has already paid for (or agreed to pay for).

</td>
</tr>
<tr>
<td width="40%"><a id="WCM_CONNECTION_COST_VARIABLE"></a><a id="wcm_connection_cost_variable"></a><dl>
<dt><b>WCM_CONNECTION_COST_VARIABLE</b></dt>
<dt>0x4</dt>
</dl>
</td>
<td width="60%">
The connection cost is on a per-byte basis.

</td>
</tr>
</table>
 

And may include any combination of the following flags:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WCM_CONNECTION_COST_OVERDATALIMIT"></a><a id="wcm_connection_cost_overdatalimit"></a><dl>
<dt><b>WCM_CONNECTION_COST_OVERDATALIMIT</b></dt>
<dt>0x10000</dt>
</dl>
</td>
<td width="60%">
The connection has exceeded its data limit.

</td>
</tr>
<tr>
<td width="40%"><a id="WCM_CONNECTION_COST_CONGESTED"></a><a id="wcm_connection_cost_congested"></a><dl>
<dt><b>WCM_CONNECTION_COST_CONGESTED</b></dt>
<dt>0x20000</dt>
</dl>
</td>
<td width="60%">
The connection is throttled due to high traffic.

</td>
</tr>
<tr>
<td width="40%"><a id="WCM_CONNECTION_COST_ROAMING"></a><a id="wcm_connection_cost_roaming"></a><dl>
<dt><b>WCM_CONNECTION_COST_ROAMING</b></dt>
<dt>0x40000</dt>
</dl>
</td>
<td width="60%">
The connection is outside of the home network.

</td>
</tr>
</table>
 


### -field CostSource

Type: <b><a href="https://msdn.microsoft.com/cd9e5562-dd50-46fc-be11-0ea89e6933c0">WCM_CONNECTION_COST_SOURCE</a></b>

Specifies the cost source.


## -see-also




<a href="https://msdn.microsoft.com/cd9e5562-dd50-46fc-be11-0ea89e6933c0">WCM_CONNECTION_COST_SOURCE</a>
 

 

