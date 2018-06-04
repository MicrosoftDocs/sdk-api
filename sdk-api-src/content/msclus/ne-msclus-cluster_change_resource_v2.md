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

# CLUSTER_CHANGE_RESOURCE_V2 enumeration


## -description


Defines the list of notifications that are generated for a resource.


## -enum-fields




### -field CLUSTER_CHANGE_RESOURCE_COMMON_PROPERTY_V2

Indicates that the resource's common properties have changed.


### -field CLUSTER_CHANGE_RESOURCE_PRIVATE_PROPERTY_V2

Indicates that the resource's private properties have changed.


### -field CLUSTER_CHANGE_RESOURCE_STATE_V2

Indicates that the state of the resource has changed.


### -field CLUSTER_CHANGE_RESOURCE_OWNER_GROUP_V2

Indicates that the owner group of the resource has changed.


### -field CLUSTER_CHANGE_RESOURCE_DEPENDENCIES_V2

Indicates that the resource's dependencies have changed.


### -field CLUSTER_CHANGE_RESOURCE_DEPENDENTS_V2

Indicates that the resource's dependents have changed.


### -field CLUSTER_CHANGE_RESOURCE_POSSIBLE_OWNERS_V2

Indicates that the resource's possible owner nodes have changed.


### -field CLUSTER_CHANGE_RESOURCE_DELETED_V2

Indicates that the resource has been deleted.


### -field CLUSTER_CHANGE_RESOURCE_DLL_UPGRADED_V2

Indicates that the resource's DLL has been upgraded.


### -field CLUSTER_CHANGE_RESOURCE_HANDLE_CLOSE_V2

Indicates that the resource's context handle was closed.


### -field CLUSTER_CHANGE_RESOURCE_TERMINAL_STATE_V2

TBD


### -field CLUSTER_CHANGE_RESOURCE_ALL_V2

Indicates all V2 resource notifications.


## -remarks



Protocol version 2.0 servers do not support this enumeration.



