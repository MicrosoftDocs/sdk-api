---
UID: NC:mgm.PMGM_CREATION_ALERT_CALLBACK
title: PMGM_CREATION_ALERT_CALLBACK (mgm.h)
description: The PMGM_CREATION_ALERT_CALLBACK callback is a call into a routing protocol. This call determines the subset of interfaces owned by the routing protocol on which a multicast packet from a new source should be forwarded.
helpviewer_keywords: ["MgmCreationAlertCallback","PMGM_CREATION_ALERT_CALLBACK","PMGM_CREATION_ALERT_CALLBACK callback","PMGM_CREATION_ALERT_CALLBACK callback function [RAS]","_mpr_pmgm_creation_alert_callback","mgm/PMGM_CREATION_ALERT_CALLBACK","rras.pmgm_creation_alert_callback"]
old-location: rras\pmgm_creation_alert_callback.htm
tech.root: RRAS
ms.assetid: 1d161a7e-3ceb-429f-a41e-eccd7f98f084
ms.date: 12/05/2018
ms.keywords: MgmCreationAlertCallback, PMGM_CREATION_ALERT_CALLBACK, PMGM_CREATION_ALERT_CALLBACK callback, PMGM_CREATION_ALERT_CALLBACK callback function [RAS], _mpr_pmgm_creation_alert_callback, mgm/PMGM_CREATION_ALERT_CALLBACK, rras.pmgm_creation_alert_callback
req.header: mgm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PMGM_CREATION_ALERT_CALLBACK
 - mgm/PMGM_CREATION_ALERT_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Mgm.h
api_name:
 - PMGM_CREATION_ALERT_CALLBACK
---

# PMGM_CREATION_ALERT_CALLBACK callback function


## -description

The 
<b>PMGM_CREATION_ALERT_CALLBACK</b> callback is a call into a routing protocol. This call determines the subset of interfaces owned by the routing protocol on which a multicast packet from a new source should be forwarded.

When a packet sent from a new source, or destined for a new group, arrives on an interface, the multicast group manager creates a new MFE. The multicast group manager then invokes this callback to those routing protocols that have outgoing interfaces in this new MFE. A routing protocol can choose to disable the forwarding of data from the source to the group on specific interfaces.

## -parameters

### -param dwSourceAddr [in]

Specifies the source address from which the multicast data was received. Zero indicates that data is received from all sources (a wildcard receiver for a group); otherwise, the value of <i>dwSourceAddr</i> is the IP address of the source or source network. 




To specify a range of source addresses, the multicast group manager specifies the source network using <i>dwSourceAddr</i>, and specifies a subnet mask using <i>dwSourceMask</i>.

### -param dwSourceMask [in]

Specifies the subnet mask that corresponds to <i>dwSourceAddr</i>. The <i>dwSourceAddr</i> and <i>dwSourceMask</i> parameters are used together to define a range of sources from which to receive multicast data. 




The multicast group manager specifies zero for this parameter if it also specified zero for <i>dwSourceAddr</i> (a wildcard receiver).

### -param dwGroupAddr [in]

Specifies the multicast group for which the data is destined. Zero indicates that all groups are received (a wildcard receiver); otherwise, the value of <i>dwGroupAddr</i> is the IP address of the group. 




To specify a range of group addresses, the multicast group manager specifies the group address using <i>dwGroupAddr</i>, and specifies a subnet mask using <i>dwGroupMask</i>.

### -param dwGroupMask [in]

Specifies the subnet mask that corresponds to <i>dwGroupAddr</i>. The <i>dwGroupAddr</i> and <i>dwGroupMask</i> parameters are used together to define a range of multicast groups. 




The multicast group manager specifies zero for this parameter if it also specified zero for <i>dwGroupAddr</i> (a wildcard receiver).

### -param dwInIfIndex [in]

Specifies the interface on which the multicast data from the source should arrive.

### -param dwInIfNextHopAddr [in]

Specifies the address of the next hop that corresponds to the index specified by <i>dwIfIndex</i>. The <i>dwIfIndex</i> and <i>dwIfNextHopIPAddr</i> parameters uniquely identify a next hop on point-to-multipoint interfaces. A point-to-multipoint interface is a connection where one interface connects to multiple networks. Examples of point-to-multipoint interfaces include non-broadcast multiple access (NBMA) interfaces and the internal interface on which all dial-up clients connect. 




For broadcast interfaces (such as Ethernet interfaces) or point-to-point interfaces, which are identified by only the value of <i>dwIfIndex</i>, specify zero.

### -param dwIfCount [in]

Specifies the number of interfaces in the buffer pointed to by <i>pmieOutIfList</i>.

### -param pmieOutIfList [in, out]

On input, a pointer to a buffer that contains the set of interfaces owned by the protocol on which data will be forwarded. 




On output, the client can set the <b>bIsEnabled</b> member of the corresponding 
<a href="/windows/desktop/api/mgm/ns-mgm-mgm_if_entry">MGM_IF_ENTRY</a> structure to <b>FALSE</b> to prevent forwarding on any of its interfaces. A client may not be required to prevent forwarding; such a client would accept the default value of <b>bIsEnabled</b>.

## -returns

RRAS does not expect the application to return any specific value; any value returned is ignored by RRAS.

## -see-also

<a href="/windows/desktop/api/mgm/ns-mgm-mgm_if_entry">MGM_IF_ENTRY</a>