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

# CLUSTER_CHANGE_QUORUM_V2 enumeration


## -description


Defines the notifications that are generated for quorum-specific information.


## -enum-fields




### -field CLUSTER_CHANGE_QUORUM_STATE_V2

Indicates that the quorum configuration of the cluster has changed.


### -field CLUSTER_CHANGE_QUORUM_ALL_V2

Indicates all V2 quorum notifications.


## -remarks



Protocol version 2.0 servers do not support this enumeration.



