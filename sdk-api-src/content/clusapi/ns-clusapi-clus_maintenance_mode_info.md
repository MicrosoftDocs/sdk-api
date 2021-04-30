---
UID: NS:clusapi.CLUS_MAINTENANCE_MODE_INFO
title: CLUS_MAINTENANCE_MODE_INFO (clusapi.h)
description: Enables or disables maintenance mode on a cluster node.
helpviewer_keywords: ["*PCLUS_MAINTENANCE_MODE_INFO","CLUS_MAINTENANCE_MODE_INFO","CLUS_MAINTENANCE_MODE_INFO structure [Failover Cluster]","PCLUS_MAINTENANCE_MODE_INFO","PCLUS_MAINTENANCE_MODE_INFO structure pointer [Failover Cluster]","clusapi/CLUS_MAINTENANCE_MODE_INFO","clusapi/PCLUS_MAINTENANCE_MODE_INFO","mscs.clus_maintenance_mode_info"]
old-location: mscs\clus_maintenance_mode_info.htm
tech.root: MsCS
ms.assetid: dc53dc5e-b7ed-49f8-a08f-495e2c0e45e2
ms.date: 12/05/2018
ms.keywords: '*PCLUS_MAINTENANCE_MODE_INFO, CLUS_MAINTENANCE_MODE_INFO, CLUS_MAINTENANCE_MODE_INFO structure [Failover Cluster], PCLUS_MAINTENANCE_MODE_INFO, PCLUS_MAINTENANCE_MODE_INFO structure pointer [Failover Cluster], clusapi/CLUS_MAINTENANCE_MODE_INFO, clusapi/PCLUS_MAINTENANCE_MODE_INFO, mscs.clus_maintenance_mode_info'
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise with SP1, Windows Server 2008 Datacenter with SP1
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
req.typenames: CLUS_MAINTENANCE_MODE_INFO, *PCLUS_MAINTENANCE_MODE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUS_MAINTENANCE_MODE_INFO
 - clusapi/CLUS_MAINTENANCE_MODE_INFO
 - PCLUS_MAINTENANCE_MODE_INFO
 - clusapi/PCLUS_MAINTENANCE_MODE_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUS_MAINTENANCE_MODE_INFO
---

# CLUS_MAINTENANCE_MODE_INFO structure


## -description

Enables or disables maintenance mode on a cluster node.

## -struct-fields

### -field InMaintenance

Set to <b>TRUE</b> to enable or <b>FALSE</b> to disable maintenance 
      mode for the identified resource.

When queried, a resource will return <b>True</b> or <b>False</b> to 
       indicate the current maintenance mode state of the resource.

## -remarks

When using <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterresourcecontrol">ClusterResourceControl</a> to enable 
    or disable maintenance mode on a specified resource, the calling routine can specify a larger buffer with addition 
    resource-specific data by including it immediately after the 
    <b>CLUS_MAINTENANCE_MODE_INFO</b> structure. This 
    data then becomes private to the resource as it cannot be retrieved by the calling program using the 
    <a href="/previous-versions/windows/desktop/mscs/clusctl-resource-query-maintenance-mode">CLUSCTL_RESOURCE_QUERY_MAINTENANCE_MODE</a> 
    control code.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-query-maintenance-mode">CLUSCTL_RESOURCE_QUERY_MAINTENANCE_MODE</a>



<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-set-maintenance-mode">CLUSCTL_RESOURCE_SET_MAINTENANCE_MODE</a>



<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterresourcecontrol">ClusterResourceControl</a>



<a href="/previous-versions/windows/desktop/mscs/utility-structures">Utility structures</a>