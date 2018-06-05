---
UID: NC:clusapi.PCLUSAPI_CLUSTER_UPGRADE
title: PCLUSAPI_CLUSTER_UPGRADE
author: windows-sdk-content
description: Initiates a rolling upgrade of the operating system on a cluster. PCLUSAPI_CLUSTER_UPGRADE defines a pointer to this function.
old-location: mscs\clusterupgradefunctionallevel.htm
old-project: MsCS
ms.assetid: EA013501-A4E2-48D8-9062-D20141485CC5
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: PCLUSAPI_CLUSTER_UPGRADE, PCLUSAPI_CLUSTER_UPGRADE callback, PCLUSAPI_CLUSTER_UPGRADE callback function [Failover Cluster], clusapi/PCLUSAPI_CLUSTER_UPGRADE, mscs.clusterupgradefunctionallevel
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
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
req.typenames: Sources
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ClusAPI.h
api_name:
-	PCLUSAPI_CLUSTER_UPGRADE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

