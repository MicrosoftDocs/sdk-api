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

# CLUSTER_CHANGE_GROUP_V2 enumeration


## -description


Defines the list of notifications that are generated for a group.


## -enum-fields




### -field CLUSTER_CHANGE_GROUP_DELETED_V2

Indicates that a group was deleted.


### -field CLUSTER_CHANGE_GROUP_COMMON_PROPERTY_V2

Indicates that a group's common property changed.


### -field CLUSTER_CHANGE_GROUP_PRIVATE_PROPERTY_V2

Indicates that a group's private property changed.


### -field CLUSTER_CHANGE_GROUP_STATE_V2

Indicates that the group's state changed.


### -field CLUSTER_CHANGE_GROUP_OWNER_NODE_V2

Indicates that the group's owner node has changed.


### -field CLUSTER_CHANGE_GROUP_PREFERRED_OWNERS_V2

Indicates that the group's preferred owners have changed.


### -field CLUSTER_CHANGE_GROUP_RESOURCE_ADDED_V2

Indicates that a resource was added to the group.


### -field CLUSTER_CHANGE_GROUP_RESOURCE_GAINED_V2

Indicates that the group gained a resource.


### -field CLUSTER_CHANGE_GROUP_RESOURCE_LOST_V2

Indicates that a resource is no longer part of the group.


### -field CLUSTER_CHANGE_GROUP_HANDLE_CLOSE_V2

Indicates that the group's context handle was closed.


### -field CLUSTER_CHANGE_GROUP_ALL_V2

Indicates all V2 group notifications.


## -remarks



Protocol version 2.0 servers do not support this enumeration.



