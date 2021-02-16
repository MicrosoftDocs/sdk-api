---
UID: NS:clusapi._CLUS_MAINTENANCE_MODE_INFOEX
title: CLUS_MAINTENANCE_MODE_INFOEX (clusapi.h)
description: Represents the extended maintenance mode settings for a storage class resource.
helpviewer_keywords: ["*PCLUS_MAINTENANCE_MODE_INFOEX","CLUS_MAINTENANCE_MODE_INFOEX","CLUS_MAINTENANCE_MODE_INFOEX structure [Failover Cluster]","ClusterResourceFailed","ClusterResourceInitializing","ClusterResourceOffline","ClusterResourceOfflinePending","ClusterResourceOnline","ClusterResourceOnlinePending","ClusterResourceStateUnknown","MaintenanceModeTypeDisableIsAliveCheck","MaintenanceModeTypeOfflineResource","MaintenanceModeTypeUnclusterResource","PCLUS_MAINTENANCE_MODE_INFOEX","PCLUS_MAINTENANCE_MODE_INFOEX structure pointer [Failover Cluster]","clusapi/CLUS_MAINTENANCE_MODE_INFOEX","clusapi/PCLUS_MAINTENANCE_MODE_INFOEX","mscs.clus_maintenance_mode_infoex"]
old-location: mscs\clus_maintenance_mode_infoex.htm
tech.root: MsCS
ms.assetid: d68b187d-39c5-42d3-b268-d5061da257c4
ms.date: 12/05/2018
ms.keywords: '*PCLUS_MAINTENANCE_MODE_INFOEX, CLUS_MAINTENANCE_MODE_INFOEX, CLUS_MAINTENANCE_MODE_INFOEX structure [Failover Cluster], ClusterResourceFailed, ClusterResourceInitializing, ClusterResourceOffline, ClusterResourceOfflinePending, ClusterResourceOnline, ClusterResourceOnlinePending, ClusterResourceStateUnknown, MaintenanceModeTypeDisableIsAliveCheck, MaintenanceModeTypeOfflineResource, MaintenanceModeTypeUnclusterResource, PCLUS_MAINTENANCE_MODE_INFOEX, PCLUS_MAINTENANCE_MODE_INFOEX structure pointer [Failover Cluster], clusapi/CLUS_MAINTENANCE_MODE_INFOEX, clusapi/PCLUS_MAINTENANCE_MODE_INFOEX, mscs.clus_maintenance_mode_infoex'
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
req.typenames: CLUS_MAINTENANCE_MODE_INFOEX, *PCLUS_MAINTENANCE_MODE_INFOEX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLUS_MAINTENANCE_MODE_INFOEX
 - clusapi/_CLUS_MAINTENANCE_MODE_INFOEX
 - PCLUS_MAINTENANCE_MODE_INFOEX
 - clusapi/PCLUS_MAINTENANCE_MODE_INFOEX
 - CLUS_MAINTENANCE_MODE_INFOEX
 - clusapi/CLUS_MAINTENANCE_MODE_INFOEX
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
 - CLUS_MAINTENANCE_MODE_INFOEX
---

# CLUS_MAINTENANCE_MODE_INFOEX structure


## -description

Represents the extended maintenance mode settings for a storage class resource.

## -struct-fields

### -field InMaintenance

Set to <b>TRUE</b> to enable or <b>FALSE</b> to disable maintenance 
      mode for the identified resource.
      When queried, a resource will return <b>True</b> or <b>False</b> to 
       indicate the current maintenance mode state of the resource.

### -field MaintainenceModeType

Unless the resource in question is in a type of maintenance mode, this member is set to 0.  Otherwise this member  takes an <b>enumerator</b> from the  <a href="/windows/desktop/api/clusapi/ne-clusapi-maintenance_mode_type_enum">MAINTENANCE_MODE_TYPE_ENUM</a> enumeration as its value.  The possible values of this member are as follows.



#### 0

The resource is not in maintenance mode.



#### MaintenanceModeTypeDisableIsAliveCheck (1)

Indicates that the server is ignoring the result of the resource's health check.



#### MaintenanceModeTypeOfflineResource (2)

Indicates that the server has internally performed the operations to bring the storage resource to the ClusterResourceOffline state without changing the client visible state of the resource.



#### MaintenanceModeTypeUnclusterResource (3)

Indicates the server has released ownership of the storage resource.

### -field InternalState

This member represents the internal resource state. This field is valid only when written by the server.  This member takes an enumerator from the <a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_resource_state">CLUSTER_RESOURCE_STATE</a> enumeration.  The possible values of this member are as follows.



#### ClusterResourceStateUnknown (–1)

The operation was not successful. For more information about the error, call the function 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.



#### ClusterResourceInitializing (1)

The resource is performing initialization.



#### ClusterResourceOnline (2)

The resource is operational and functioning normally.



#### ClusterResourceOffline (3)

The resource is not operational.



#### ClusterResourceFailed (4)

The resource has <a href="/previous-versions/windows/desktop/mscs/f-gly">failed</a>.



#### ClusterResourceOnlinePending (129)

The resource is in the process of coming online.



#### ClusterResourceOfflinePending (130)

The resource is in the process of going offline.

### -field Signature

A 32-bit integer that must contain the value 0xABBAF00F.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_resource_state">CLUSTER_RESOURCE_STATE</a>



<a href="/windows/desktop/api/clusapi/ne-clusapi-maintenance_mode_type_enum">MAINTENANCE_MODE_TYPE_ENUM</a>



<a href="/previous-versions/windows/desktop/mscs/utility-structures">Utility structures</a>