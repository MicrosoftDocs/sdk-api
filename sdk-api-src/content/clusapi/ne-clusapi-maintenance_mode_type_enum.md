---
UID: NE:clusapi._MAINTENANCE_MODE_TYPE_ENUM
title: MAINTENANCE_MODE_TYPE_ENUM (clusapi.h)
description: Defines the possible states that a storage class resource can be placed in when marked for maintenance.
helpviewer_keywords: ["*PMAINTENANCE_MODE_TYPE_ENUM","MAINTENANCE_MODE_TYPE_ENUM","MAINTENANCE_MODE_TYPE_ENUM enumeration [Failover Cluster]","MaintenanceModeTypeDisableIsAliveCheck","MaintenanceModeTypeOfflineResource","MaintenanceModeTypeUnclusterResource","PMAINTENANCE_MODE_TYPE_ENUM","PMAINTENANCE_MODE_TYPE_ENUM enumeration pointer [Failover Cluster]","clusapi/MAINTENANCE_MODE_TYPE_ENUM","clusapi/MaintenanceModeTypeDisableIsAliveCheck","clusapi/MaintenanceModeTypeOfflineResource","clusapi/MaintenanceModeTypeUnclusterResource","clusapi/PMAINTENANCE_MODE_TYPE_ENUM","mscs.maintenance_mode_type_enum"]
old-location: mscs\maintenance_mode_type_enum.htm
tech.root: MsCS
ms.assetid: b71f6a3b-4c9d-49f9-b60f-ee4c4fb6b169
ms.date: 12/05/2018
ms.keywords: '*PMAINTENANCE_MODE_TYPE_ENUM, MAINTENANCE_MODE_TYPE_ENUM, MAINTENANCE_MODE_TYPE_ENUM enumeration [Failover Cluster], MaintenanceModeTypeDisableIsAliveCheck, MaintenanceModeTypeOfflineResource, MaintenanceModeTypeUnclusterResource, PMAINTENANCE_MODE_TYPE_ENUM, PMAINTENANCE_MODE_TYPE_ENUM enumeration pointer [Failover Cluster], clusapi/MAINTENANCE_MODE_TYPE_ENUM, clusapi/MaintenanceModeTypeDisableIsAliveCheck, clusapi/MaintenanceModeTypeOfflineResource, clusapi/MaintenanceModeTypeUnclusterResource, clusapi/PMAINTENANCE_MODE_TYPE_ENUM, mscs.maintenance_mode_type_enum'
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
req.typenames: MAINTENANCE_MODE_TYPE_ENUM, *PMAINTENANCE_MODE_TYPE_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MAINTENANCE_MODE_TYPE_ENUM
 - clusapi/_MAINTENANCE_MODE_TYPE_ENUM
 - PMAINTENANCE_MODE_TYPE_ENUM
 - clusapi/PMAINTENANCE_MODE_TYPE_ENUM
 - MAINTENANCE_MODE_TYPE_ENUM
 - clusapi/MAINTENANCE_MODE_TYPE_ENUM
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
 - MAINTENANCE_MODE_TYPE_ENUM
---

# MAINTENANCE_MODE_TYPE_ENUM enumeration


## -description

Defines the possible states that a storage class resource can be placed in when marked for maintenance.

## -enum-fields

### -field MaintenanceModeTypeDisableIsAliveCheck:1

Indicates that the server is ignoring the result of the resource's health check.

### -field MaintenanceModeTypeOfflineResource:2

Indicates that the server has internally performed the operations to bring the storage resource to the ClusterResourceOffline state without changing the client visible state of the resource.

### -field MaintenanceModeTypeUnclusterResource:3

Indicates the server has released ownership of the storage resource.

## -see-also

<a href="/windows/desktop/api/clusapi/ns-clusapi-clus_maintenance_mode_infoex">CLUS_MAINTENANCE_MODE_INFOEX</a>



<a href="/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>



<a href="/previous-versions/windows/desktop/mscs/maintenancemode">MaintenanceMode</a>
