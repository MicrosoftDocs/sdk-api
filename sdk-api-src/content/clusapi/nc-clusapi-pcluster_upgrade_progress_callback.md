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

# PCLUSTER_UPGRADE_PROGRESS_CALLBACK callback function


## -description


Retrieves status information for a rolling upgrade of the operating system on a cluster. <b>PCLUSTER_UPGRADE_PROGRESS_CALLBACK</b> type defines a pointer to this function.


## -parameters




### -param pvCallbackArg

A pointer to the arguments.


### -param eUpgradePhase

A  <a href="https://msdn.microsoft.com/75FB1BCD-03E0-4A6F-8C97-99AE8E958174">CLUSTER_UPGRADE_PHASE</a> enumeration values that indicates the state of the rolling upgrade.


## -returns




This function returns one of the following values:






## -see-also




<a href="https://msdn.microsoft.com/EA013501-A4E2-48D8-9062-D20141485CC5">ClusterUpgradeFunctionalLevel</a>



<a href="https://msdn.microsoft.com/1b3a3b23-39db-47b7-b4a8-17fc1ee45df6">Failover Cluster Management Functions</a>
 

 

