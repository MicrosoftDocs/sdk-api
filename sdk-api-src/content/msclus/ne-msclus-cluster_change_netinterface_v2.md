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

# CLUSTER_CHANGE_NETINTERFACE_V2 enumeration


## -description


Defines the set of notifications that are generated for a cluster network interface.


## -enum-fields




### -field CLUSTER_CHANGE_NETINTERFACE_DELETED_V2

Indicates that the cluster network interface has been deleted.


### -field CLUSTER_CHANGE_NETINTERFACE_COMMON_PROPERTY_V2

Indicates that the common properties for the cluster interface have changed.


### -field CLUSTER_CHANGE_NETINTERFACE_PRIVATE_PROPERTY_V2

Indicates that the private properties for the cluster interface have changed.


### -field CLUSTER_CHANGE_NETINTERFACE_STATE_V2

Indicates that the state of the cluster interface has changed.


### -field CLUSTER_CHANGE_NETINTERFACE_HANDLE_CLOSE_V2

Indicates that the cluster interface's context handle was closed.


### -field CLUSTER_CHANGE_NETINTERFACE_ALL_V2

Indicates all V2 network interface notifications.


## -remarks



Protocol version 2.0 servers do not support this enumeration.



