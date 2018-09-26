---
UID: NE:ifdef._NET_IF_MEDIA_CONNECT_STATE
title: "_NET_IF_MEDIA_CONNECT_STATE"
author: windows-sdk-content
description: The NET_IF_MEDIA_CONNECT_STATE enumeration type specifies the NDIS network interface connection state.
old-location: netvista\net_if_media_connect_state.htm
tech.root: NetVista
ms.assetid: 5af5e050-4b2b-45a9-8549-3a3818d7b06f
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: "*PNET_IF_MEDIA_CONNECT_STATE, MediaConnectStateConnected, MediaConnectStateDisconnected, MediaConnectStateUnknown, NET_IF_MEDIA_CONNECT_STATE, NET_IF_MEDIA_CONNECT_STATE enumeration [Network Drivers Starting with Windows Vista], PNET_IF_MEDIA_CONNECT_STATE, PNET_IF_MEDIA_CONNECT_STATE enumeration pointer [Network Drivers Starting with Windows Vista], _NET_IF_MEDIA_CONNECT_STATE, ifdef/MediaConnectStateConnected, ifdef/MediaConnectStateDisconnected, ifdef/MediaConnectStateUnknown, ifdef/NET_IF_MEDIA_CONNECT_STATE, ifdef/PNET_IF_MEDIA_CONNECT_STATE, net_if_enums_ref_567021be-60dc-4356-bc88-1430769b9ac8.xml, netvista.net_if_media_connect_state"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: ifdef.h
req.include-header: Netioapi.h, Ntddndis.h
req.target-type: Windows
req.target-min-winverclnt: Supported in NDIS 6.0 and later.
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ifdef.h
api_name:
 - NET_IF_MEDIA_CONNECT_STATE
product: Windows
targetos: Windows
req.typenames: NET_IF_MEDIA_CONNECT_STATE, *PNET_IF_MEDIA_CONNECT_STATE
req.redist: 
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


