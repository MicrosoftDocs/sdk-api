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

# CLUSTER_OBJECT_TYPE enumeration


## -description


Defines the type of object for which a notification is requested or generated.


## -enum-fields




### -field CLUSTER_OBJECT_TYPE_NONE

The notification is for an unspecified type.


### -field CLUSTER_OBJECT_TYPE_CLUSTER

The notification is for the cluster.


### -field CLUSTER_OBJECT_TYPE_GROUP

The notification is for a group.


### -field CLUSTER_OBJECT_TYPE_RESOURCE

The notification is for a resource.


### -field CLUSTER_OBJECT_TYPE_RESOURCE_TYPE

The notification is for a resource type.


### -field CLUSTER_OBJECT_TYPE_NETWORK_INTERFACE

The notification is for a cluster network interface.


### -field CLUSTER_OBJECT_TYPE_NETWORK

The notification is for a cluster network.


### -field CLUSTER_OBJECT_TYPE_NODE

The notification is for a cluster node.


### -field CLUSTER_OBJECT_TYPE_REGISTRY

The notification is for a cluster registry key.


### -field CLUSTER_OBJECT_TYPE_QUORUM

The notification is for a quorum resource.


### -field CLUSTER_OBJECT_TYPE_SHARED_VOLUME

The notification is for a cluster shared volume.


### -field CLUSTER_OBJECT_TYPE_GROUPSET

The notification is for a groupset.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This value is unavailable prior to Windows Server 2016.

