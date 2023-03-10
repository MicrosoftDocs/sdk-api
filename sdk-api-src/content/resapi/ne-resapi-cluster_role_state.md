---
UID: NE:resapi._CLUSTER_ROLE_STATE
title: CLUSTER_ROLE_STATE (resapi.h)
description: Defines the potential return values for the ResUtilGetClusterRoleState function.
helpviewer_keywords: ["CLUSTER_ROLE_STATE","CLUSTER_ROLE_STATE enumeration [Failover Cluster]","ClusterRoleClustered","ClusterRoleUnclustered","ClusterRoleUnknown","mscs.cluster_role_state","resapi/CLUSTER_ROLE_STATE","resapi/ClusterRoleClustered","resapi/ClusterRoleUnclustered","resapi/ClusterRoleUnknown"]
old-location: mscs\cluster_role_state.htm
tech.root: MsCS
ms.assetid: 21424e31-4eba-4ff9-95c1-0908827936df
ms.date: 12/05/2018
ms.keywords: CLUSTER_ROLE_STATE, CLUSTER_ROLE_STATE enumeration [Failover Cluster], ClusterRoleClustered, ClusterRoleUnclustered, ClusterRoleUnknown, mscs.cluster_role_state, resapi/CLUSTER_ROLE_STATE, resapi/ClusterRoleClustered, resapi/ClusterRoleUnclustered, resapi/ClusterRoleUnknown
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise
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
req.typenames: CLUSTER_ROLE_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLUSTER_ROLE_STATE
 - resapi/_CLUSTER_ROLE_STATE
 - CLUSTER_ROLE_STATE
 - resapi/CLUSTER_ROLE_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ResApi.h
api_name:
 - CLUSTER_ROLE_STATE
---

# CLUSTER_ROLE_STATE enumeration


## -description

Defines the potential return values for the <a href="/previous-versions/windows/desktop/api/resapi/nf-resapi-resutilgetclusterrolestate">ResUtilGetClusterRoleState</a> function.

## -enum-fields

### -field ClusterRoleUnknown:-1

It is unknown whether or not the role is clustered.

### -field ClusterRoleClustered

The role is clustered.

### -field ClusterRoleUnclustered

The role is not clustered.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>



<a href="/previous-versions/windows/desktop/api/resapi/nf-resapi-resutilgetclusterrolestate">ResUtilGetClusterRoleState</a>
