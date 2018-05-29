---
UID: NC:mgm.PMGM_LOCAL_JOIN_CALLBACK
title: PMGM_LOCAL_JOIN_CALLBACK
author: windows-sdk-content
description: The PMGM_LOCAL_JOIN_CALLBACK callback is a call into a routing protocol to notify the protocol that IGMP has detected new receivers for a group on an interface that is currently owned by the routing protocol.
old-location: rras\pmgm_local_join_callback.htm
old-project: RRAS
ms.assetid: e8245b09-0fbc-49c3-a7bb-534115c74c88
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: PMGM_LOCAL_JOIN_CALLBACK, PMGM_LOCAL_JOIN_CALLBACK callback, PMGM_LOCAL_JOIN_CALLBACK callback function [RAS], _mpr_pmgm_local_join_callback, mgm/PMGM_LOCAL_JOIN_CALLBACK, rras.pmgm_local_join_callback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
req.typenames: STREAM_MEDIUM, *PSTREAM_MEDIUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Mgm.h
api_name:
-	PMGM_LOCAL_JOIN_CALLBACK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# PMGM_LOCAL_JOIN_CALLBACK callback function


## -description


The 
<b>PMGM_LOCAL_JOIN_CALLBACK</b> callback is a call into a routing protocol to notify the protocol that IGMP has detected new receivers for a group on an interface that is currently owned by the routing protocol.

This callback is invoked when the 
<a href="https://msdn.microsoft.com/b767961e-0935-4662-9f54-d82dfa0e7bd0">MgmAddGroupMembershipEntry</a> function is called by IGMP.


## -parameters




### -param dwSourceAddr [in]

Specifies the source address from which the multicast data was received. Zero indicates that data is received from all sources (a wildcard receiver for a group); otherwise, the value of <i>dwSourceAddr</i> is the IP address of the source or source network. 




To specify a range of source addresses, the multicast group manager specifies the source network using <i>dwSourceAddr</i>, and specifies a subnet mask using <i>dwSourceMask</i>.


### -param dwSourceMask [in]

Specifies the subnet mask that corresponds to <i>dwSourceAddr</i>. The <i>dwSourceAddr</i> and <i>dwSourceMask</i> parameters are used together to define a range of sources from which to receive multicast data. 




The multicast group manager specifies zero for this parameter if it also specified zero for <i>dwSourceAddr</i> (a wildcard receiver).
						


### -param dwGroupAddr [in]

Specifies the multicast group for which the data is destined. Zero indicates that all groups are received (a wildcard receiver); otherwise the value of <i>dwGroupAddr</i> is the IP address of the group. 




To specify a range of group addresses, the multicast group manager specifies the group address using <i>dwGroupAddr</i>, and specifies a subnet mask using <i>dwGroupMask</i>.


### -param dwGroupMask [in]

Specifies the subnet mask that corresponds to <i>dwGroupAddr</i>. The <i>dwGroupAddr</i> and <i>dwGroupMask</i> parameters are used together to define a range of multicast groups. 




The multicast group manager specifies zero for this parameter if it also specified zero for <i>dwGroupAddr</i> (a wildcard receiver).


### -param dwIfIndex [in]

Specifies the interface on which the multicast data from the source should arrive.


### -param dwIfNextHopAddr [in]

Specifies the address of the next hop that corresponds to the index specified by <i>dwIfIndex</i>. The <i>dwIfIndex</i> and <i>dwIfNextHopIPAddr</i> parameters uniquely identify a next hop on point-to-multipoint interfaces. A point-to-multipoint interface is a connection where one interface connects to multiple networks. Examples of point-to-multipoint interfaces include non-broadcast multiple access (NBMA) interfaces and the internal interface on which all dial-up clients connect. 




For broadcast interfaces (such as Ethernet interfaces) or point-to-point interfaces, which are identified by only the value of <i>dwIfIndex</i>, specify zero.


## -returns



RRAS does not expect the application to return any specific value; any value returned is ignored by RRAS.





## -remarks



This version of the Multicast Group Manager API supports only wildcard sources (*, g) or specific sources (s, g), not a range of sources. The same restriction applies to groups (that is, no group ranges are permitted).




## -see-also




<a href="https://msdn.microsoft.com/9569c0e5-f9bb-4dc9-9689-f97d107697b5">PMGM_LOCAL_LEAVE_CALLBACK</a>
 

 

