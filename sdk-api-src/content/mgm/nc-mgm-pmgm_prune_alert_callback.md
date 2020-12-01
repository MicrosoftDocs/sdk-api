---
UID: NC:mgm.PMGM_PRUNE_ALERT_CALLBACK
title: PMGM_PRUNE_ALERT_CALLBACK (mgm.h)
description: The PMGM_PRUNE_ALERT_CALLBACK callback is a call into a routing protocol to notify the protocol that receivers are no longer present on interfaces owned by other routing protocols.
helpviewer_keywords: ["MgmPruneAlertCallback","PMGM_PRUNE_ALERT_CALLBACK","PMGM_PRUNE_ALERT_CALLBACK callback","PMGM_PRUNE_ALERT_CALLBACK callback function [RAS]","_mpr_pmgm_prune_alert_callback","mgm/PMGM_PRUNE_ALERT_CALLBACK","rras.pmgm_prune_alert_callback"]
old-location: rras\pmgm_prune_alert_callback.htm
tech.root: RRAS
ms.assetid: 1c23df04-2a31-475e-a8da-783796a60e00
ms.date: 12/05/2018
ms.keywords: MgmPruneAlertCallback, PMGM_PRUNE_ALERT_CALLBACK, PMGM_PRUNE_ALERT_CALLBACK callback, PMGM_PRUNE_ALERT_CALLBACK callback function [RAS], _mpr_pmgm_prune_alert_callback, mgm/PMGM_PRUNE_ALERT_CALLBACK, rras.pmgm_prune_alert_callback
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
 - PMGM_PRUNE_ALERT_CALLBACK
 - mgm/PMGM_PRUNE_ALERT_CALLBACK
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
 - PMGM_PRUNE_ALERT_CALLBACK
---

# PMGM_PRUNE_ALERT_CALLBACK callback function


## -description

The 
<b>PMGM_PRUNE_ALERT_CALLBACK</b> callback is a call into a routing protocol to notify the protocol that receivers are no longer present on interfaces owned by other routing protocols.

## -parameters

### -param dwSourceAddr [in]

Specifies the source address from which to stop receiving multicast data. Zero indicates to stop receiving data from all sources (a wildcard receiver for a group); otherwise, the value of <i>dwSourceAddr</i> is the IP address of the source or source network. 




To specify a range of source addresses, the multicast group manager specifies the source network using <i>dwSourceAddr</i>, and specifies a subnet mask using <i>dwSourceMask</i>.

### -param dwSourceMask [in]

Specifies the subnet mask that corresponds to <i>dwSourceAddr</i>. The <i>dwSourceAddr</i> and <i>dwSourceMask</i> parameters are used together to define a range of sources from which to stop receiving receive multicast data. 




The multicast group manager specifies zero for this parameter if it also specified zero for <i>dwSourceAddr</i> (a wildcard receiver).

### -param dwGroupAddr [in]

Specifies the multicast group for which to stop receiving data. Zero indicates to stop receiving data for all groups (a wildcard receiver); otherwise, the value of <i>dwGroupAddr</i> is the IP address of the group. 




To specify a range of group addresses, the multicast group manager specifies the group address using <i>dwGroupAddr</i>, and specifies a subnet mask using <i>dwGroupMask</i>.

### -param dwGroupMask [in]

Specifies the subnet mask that corresponds to <i>dwGroupAddr</i>. The <i>dwGroupAddr</i> and <i>dwGroupMask</i> parameters are used together to define a range of multicast groups. 




The multicast group manager specifies zero for this parameter if it also specified zero for <i>dwGroupAddr</i> (a wildcard receiver).

### -param dwIfIndex [in]

Specifies the interface on which to stop receiving multicast data.

### -param dwIfNextHopAddr [in]

Specifies the address of the next hop that corresponds to the index specified by <i>dwIfIndex</i>. The <i>dwIfIndex</i> and <i>dwIfNextHopIPAddr</i> parameters uniquely identify a next hop on point-to-multipoint interfaces. A point-to-multipoint interface is a connection where one interface connects to multiple networks. Examples of point-to-multipoint interfaces include non-broadcast multiple access (NBMA) interfaces and the internal interface on which all dial-up clients connect. 




For broadcast interfaces (such as Ethernet interfaces) or point-to-point interfaces, which are identified by only the value of <i>dwIfIndex</i>, specify zero.

### -param bMemberDelete [in]

Specifies whether the callback was invoked because the 
<a href="/windows/desktop/api/mgm/nf-mgm-mgmaddgroupmembershipentry">MgmAddGroupMembershipEntry</a> was called by a client (the multicast group manager sets this parameter to <b>TRUE</b>), or because an MFE was created or updated (the multicast group manager sets this parameter to <b>FALSE</b>).

### -param pdwTimeout [in, out]

On input, <i>pdwTimeout</i> points to a <b>DWORD</b>-sized memory location. 




If <i>bMemberDelete</i> is <b>FALSE</b>, this parameter can be used to specify how long the corresponding MFE should remain in the multicast forwarding cache. If the client does not specify a value, the default value is 900 seconds.

On output, <i>pdwTimeout</i> receives the time-out value, in seconds, for this MFE.

## -returns

RRAS does not expect the application to return any specific value; any value returned is ignored by RRAS.

## -remarks

The multicast group manager sets the <i>bMemberDelete</i> parameter to <b>TRUE</b> and invokes this callback if a client calls the 
<a href="/windows/desktop/api/mgm/nf-mgm-mgmdeletegroupmembershipentry">MgmDeleteGroupMembershipEntry</a> function for a (s, g), (*, g), or (*, *) entry (that is, the group membership changes).

The multicast group manager sets the <i>bMemberDelete</i> parameter to <b>FALSE</b> if the outgoing interface list for an MFE changes. This change typically occurs for a change in membership for the group corresponding to the MFE.

A multicast routing protocol can use the <i>bMemberDelete</i> parameter to distinguish between changes to group membership and changes to the MFE.

The action taken by the routing protocol when this callback is received is protocol-specific. The protocol may ignore the callback if the <i>bMemberDelete</i> parameter is set to <b>FALSE</b>, if the protocol specification indicates that this is the correct behavior.

When 
<a href="/windows/desktop/api/mgm/nf-mgm-mgmdeletegroupmembershipentry">MgmDeleteGroupMembershipEntry</a> is called, the multicast group manager uses this callback to notify other multicast group manager clients that there are no more receivers for the specified source and group.

The multicast group manager uses the following rules to determine when to invoke this callback for wildcard (*, g) joins:

<ul>
<li>If the final interface is being removed for the second-to-last client (that is, when interfaces for only a single client remain), the multicast group manager invokes the 
<b>PMGM_PRUNE_ALERT_CALLBACK</b> callback to that remaining client.</li>
<li>If the final interface is being removed for the last client (that is, when no other interfaces remain), then this callback is invoked for all the other clients that are registered with the multicast group manager.</li>
</ul>
The multicast group manager uses the following rule to determine when to invoke this callback for source-specific (s, g) joins:

<ul>
<li>When a source-specific prune for a group (s, g) is received, the multicast group manager invokes the 
<b>PMGM_PRUNE_ALERT_CALLBACK</b> callback only for the client that owns the incoming interface towards the source "s".</li>
</ul>
This version of the Multicast Group Manager API supports only wildcard sources (*, g) or specific sources (s, g), not a range of sources. The same restriction applies to groups (that is, no group ranges are permitted).

## -see-also

<a href="/windows/desktop/api/mgm/nc-mgm-pmgm_creation_alert_callback">PMGM_CREATION_ALERT_CALLBACK</a>