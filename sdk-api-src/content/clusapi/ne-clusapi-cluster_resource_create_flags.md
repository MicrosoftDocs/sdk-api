---
UID: NE:clusapi.CLUSTER_RESOURCE_CREATE_FLAGS
title: CLUSTER_RESOURCE_CREATE_FLAGS (clusapi.h)
description: Determines which resource monitor a given resource will be assigned to.
helpviewer_keywords: ["CLUSTER_RESOURCE_CREATE_FLAGS","CLUSTER_RESOURCE_CREATE_FLAGS enumeration [Failover Cluster]","CLUSTER_RESOURCE_DEFAULT_MONITOR","CLUSTER_RESOURCE_SEPARATE_MONITOR","CLUSTER_RESOURCE_VALID_FLAGS","_CLUSTER_RESOURCE_CREATE_FLAGS","_CLUSTER_RESOURCE_CREATE_FLAGS enumeration [Failover Cluster]","clusapi/CLUSTER_RESOURCE_CREATE_FLAGS","clusapi/CLUSTER_RESOURCE_DEFAULT_MONITOR","clusapi/CLUSTER_RESOURCE_SEPARATE_MONITOR","clusapi/CLUSTER_RESOURCE_VALID_FLAGS","clusapi/_CLUSTER_RESOURCE_CREATE_FLAGS","msclus/CLUSTER_RESOURCE_CREATE_FLAGS","msclus/CLUSTER_RESOURCE_DEFAULT_MONITOR","msclus/CLUSTER_RESOURCE_SEPARATE_MONITOR","msclus/CLUSTER_RESOURCE_VALID_FLAGS","msclus/_CLUSTER_RESOURCE_CREATE_FLAGS","mscs.cluster_resource_create_flags"]
old-location: mscs\cluster_resource_create_flags.htm
tech.root: MsCS
ms.assetid: 16f5ab58-2507-431a-98f9-bd00a24485ba
ms.date: 12/05/2018
ms.keywords: CLUSTER_RESOURCE_CREATE_FLAGS, CLUSTER_RESOURCE_CREATE_FLAGS enumeration [Failover Cluster], CLUSTER_RESOURCE_DEFAULT_MONITOR, CLUSTER_RESOURCE_SEPARATE_MONITOR, CLUSTER_RESOURCE_VALID_FLAGS, _CLUSTER_RESOURCE_CREATE_FLAGS, _CLUSTER_RESOURCE_CREATE_FLAGS enumeration [Failover Cluster], clusapi/CLUSTER_RESOURCE_CREATE_FLAGS, clusapi/CLUSTER_RESOURCE_DEFAULT_MONITOR, clusapi/CLUSTER_RESOURCE_SEPARATE_MONITOR, clusapi/CLUSTER_RESOURCE_VALID_FLAGS, clusapi/_CLUSTER_RESOURCE_CREATE_FLAGS, msclus/CLUSTER_RESOURCE_CREATE_FLAGS, msclus/CLUSTER_RESOURCE_DEFAULT_MONITOR, msclus/CLUSTER_RESOURCE_SEPARATE_MONITOR, msclus/CLUSTER_RESOURCE_VALID_FLAGS, msclus/_CLUSTER_RESOURCE_CREATE_FLAGS, mscs.cluster_resource_create_flags
req.header: clusapi.h
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
req.typenames: CLUSTER_RESOURCE_CREATE_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSTER_RESOURCE_CREATE_FLAGS
 - clusapi/CLUSTER_RESOURCE_CREATE_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
 - MsClus.h
api_name:
 - CLUSTER_RESOURCE_CREATE_FLAGS
---

# CLUSTER_RESOURCE_CREATE_FLAGS enumeration


## -description

Determines which resource monitor a given resource will be assigned to.

## -enum-fields

### -field CLUSTER_RESOURCE_DEFAULT_MONITOR:0

The <a href="/previous-versions/windows/desktop/mscs/cluster-service">Cluster service</a> determines the 
      <a href="/previous-versions/windows/desktop/mscs/resource-monitor">Resource Monitor</a> to which the new resource will be 
      assigned.

### -field CLUSTER_RESOURCE_SEPARATE_MONITOR:1

Causes the Cluster service to create a separate Resource Monitor dedicated exclusively to the new 
      resource.

### -field CLUSTER_RESOURCE_VALID_FLAGS

Contains all valid flags for the 
      <a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_resource_create_flags">CLUSTER_RESOURCE_CREATE_FLAGS</a> 
      enumeration.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-createclusterresource">CreateClusterResource</a>



<a href="/previous-versions/windows/desktop/mscs/clusresdependencies-createitem">CreateItem Method of the ClusResDependencies Object</a>



<a href="/previous-versions/windows/desktop/mscs/clusresdependents-createitem">CreateItem Method of the ClusResDependents Object</a>



<a href="/previous-versions/windows/desktop/mscs/clusrestyperesources-createitem">CreateItem Method of the ClusResTypeResources Object</a>



<a href="/previous-versions/windows/desktop/mscs/clusresources-createitem">CreateItem Method of the ClusResources Object</a>



<a href="/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>
