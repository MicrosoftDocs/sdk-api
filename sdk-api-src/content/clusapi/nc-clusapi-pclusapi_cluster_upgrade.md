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

# PCLUSAPI_CLUSTER_UPGRADE callback function


## -description


Initiates a rolling upgrade of the operating system on a cluster. <b>PCLUSAPI_CLUSTER_UPGRADE</b> defines a pointer to this function.


## -parameters




### -param hCluster [in]

A handle to the cluster to upgrade.


### -param perform [in]

<b>True</b> to initiate the rolling upgrade; otherwise <b>false</b>.


### -param pfnProgressCallback [in, optional]

A pointer to the <a href="https://msdn.microsoft.com/EE803D8C-3EFD-414F-8E38-65A1DFA8079B">ClusterUpgradeProgressCallback</a> callback function that retrieves the status of the rolling upgrade.


### -param pvCallbackArg [in, optional]

A pointer to the arguments for <b>pfnProgressCallback</b>.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>. If the operation fails, the function returns a system error code.




## -see-also




<a href="https://msdn.microsoft.com/55E9FF3F-B4B7-4A94-A515-D608A37DF84E">ClusterFunctionalLevel</a>



<a href="https://msdn.microsoft.com/1b3a3b23-39db-47b7-b4a8-17fc1ee45df6">Failover Cluster Management Functions</a>
 

 

