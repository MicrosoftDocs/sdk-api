---
UID: NC:mgm.PMGM_RPF_CALLBACK
title: PMGM_RPF_CALLBACK (mgm.h)
description: The PMGM_RPF_CALLBACK callback is a call into a routing protocol to determine if a given packet was received on the correct interface.
helpviewer_keywords: ["MgmRpfCallback","PMGM_RPF_CALLBACK","PMGM_RPF_CALLBACK callback","PMGM_RPF_CALLBACK callback function [RAS]","_mpr_pmgm_rpf_callback","mgm/PMGM_RPF_CALLBACK","rras.pmgm_rpf_callback"]
old-location: rras\pmgm_rpf_callback.htm
tech.root: RRAS
ms.assetid: 114a44c2-e352-45b9-9842-cfb369072c84
ms.date: 12/05/2018
ms.keywords: MgmRpfCallback, PMGM_RPF_CALLBACK, PMGM_RPF_CALLBACK callback, PMGM_RPF_CALLBACK callback function [RAS], _mpr_pmgm_rpf_callback, mgm/PMGM_RPF_CALLBACK, rras.pmgm_rpf_callback
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
 - PMGM_RPF_CALLBACK
 - mgm/PMGM_RPF_CALLBACK
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
 - PMGM_RPF_CALLBACK
---

# PMGM_RPF_CALLBACK callback function


## -description

The 
<b>PMGM_RPF_CALLBACK</b> callback is a call into a routing protocol to determine if a given packet was received on the correct interface.

This callback is invoked when a packet from a new source or destined for a new group is received. The multicast group manager invokes this callback to the routing protocol that owns the incoming interface towards the source.

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

### -param pdwInIfIndex [in, out]

On input, a pointer to a <b>DWORD</b>-sized memory location that specifies the index of the interface on which data from the source is expected to be received, based on the multicast view of the routing table. 




On output, <i>pdwInIfIndex</i> points to a <b>DWORD</b>-sized memory location that contains the index of the interface on which the protocol expects to receive packets. The interface index may differ on output from the index specified on input.

### -param pdwInIfNextHopAddr [in, out]

On input, <i>pdwInIfNextHopAddr</i> specifies the address of the next hop that corresponds to the index specified by <i>dwIfIndex</i>. 




The <i>dwIfIndex</i> and <i>dwIfNextHopIPAddr</i> parameters uniquely identify a next hop on point-to-multipoint interfaces. A point-to-multipoint interface is a connection where one interface connects to multiple networks. Examples of point-to-multipoint interfaces include non-broadcast multiple access (NBMA) interfaces and the internal interface on which all dial-up clients connect.

For broadcast interfaces (such as Ethernet interfaces) or point-to-point interfaces, which are identified by only the value of <i>dwIfIndex</i>, specify zero.

On output, <i>pdwInIfNextHopAddr</i> points to the next hop that corresponds to <i>pdwInIfIndex</i>.

### -param pdwUpStreamNbr [in, out]

On input, <i>pdwUpStreamNbr</i> points to a <b>DWORD</b> value specifying the immediate upstream neighbor towards the source (the source is found in the multicast view of the routing table). 




On output, <i>pdwUpStreamNbr</i> may have been modified by the protocol. This parameter is for informational purposes only.

### -param dwHdrSize [in]

Specifies, in bytes, the size of the buffer pointed to by <i>pbPacketHdr</i>.

### -param pbPacketHdr [in]

Pointer to a buffer that contains the IP header of the packet, including the IP options and a fragment of the data. This parameter is used by those protocols that examine the contents of the packet header.

### -param pbRoute [in, out]

On input, <i>pbRoute</i> points to a buffer that contains the route towards the source. The buffer contains an 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_dest_info">RTM_DEST_INFO</a> structure. 




On output, <i>pbRoute</i> points to a buffer that contains the route used by the protocol to determine the interface towards the source.

## -returns

RRAS does not expect the application to return any specific value; any value returned is ignored by RRAS.

## -remarks

This callback is invoked when an MFE is created. MFEs are created when data from a new multicast source, or destined to a new group, is received.

The multicast group manager invokes this callback to the routing protocol that owns the incoming interface towards the source. The multicast group manager determines the interface by looking up the source of the multicast data in the multicast view of the routing table. This interface is not always the same as the interface on which the data was actually received; this condition occurs if multicast data was received on the wrong interface.

When this callback is invoked, the routing protocol can change the incoming interface if the routing protocol behavior requires it to receive the data for the group from another interface.