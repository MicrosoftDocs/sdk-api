---
UID: NC:mgm.PMGM_DISABLE_IGMP_CALLBACK
title: PMGM_DISABLE_IGMP_CALLBACK (mgm.h)
description: The PMGM_DISABLE_IGMP_CALLBACK callback is a call into IGMP to notify it that a routing protocol is taking or releasing ownership of an interface on which IGMP is enabled.
helpviewer_keywords: ["MgmDisableIgmpCallback","PMGM_DISABLE_IGMP_CALLBACK","PMGM_DISABLE_IGMP_CALLBACK callback","PMGM_DISABLE_IGMP_CALLBACK callback function [RAS]","_mpr_pmgm_disable_igmp_callback","mgm/PMGM_DISABLE_IGMP_CALLBACK","rras.pmgm_disable_igmp_callback"]
old-location: rras\pmgm_disable_igmp_callback.htm
tech.root: RRAS
ms.assetid: 4f790e1b-b10f-477b-b2bc-75c95560d7f4
ms.date: 12/05/2018
ms.keywords: MgmDisableIgmpCallback, PMGM_DISABLE_IGMP_CALLBACK, PMGM_DISABLE_IGMP_CALLBACK callback, PMGM_DISABLE_IGMP_CALLBACK callback function [RAS], _mpr_pmgm_disable_igmp_callback, mgm/PMGM_DISABLE_IGMP_CALLBACK, rras.pmgm_disable_igmp_callback
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
 - PMGM_DISABLE_IGMP_CALLBACK
 - mgm/PMGM_DISABLE_IGMP_CALLBACK
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
 - PMGM_DISABLE_IGMP_CALLBACK
---

# PMGM_DISABLE_IGMP_CALLBACK callback function


## -description

The 
<b>PMGM_DISABLE_IGMP_CALLBACK</b> callback is a call into IGMP to notify it that a routing protocol is taking or releasing ownership of an interface on which IGMP is enabled.

When this callback is invoked, IGMP should stop adding and deleting group memberships on the specified interface.

## -parameters

### -param dwIfIndex [in]

Specifies the interface on which to disable IGMP.

### -param dwIfNextHopAddr [in]

Specifies the address of the next hop that corresponds to the index specified by <i>dwIfIndex</i>. The <i>dwIfIndex</i> and <i>dwIfNextHopIPAddr</i> parameters uniquely identify a next hop on point-to-multipoint interfaces. A point-to-multipoint interface is a connection where one interface connects to multiple networks. Examples of point-to-multipoint interfaces include non-broadcast multiple access (NBMA) interfaces and the internal interface on which all dial-up clients connect. 




For broadcast interfaces (such as Ethernet interfaces) or point-to-point interfaces, which are identified by only the value of <i>dwIfIndex</i>, specify zero.

## -returns

RRAS does not expect the application to return any specific value; any value returned is ignored by RRAS.

## -see-also

<a href="/windows/desktop/api/mgm/nc-mgm-pmgm_enable_igmp_callback">PMGM_ENABLE_IGMP_CALLBACK</a>