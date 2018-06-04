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

# CLUSTER_CHANGE_RESOURCE_TYPE_V2 enumeration


## -description


Defines the set of notifications that are generated for a resource type.


## -enum-fields




### -field CLUSTER_CHANGE_RESOURCE_TYPE_DELETED_V2

Indicates that the resource type has been deleted.


### -field CLUSTER_CHANGE_RESOURCE_TYPE_COMMON_PROPERTY_V2

Indicates that the resource type common properties have changed.


### -field CLUSTER_CHANGE_RESOURCE_TYPE_PRIVATE_PROPERTY_V2

Indicates that the resource type private properties have changed.


### -field CLUSTER_CHANGE_RESOURCE_TYPE_POSSIBLE_OWNERS_V2

Indicates that the possible owners for the resource type have changed.


### -field CLUSTER_CHANGE_RESOURCE_TYPE_DLL_UPGRADED_V2

Indicates that the resource type DLL has been upgraded.


### -field CLUSTER_RESOURCE_TYPE_SPECIFIC_V2

An indication that is specific to the resource type.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This member is not supported until Windows Server 2016.


### -field CLUSTER_CHANGE_RESOURCE_TYPE_ALL_V2

Indicates all V2 resource type notifications.

