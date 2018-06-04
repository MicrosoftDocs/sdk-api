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

# CLUSTER_CHANGE_NODE_UPGRADE_PHASE_V2 enumeration


## -description


Defines the notifications that are generated for the upgrade of a cluster node.


## -enum-fields




### -field CLUSTER_CHANGE_UPGRADE_NODE_PREPARE

Indicates that the upgrade is being prepared.


### -field CLUSTER_CHANGE_UPGRADE_NODE_COMMIT

Indicates that the upgrade is in progress.


### -field CLUSTER_CHANGE_UPGRADE_NODE_POSTCOMMIT

Indicates that the upgrade is finished.


### -field CLUSTER_CHANGE_UPGRADE_ALL

Indicates all <b>CLUSTER_CHANGE_NODE_UPGRADE_PHASE_V2</b> notifications.


## -see-also




<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>
 

 

