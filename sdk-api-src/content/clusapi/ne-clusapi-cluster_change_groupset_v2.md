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

# CLUSTER_CHANGE_GROUPSET_V2 enumeration


## -description


Defines the list of notifications that are generated for a groupset.


## -enum-fields




### -field CLUSTER_CHANGE_GROUPSET_DELETED_v2

Indicates that a groupset was deleted.


### -field CLUSTER_CHANGE_GROUPSET_COMMON_PROPERTY_V2

Indicates that a common property of the groupset has changed.


### -field CLUSTER_CHANGE_GROUPSET_PRIVATE_PROPERTY_V2

Indicates that a private property of the groupset has changed.


### -field CLUSTER_CHANGE_GROUPSET_STATE_V2

Indicates that the group's state changed.


### -field CLUSTER_CHANGE_GROUPSET_GROUP_ADDED

Indicates that a group has been added to the groupset.


### -field CLUSTER_CHANGE_GROUPSET_GROUP_REMOVED

Indicates that a group has been removed from the groupset.


### -field CLUSTER_CHANGE_GROUPSET_DEPENDENCIES_V2

Indicates that the groupset's dependencies have changed.


### -field CLUSTER_CHANGE_GROUPSET_DEPENDENTS_V2

Indicates that the groupset's dependents have changed.


### -field CLUSTER_CHANGE_GROUPSET_HANDLE_CLOSE_v2

Indicates that the group's context handle was closed.


### -field CLUSTER_CHANGE_GROUPSET_ALL_V2

