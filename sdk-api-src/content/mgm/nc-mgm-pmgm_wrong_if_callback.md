---
UID: NC:mgm.PMGM_WRONG_IF_CALLBACK
title: PMGM_WRONG_IF_CALLBACK (mgm.h)
description: The PMGM_WRONG_IF_CALLBACK is a call into a routing protocol to notify the protocol that a packet has been received from the specified source and for the specified group on the wrong interface.
helpviewer_keywords: ["MgmWrongIfCallback","PMGM_WRONG_IF_CALLBACK","PMGM_WRONG_IF_CALLBACK callback","PMGM_WRONG_IF_CALLBACK callback function [RAS]","_mpr_pmgm_wrong_if_callback","mgm/PMGM_WRONG_IF_CALLBACK","rras.pmgm_wrong_if_callback"]
old-location: rras\pmgm_wrong_if_callback.htm
tech.root: RRAS
ms.assetid: d74f6984-35a0-42f4-8460-b7ad2fbba1b8
ms.date: 12/05/2018
ms.keywords: MgmWrongIfCallback, PMGM_WRONG_IF_CALLBACK, PMGM_WRONG_IF_CALLBACK callback, PMGM_WRONG_IF_CALLBACK callback function [RAS], _mpr_pmgm_wrong_if_callback, mgm/PMGM_WRONG_IF_CALLBACK, rras.pmgm_wrong_if_callback
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
 - PMGM_WRONG_IF_CALLBACK
 - mgm/PMGM_WRONG_IF_CALLBACK
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
 - PMGM_WRONG_IF_CALLBACK
---

# PMGM_WRONG_IF_CALLBACK callback function


## -description

The 
<b>PMGM_WRONG_IF_CALLBACK</b> is a call into a routing protocol to notify the protocol that a packet has been received from the specified source and for the specified group on the wrong interface.

## -parameters

### -param dwSourceAddr [in]

Specifies the source address from which the multicast data was received. Zero indicates that data is received from all sources (a wildcard receiver for a group); otherwise, the value of <i>dwSourceAddr</i> is the IP address of the source or source network.

### -param dwGroupAddr [in]

Specifies the multicast group for which the data is destined. Zero indicates that all groups are received (a wildcard receiver); otherwise, the value of <i>dwGroupAddr</i> is the IP address of the group.

### -param dwIfIndex [in]

Specifies the interface on which the packet arrived.

### -param dwIfNextHopAddr [in]

Specifies the address of the next hop that corresponds to the index specified by <i>dwIfIndex</i>. The <i>dwIfIndex</i> and <i>dwIfNextHopIPAddr</i> parameters uniquely identify a next hop on point-to-multipoint interfaces. A point-to-multipoint interface is a connection where one interface connects to multiple networks. Examples of point-to-multipoint interfaces include non-broadcast multiple access (NBMA) interfaces and the internal interface on which all dial-up clients connect. 




For broadcast interfaces (such as Ethernet interfaces) or point-to-point interfaces, which are identified by only the value of <i>dwIfIndex</i>, specify zero.

### -param dwHdrSize [in]

Specifies, in bytes, the size of the buffer pointed to by <i>pbPacketHdr</i>.

### -param pbPacketHdr [in]

Pointer to a buffer that contains the IP header of the packet, including the IP options and a fragment of the data. This parameter is used by those protocols that examine the contents of the packet header.

## -returns

RRAS does not expect the application to return any specific value; any value returned is ignored by RRAS.

## -remarks

This callback is not currently available.

