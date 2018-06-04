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

# CLUSTER_NODE_STATUS enumeration


## -description


Describes the status of a cluster node. This enumeration is used by the <b>CLUSREG_NAME_NODE_STATUS_INFO</b> property.


## -enum-fields




### -field NodeStatusNormal

The node status is normal.


### -field NodeStatusIsolated

The node has been isolated.


### -field NodeStatusQuarantined

The node has been quarantined.


### -field NodeStatusDrainInProgress

The node is in the process of being drained.


### -field NodeStatusDrainCompleted

The node has completed a node drain operation.


### -field NodeStatusDrainFailed

A node drain operation failed on the node.


### -field NodeStatusAvoidPlacement


### -field NodeStatusMax

The node has experienced a node drain failure, and is therefore isolated and quarantined.


## -see-also




<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>
 

 

