---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

