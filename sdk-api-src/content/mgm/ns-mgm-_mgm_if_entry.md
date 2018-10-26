---
UID: NS:mgm._MGM_IF_ENTRY
title: "_MGM_IF_ENTRY"
author: windows-sdk-content
description: The MGM_IF_ENTRY structure describes a router interface.
old-location: rras\mgm_if_entry_str.htm
tech.root: rras
ms.assetid: df3d18fe-1f73-47fd-aab8-818f83c7fcb9
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: "*PMGM_IF_ENTRY, MGM_IF_ENTRY, MGM_IF_ENTRY structure [RAS], PMGM_IF_ENTRY, PMGM_IF_ENTRY structure pointer [RAS], _MGM_IF_ENTRY, _mpr_mgm_if_entry_str, mgm/MGM_IF_ENTRY, mgm/PMGM_IF_ENTRY, rras.mgm_if_entry_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mgm.h
api_name:
 - MGM_IF_ENTRY
product: Windows
targetos: Windows
req.typenames: MGM_IF_ENTRY, *PMGM_IF_ENTRY
req.redist: 
---

# _MGM_IF_ENTRY structure


## -description


The 
<b>MGM_IF_ENTRY</b> structure describes a router interface. This structure is used in the 
<a href="https://msdn.microsoft.com/1d161a7e-3ceb-429f-a41e-eccd7f98f084">PMGM_CREATION_ALERT_CALLBACK</a>. In the context of this callback, the routing protocol must enable or disable multicast forwarding on each interface, notifying the multicast group manager by using the <b>bIsEnabled</b> member.


## -struct-fields




### -field dwIfIndex

Specifies the index of the interface.


### -field dwIfNextHopAddr

Specifies the address of the next hop that corresponds to the index specified by <b>dwIfIndex</b>. The <b>dwIfIndex</b> and <b>dwIfNextHopIPAddr</b> members uniquely identify a next hop on point-to-multipoint interfaces. A point-to-multipoint interface is a connection where one interface connects to multiple networks. Examples of point-to-multipoint interfaces include non-broadcast multiple access (NBMA) interfaces and the internal interface on which all dial-up clients connect. 




For broadcast interfaces (such as Ethernet interfaces) or point-to-point interfaces, which are identified by only the value of <b>dwIfIndex</b>, specify zero.


### -field bIGMP

Indicates whether or not IGMP is enabled on this interface. If <b>bIGMP</b> is <b>TRUE</b>, then IGMP is enabled on this interface. If <b>bIGMP</b> is <b>FALSE</b>, then IGMP is not enabled on this interface.


### -field bIsEnabled

Indicates whether or not multicast forwarding is enabled on this interface. If <b>bIsEnabled</b> is <b>TRUE</b>, multicast forwarding is enabled on this interface. If <b>bIsEnabled</b> is <b>FALSE</b>, multicast forwarding is disabled on this interface.


## -see-also




<a href="https://msdn.microsoft.com/1d161a7e-3ceb-429f-a41e-eccd7f98f084">PMGM_CREATION_ALERT_CALLBACK</a>
 

 

