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

# _NET_IF_MEDIA_CONNECT_STATE enumeration


## -description


The NET_IF_MEDIA_CONNECT_STATE enumeration type specifies the 
  <a href="netvista.ndis_network_interfaces2">NDIS network interface</a> connection
  state.


## -enum-fields




### -field MediaConnectStateUnknown

The connection state of the interface is unknown.


### -field MediaConnectStateConnected

The interface is connected to the network.


### -field MediaConnectStateDisconnected

The interface is not connected to the network.


## -remarks



The NDIS_MEDIA_CONNECT_STATE enumeration type, used to describe NDIS interface providers in the
    OID_GEN_MEDIA_CONNECT_STATUS_EX OID, is equivalent to this enumeration.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>typedef NET_IF_MEDIA_CONNECT_STATE NDIS_MEDIA_CONNECT_STATE, *PNDIS_MEDIA_CONNECT_STATE;</pre>
</td>
</tr>
</table></span></div>


