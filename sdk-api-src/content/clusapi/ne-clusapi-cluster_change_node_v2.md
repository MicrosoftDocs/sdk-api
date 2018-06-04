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

# CLUSTER_CHANGE_NODE_V2 enumeration


## -description


Defines the notifications that are generated for a cluster node.


## -enum-fields




### -field CLUSTER_CHANGE_NODE_NETINTERFACE_ADDED_V2

Indicates that the network interface for the cluster node has been added.


### -field CLUSTER_CHANGE_NODE_DELETED_V2

Indicates that the cluster node has been deleted.


### -field CLUSTER_CHANGE_NODE_COMMON_PROPERTY_V2

Indicates that the common properties for the cluster node have been changed.


### -field CLUSTER_CHANGE_NODE_PRIVATE_PROPERTY_V2

Indicates that the private properties for the cluster node have been changed.


### -field CLUSTER_CHANGE_NODE_STATE_V2

Indicates that the state of the cluster node has changed.


### -field CLUSTER_CHANGE_NODE_GROUP_GAINED_V2

Indicates that the cluster node has gained a group.


### -field CLUSTER_CHANGE_NODE_GROUP_LOST_V2

Indicates that the cluster node has lost a group.


### -field CLUSTER_CHANGE_NODE_HANDLE_CLOSE_V2

Indicates that the cluster node's context handle was closed.


### -field CLUSTER_CHANGE_NODE_ALL_V2

Indicates all V2 cluster node notifications.


## -remarks



Protocol version 2.0 servers do not support this enumeration.



