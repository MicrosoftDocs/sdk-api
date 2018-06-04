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

# _CLUS_MAINTENANCE_MODE_INFOEX structure


## -description


Represents the extended maintenance mode settings for a storage class resource.


## -struct-fields




### -field InMaintenance

Set to <b>TRUE</b> to enable or <b>FALSE</b> to disable maintenance 
      mode for the identified resource.
      When queried, a resource will return <b>True</b> or <b>False</b> to 
       indicate the current maintenance mode state of the resource.


### -field MaintainenceModeType

Unless the resource in question is in a type of maintenance mode, this member is set to 0.  Otherwise this member  takes an <b>enumerator</b> from the  <a href="https://msdn.microsoft.com/b71f6a3b-4c9d-49f9-b60f-ee4c4fb6b169">MAINTENANCE_MODE_TYPE_ENUM</a> enumeration as its value.  The possible values of this member are as follows.



#### 0

The resource is not in maintenance mode.



#### MaintenanceModeTypeDisableIsAliveCheck (1)

Indicates that the server is ignoring the result of the resource's health check.



#### MaintenanceModeTypeOfflineResource (2)

Indicates that the server has internally performed the operations to bring the storage resource to the ClusterResourceOffline state without changing the client visible state of the resource.



#### MaintenanceModeTypeUnclusterResource (3)

Indicates the server has released ownership of the storage resource.


### -field InternalState

This member represents the internal resource state. This field is valid only when written by the server.  This member takes an enumerator from the <a href="https://msdn.microsoft.com/bd5dee18-a06f-4e46-a27e-c907b1c25a68">CLUSTER_RESOURCE_STATE</a> enumeration.  The possible values of this member are as follows.



#### ClusterResourceStateUnknown (–1)

The operation was not successful. For more information about the error, call the function 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.



#### ClusterResourceInitializing (1)

The resource is performing initialization.



#### ClusterResourceOnline (2)

The resource is operational and functioning normally.



#### ClusterResourceOffline (3)

The resource is not operational.



#### ClusterResourceFailed (4)

The resource has <a href="f_gly.htm">failed</a>.



#### ClusterResourceOnlinePending (129)

The resource is in the process of coming online.



#### ClusterResourceOfflinePending (130)

The resource is in the process of going offline.


### -field Signature

A 32-bit integer that must contain the value 0xABBAF00F.


## -see-also




<a href="https://msdn.microsoft.com/bd5dee18-a06f-4e46-a27e-c907b1c25a68">CLUSTER_RESOURCE_STATE</a>



<a href="https://msdn.microsoft.com/b71f6a3b-4c9d-49f9-b60f-ee4c4fb6b169">MAINTENANCE_MODE_TYPE_ENUM</a>



<a href="https://msdn.microsoft.com/45da8dbc-dd70-4f95-b933-66d8e4340448">Utility structures</a>
 

 

