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

# CLUSTER_NODE_DRAIN_STATUS enumeration


## -description


Enumerates the possible values of the status of a node drain. This enumeration is used in the 
    <a href="https://msdn.microsoft.com/B68E19D2-2B81-496A-B090-06B6B3495268">NodeDrainStatus</a> property.


## -enum-fields




### -field NodeDrainStatusNotInitiated

Indicates that node draining has not started.


### -field NodeDrainStatusInProgress

Indicates that node draining is in progress.


### -field NodeDrainStatusCompleted

Indicates that node draining has been completed.


### -field NodeDrainStatusFailed

Indicates that node draining has failed.


### -field ClusterNodeDrainStatusCount

Defines the maximum number of drain statuses.


## -see-also




<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>



<a href="https://msdn.microsoft.com/B68E19D2-2B81-496A-B090-06B6B3495268">NodeDrainStatus</a>
 

 

