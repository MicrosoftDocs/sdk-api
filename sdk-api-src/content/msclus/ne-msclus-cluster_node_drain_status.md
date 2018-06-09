---
UID: NE:msclus.CLUSTER_NODE_DRAIN_STATUS
title: CLUSTER_NODE_DRAIN_STATUS
author: windows-sdk-content
description: Enumerates the possible values of the status of a node drain.
old-location: mscs\cluster_node_drain_status.htm
old-project: MsCS
ms.assetid: B6BC00A8-7D1E-4A86-8756-42917160DF30
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: CLUSTER_NODE_DRAIN_STATUS, CLUSTER_NODE_DRAIN_STATUS enumeration [Failover Cluster], ClusterNodeDrainStatusCount, NodeDrainStatusCompleted, NodeDrainStatusFailed, NodeDrainStatusInProgress, NodeDrainStatusNotInitiated, clusapi/CLUSTER_NODE_DRAIN_STATUS, clusapi/ClusterNodeDrainStatusCount, clusapi/NodeDrainStatusCompleted, clusapi/NodeDrainStatusFailed, clusapi/NodeDrainStatusInProgress, clusapi/NodeDrainStatusNotInitiated, msclus/CLUSTER_NODE_DRAIN_STATUS, msclus/ClusterNodeDrainStatusCount, msclus/NodeDrainStatusCompleted, msclus/NodeDrainStatusFailed, msclus/NodeDrainStatusInProgress, msclus/NodeDrainStatusNotInitiated, mscs.cluster_node_drain_status
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: msclus.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CLUSTER_NODE_DRAIN_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusApi.h
 - MSClus.h
api_name:
 - CLUSTER_NODE_DRAIN_STATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 

