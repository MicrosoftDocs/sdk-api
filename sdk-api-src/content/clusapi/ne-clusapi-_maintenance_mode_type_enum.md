---
UID: NE:clusapi._MAINTENANCE_MODE_TYPE_ENUM
title: "_MAINTENANCE_MODE_TYPE_ENUM"
author: windows-sdk-content
description: Defines the possible states that a storage class resource can be placed in when marked for maintenance.
old-location: mscs\maintenance_mode_type_enum.htm
tech.root: mscs
ms.assetid: b71f6a3b-4c9d-49f9-b60f-ee4c4fb6b169
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: "*PMAINTENANCE_MODE_TYPE_ENUM, MAINTENANCE_MODE_TYPE_ENUM, MAINTENANCE_MODE_TYPE_ENUM enumeration [Failover Cluster], MaintenanceModeTypeDisableIsAliveCheck, MaintenanceModeTypeOfflineResource, MaintenanceModeTypeUnclusterResource, PMAINTENANCE_MODE_TYPE_ENUM, PMAINTENANCE_MODE_TYPE_ENUM enumeration pointer [Failover Cluster], _MAINTENANCE_MODE_TYPE_ENUM, clusapi/MAINTENANCE_MODE_TYPE_ENUM, clusapi/MaintenanceModeTypeDisableIsAliveCheck, clusapi/MaintenanceModeTypeOfflineResource, clusapi/MaintenanceModeTypeUnclusterResource, clusapi/PMAINTENANCE_MODE_TYPE_ENUM, mscs.maintenance_mode_type_enum"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - MAINTENANCE_MODE_TYPE_ENUM
product: Windows
targetos: Windows
req.typenames: MAINTENANCE_MODE_TYPE_ENUM, *PMAINTENANCE_MODE_TYPE_ENUM
req.redist: 
---

# _MAINTENANCE_MODE_TYPE_ENUM enumeration


## -description


Defines the possible states that a storage class resource can be placed in when marked for maintenance.


## -enum-fields




### -field MaintenanceModeTypeDisableIsAliveCheck

Indicates that the server is ignoring the result of the resource's health check.


### -field MaintenanceModeTypeOfflineResource

Indicates that the server has internally performed the operations to bring the storage resource to the ClusterResourceOffline state without changing the client visible state of the resource.


### -field MaintenanceModeTypeUnclusterResource

Indicates the server has released ownership of the storage resource.


## -see-also




<a href="https://msdn.microsoft.com/d68b187d-39c5-42d3-b268-d5061da257c4">CLUS_MAINTENANCE_MODE_INFOEX</a>



<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>



<a href="https://msdn.microsoft.com/af592311-15e6-4ad9-b7bd-4ef62bfd761f">MaintenanceMode</a>
 

 

