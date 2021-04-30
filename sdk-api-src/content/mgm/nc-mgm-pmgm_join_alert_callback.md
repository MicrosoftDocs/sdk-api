---
UID: NC:mgm.PMGM_JOIN_ALERT_CALLBACK
title: PMGM_JOIN_ALERT_CALLBACK (mgm.h)
description: The PMGM_JOIN_ALERT_CALLBACK callback is a call into a routing protocol to notify the protocol that new receivers are present for one or more groups on interfaces that are owned by other routing protocols.
helpviewer_keywords: ["PMGM_JOIN_ALERT_CALLBACK","PMGM_JOIN_ALERT_CALLBACK callback","PMGM_JOIN_ALERT_CALLBACK callback function [RAS]","_mpr_pmgm_join_alert_callback","mgm/PMGM_JOIN_ALERT_CALLBACK","rras.pmgm_join_alert_callback"]
old-location: rras\pmgm_join_alert_callback.htm
tech.root: RRAS
ms.assetid: 6274f04c-78aa-4bce-b57d-625b0f4f6e5f
ms.date: 12/05/2018
ms.keywords: PMGM_JOIN_ALERT_CALLBACK, PMGM_JOIN_ALERT_CALLBACK callback, PMGM_JOIN_ALERT_CALLBACK callback function [RAS], _mpr_pmgm_join_alert_callback, mgm/PMGM_JOIN_ALERT_CALLBACK, rras.pmgm_join_alert_callback
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
 - PMGM_JOIN_ALERT_CALLBACK
 - mgm/PMGM_JOIN_ALERT_CALLBACK
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
 - PMGM_JOIN_ALERT_CALLBACK
---

# PMGM_JOIN_ALERT_CALLBACK callback function


## -description

The 
<b>PMGM_JOIN_ALERT_CALLBACK</b> callback is a call into a routing protocol to notify the protocol that new receivers are present for one or more groups on interfaces that are owned by other routing protocols. Once a routing protocol receives this callback, it should begin forwarding multicast data for the specified source and group.

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

### -param bMemberUpdate [in]

Specifies whether the callback was invoked because the 
<a href="/windows/desktop/api/mgm/nf-mgm-mgmaddgroupmembershipentry">MgmAddGroupMembershipEntry</a> was called by a client (the multicast group manager sets this parameter to <b>TRUE</b>), or because an MFE was created or updated (the multicast group manager sets this parameter to <b>FALSE</b>).

## -returns

RRAS does not expect the application to return any specific value; any value returned is ignored by RRAS.

## -remarks

The multicast group manager sets the <i>bMemberUpdate</i> parameter to <b>TRUE</b> and invokes this callback if a client calls the 
<a href="/windows/desktop/api/mgm/nf-mgm-mgmaddgroupmembershipentry">MgmAddGroupMembershipEntry</a> function for a (s, g), (*, g), or (*, *) entry (that is, the group membership has changed).

The multicast group manager sets the <i>bMemberUpdate</i> parameter to <b>FALSE</b> if the outgoing interface list for an MFE changes. This change typically occurs for a change in membership for the group corresponding to the MFE.

A multicast routing protocol can use the <i>bMemberUpdate</i> parameter to distinguish between changes to group membership and changes to the MFE.

The action taken by the routing protocol when this callback is received is protocol-specific. The protocol may ignore the callback if the <i>bMemberUpdate</i> parameter is set to <b>FALSE</b>, if the protocol specification indicates that this is the correct behavior.

When 
<a href="/windows/desktop/api/mgm/nf-mgm-mgmaddgroupmembershipentry">MgmAddGroupMembershipEntry</a> is called, the multicast group manager uses this callback to notify other multicast group manager clients that there are receivers for the specified source and group.

The multicast group manager uses the following rules to determine when to invoke this callback for wildcard (*, g) joins:

<ul>
<li>If this is the first client to inform the multicast group manager that there are receivers on an interface for a group, the multicast group manager invokes the 
<b>PMGM_JOIN_ALERT_CALLBACK</b> callback to all other registered clients.</li>
<li>If this is the second client to inform the multicast group manager that there are receivers on an interface for a group, the multicast group manager invokes this callback to the first client to join the group.</li>
</ul>
The multicast group manager does not invoke this callback for any subsequent joins to the group.

The multicast group manager uses the following rule to determine when to invoke this callback for source-specific (s, g) joins:

<ul>
<li>If this is the first client to inform the multicast group manager that there are receivers on an interface for a source and group, the multicast group manager invokes the 
<b>PMGM_JOIN_ALERT_CALLBACK</b> callback only for the client that owns the incoming interface towards the source "s".</li>
</ul>
This version of the Multicast Group Manager API supports only wildcard sources (*, g) or specific sources (s, g), not a range of sources. The same restriction applies to groups (that is, no group ranges are permitted).