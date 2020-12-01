---
UID: NC:mgm.PMGM_ENABLE_IGMP_CALLBACK
title: PMGM_ENABLE_IGMP_CALLBACK (mgm.h)
description: The PMGM_ENABLE_IGMP_CALLBACK callback is a call into IGMP to notify it that a routing protocol has finished taking or releasing ownership of an interface.
helpviewer_keywords: ["PMGM_ENABLE_IGMP_CALLBACK","PMGM_ENABLE_IGMP_CALLBACK callback","PMGM_ENABLE_IGMP_CALLBACK callback function [RAS]","_mpr_pmgm_enable_igmp_callback","mgm/PMGM_ENABLE_IGMP_CALLBACK","rras.pmgm_enable_igmp_callback"]
old-location: rras\pmgm_enable_igmp_callback.htm
tech.root: RRAS
ms.assetid: 6c23779b-d759-4443-a134-0ff27c48dc8e
ms.date: 12/05/2018
ms.keywords: PMGM_ENABLE_IGMP_CALLBACK, PMGM_ENABLE_IGMP_CALLBACK callback, PMGM_ENABLE_IGMP_CALLBACK callback function [RAS], _mpr_pmgm_enable_igmp_callback, mgm/PMGM_ENABLE_IGMP_CALLBACK, rras.pmgm_enable_igmp_callback
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
 - PMGM_ENABLE_IGMP_CALLBACK
 - mgm/PMGM_ENABLE_IGMP_CALLBACK
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
 - PMGM_ENABLE_IGMP_CALLBACK
---

# PMGM_ENABLE_IGMP_CALLBACK callback function


## -description

The 
<b>PMGM_ENABLE_IGMP_CALLBACK</b> callback is a call into IGMP to notify it that a routing protocol has finished taking or releasing ownership of an interface.

When this callback is invoked, IGMP should add all its group memberships on the specified interface using calls to the 
<a href="/windows/desktop/api/mgm/nf-mgm-mgmaddgroupmembershipentry">MgmAddGroupMembershipEntry</a> function.

## -parameters

### -param dwIfIndex [in]

Specifies the index of the interface on which to enable IGMP.

### -param dwIfNextHopAddr [in]

Specifies the address of the next hop that corresponds to the index specified by <i>dwIfIndex</i>. The <i>dwIfIndex</i> and <i>dwIfNextHopIPAddr</i> parameters uniquely identify a next hop on point-to-multipoint interfaces. A point-to-multipoint interface is a connection where one interface connects to multiple networks. Examples of point-to-multipoint interfaces include non-broadcast multiple access (NBMA) interfaces and the internal interface on which all dial-up clients connect. 




For broadcast interfaces (such as Ethernet interfaces) or point-to-point interfaces, which are identified by only the value of <i>dwIfIndex</i>, specify zero.

## -returns

RRAS does not expect the application to return any specific value; any value returned is ignored by RRAS.

## -remarks

IGMP must not add group memberships in the context of this callback. The multicast group manager and IGMP  become deadlocked.

## -see-also

<a href="/windows/desktop/api/mgm/nc-mgm-pmgm_disable_igmp_callback">PMGM_DISABLE_IGMP_CALLBACK</a>